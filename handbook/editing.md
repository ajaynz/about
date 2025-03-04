# Editing the handbook

Every Sourcegraph teammate will be editing the Sourcegraph handbook frequently to keep information up-to-date and participate in important changes in the company. This guide helps everyone learn how to edit the handbook.

The handbook consists of Markdown files in the Git repository at [github.com/sourcegraph/about](https://github.com/sourcegraph/about). ([Why not a wiki or Google Docs?](usage.md#wiki-and-google-docs-handbooks-become-stale))

## How to get help

We don't expect everyone on the team to figure this out on their own. Other teammates are happy to help!

- Any engineer at Sourcegraph can help. (The *code* that engineers write at Sourcegraph also consists of files in a Git repository, so engineers are very familiar with making these kinds of edits.)
- [Teammates who have already made a handbook change](https://sourcegraph.com/github.com/sourcegraph/about/-/stats/contributors?path=handbook%2F) can help.
- **Handbook support**: Ask the @handbook-support group in Slack (formerly called "handbook heroes"), including @eric, @aharvey, @virginia, @ines, and @jean, for handbook help (via DM, #handbook, or #any-question). They volunteered to help anyone with anything handbook-related! _If you too want to be part of handbook support, simply edit this page, add your name to the list and ping @handbook-support in the #handbook channel to inform them_
- Ask in #handbook: `Who can screen-share with me to help me make an edit to the handbook?`
- Don't be afraid of breaking anything! It is very easy for any engineer on the team to roll back to the previous version of the handbook if you make a mistake.

## Overview

Here's the process for getting a change published to the handbook. For detailed step-by-step instructions (intended for people who are new to Git), see the sections below.

1. Propose the edits you want to make by creating a [pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) on the Git repository at [github.com/sourcegraph/about](https://github.com/sourcegraph/about).
   - Because the [handbook is public](usage.md#why-make-this-handbook-public), anyone in the world can see your proposed edits.
1. Make sure the [handbook checks pass](#handbook-checks).
1. You can request a review from specific teammates (who will get a notification) on the GitHub pull request page.
   - We don't have any rules around who needs to review what changes. Use your judgment (e.g., if your change affects the entire engineering team, request review from the VP Engineering).
   - For minor edits, you can skip review.
1. Wait for the necessary teammates to review and approve your pull request.
1. Merge the pull request.
1. Wait up to 5 minutes for your change to be live on about.sourcegraph.com.
1. Use the #handbook-announce label to notify other people of important handbook updates on the #handbook-announce Slack channel.

## Reviewing and approving another person's proposal

Frequently used links:

- [All proposed (and not yet merged) handbook changes](https://github.com/sourcegraph/about/pulls?q=is%3Apr+is%3Aopen+sort%3Aupdated-desc)
- [Proposed handbook changes waiting on review by you](https://github.com/sourcegraph/about/pulls?q=is%3Apr+is%3Aopen+sort%3Aupdated-desc+review-requested%3A%40me)
- [Proposed handbook changes submitted by you](https://github.com/sourcegraph/about/pulls?q=is%3Apr+is%3Aopen+sort%3Aupdated-desc+author%3A%40me)

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Q8tUXKU66Sk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Edit a single file

If you just need to edit a single page, you can do it entirely on the web.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/MsIGvw0IEzo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br/>

1. Visit the handbook page you want to edit on about.sourcegraph.com.
1. Press the **Edit this page** button in the sidebar.
   - If you don't see it, you may be viewing a page on about.sourcegraph.com that is not part of the handbook. Handbook pages all have the same design as the [main handbook page](https://about.sourcegraph.com/handbook). If it has a different design, [ask for help](#how-to-get-help).
1. In the text editor, make your edits.
   - The document is in a format called Markdown that lets you use headings, links, bold, lists, etc., in a plain text file. See "[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)" and feel free to [ask for help](#how-to-get-help).
1. Switch back and forth to the **Preview changes** tab at the top of the editor to see the nicely rendered page with your edits applied.
   - Deletions are shown in red, changes are shown in orange, and additions are shown in green.
1. When you're happy with your edits, scroll to the bottom of the page to the **Commit changes** box.
   - Type a short, one-line summary of your change in the first text field (instead of the default `Update filename.md` text).
   - Type a more detailed explanation of your change in the larger text field.
   - Select the **Create a new branch for this commit and start a pull request** option (if it's not already selected).
   - Press the **Commit changes** button.
1. Press the **Create pull request** button. Now your change has been proposed!
   - You can share the link to the pull request with anyone to show them your proposed change (e.g., `https://github.com/sourcegraph/about/pull/123).
1. If you want this update to be published in the Slack channel #handbook-announce, select the handbook-announce label using the **Label** button on the right side of the pull request page.
1. Select teammates to review using the **Reviewers** button on the right side of the pull request page.
1. Wait for teammates to review, comment on, and approve your pull request.
1. When you're ready to publish the change and make it live, press the **Squash and merge** button, then press **Confirm squash and merge**.
1. Wait up to 5 minutes for your change to be live on about.sourcegraph.com.

### Handbook checks

>If you are running the handbook locally, you can run these checks before you push your commit, [explained in the readme](https://github.com/sourcegraph/about#handbook).

On your Github pull request page, you'll notice a green checkmark or a red X-mark next to your commits. This information repeated at the end of the page with a "Some checks were not successful" in red or "All checks have passed" in green.

These "checks" are automated formatting and structural rules that run on your new changes. The goal is to help you catch common errors before you merge your pull request to the handbook, because if a handbook user hits these errors when they are live, it's a poor experience.

Ideally, you won't merge your pull request unless all checks have passed and are "green." If you see any red failed checks then you can click the red "X" and then click on the tooltip to be taken to more details ([example page with red X build](https://github.com/sourcegraph/about/pull/3564); [example details page](https://github.com/sourcegraph/about/runs/2976049292)). 

If you're not sure what the error message means or can't determine how to fix it, you are welcome to ask for help in Slack's #handbook and optionally tag @handbook-support, but first refer to the common errors:

#### Interpreting handbook check failures: most common examples

- **Must link to .md files ([example](https://github.com/sourcegraph/about/runs/2976049292))**: `handbook/product/user_feedback.md: must link to .md file, not ../support/support-workflow` means that the error is in the file (handbook page) `handbook/product/user_feedback.md`, and the error is that there is a link to a URL rather than the markdown file of the page itself. 
  - **Fix:** add an `.md` and make the link to `../support/support-workflow.md` instead of `../support/support-workflow`. 
  - **Note:** if there is an anchor tag in the link, the `.md` goes before the anchor tag, like `../support/support-workflow.md#support-workflow`. 
- **Disconnected page ([example](https://github.com/sourcegraph/about/runs/2975885844)):** `handbook/engineering/hiring/engineering-leadership.md: disconnected page (no inlinks from other pages)` means that the error is _not_ in the file `handbook/engineering/hiring/engineering-leadership.md`, but rather there are no pages in the handbook linking to this file page. 
   - **Fix:** Determine if this page is still valuable, and if so, on which other handbook page to add a link to this page. If it's not obvious or you're not sure, you should post for help in #handbook and tag someone you think might know better (based on the content of the disconnected page). 

## Edit multiple files or add a new file

To make edits to multiple files and submit all of the edits as a group to be reviewed together, you will follow a more complex process than when [editing a single file](#edit-a-single-file). This also is required for adding new files.

> NOTE: These steps are not exhaustively documented. Please [ask for help](#how-to-get-help) as many times as you need to until you feel comfortable with this process.

### Web interface

#### Multiple changes in a single PR

A screen recording of how to make multiple changes in a single PR in the web interface for GitHub:

<iframe src="https://drive.google.com/file/d/1UL3JqbXEGLaVXEkk4G81wGO69z8J_Cbw/preview" width="560" height="315"></iframe>

#### Making a new page

A screen recording of how to make a new file and include it for review in the web interface for GitHub:

<iframe src="https://drive.google.com/file/d/16iYS-idCL5FEGwoldF7rOQElcidgzo8i/preview" width="560" height="315"></iframe>

### macOS

### Github Desktop version
Here's a screen recording of the steps (written out below) for macOS:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/diZUeHZhekc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Prerequisites

1. Download and install [GitHub Desktop](https://desktop.github.com/).
1. Launch GitHub Desktop and sign into it using your GitHub username.
1. Clone the `sourcegraph/about` repository (assuming to the `~/Documents/GitHub/about` folder on your computer).

Optional:

- Use [Typora](https://www.typora.io/) to edit and preview Markdown (`.md`) files.

#### Steps

1. In GitHub Desktop, open the `about` repository that you cloned previously.
1. In **Current Branch**, select `main` if it's not already selected.
1. Press the **Fetch Origin** button to get the latest contents of the repository.
1. In **Current Branch**, create a new branch with a short name (like `add-travel-guidelines`, no spaces or punctuation).
1. Edit files in the `~/Documents/GitHub/about/handbook` folder on your computer.
1. When you've edited the files and saved your changes, GitHub Desktop will show you the changed files in the left sidebar. Confirm that your changes look good by viewing the diffs for each file.
1. In the bottom left `Summary (required)` text field, type your commit message (a one-line description of the change) and a longer `Description` below.
1. Press the **Commit to add-travel-guidelines** button (where `add-travel-guidelines` is the branch name you chose earlier).
1. Press the **Publish branch** button.
1. Press the **Create Pull Request** button.
1. On the pull request page in your web browser, select reviewers and wait for reviews/approvals, then merge to make the changes live.

## Adding images

Pictures, images, and graphics must be uploaded to Google Cloud Storage to be added to a handbook or documentation page. See the [Technical Writing page](product/technical_writing/index.md#uploading-graphics) for instructions.

## Uploading large files

If you want to upload a large file (such as a large image, video, or audio recording) and make it available in the handbook, upload the file to Google Drive and then get a shareable link to the file on Google Drive. Add that link to the handbook. Don't add large files to the handbook repository itself (because Git is not a good way to store large non-text files).

## Using relative paths to link handbook pages

When adding a link to another handbook page, it is best practise to use relative paths. A relative path refers to a location that is relative to a current directory. You can take a look at this video of Jean explaining relative paths and how they work.

<iframe src="https://drive.google.com/file/d/1V84J62tCZuqq8BZKCdq9pJMT9bVb5rmY/preview" width="640" height="480" allow="autoplay"></iframe>

You can also watch [it in Zoom](https://sourcegraph.zoom.us/rec/play/WCRDO_j9x4xw50xsjzBCWKIrL7eoAGBmDDOj7rdjkCIiDpRJ43rArVqrUy1tt4ybpg6fG9FEE0Flv49c.VqDasC2HEHZwRvFv?continueMode=true&_x_zm_rtaid=d0smscs5STuq8vNmHv40bg.1626856634998.9c37f9d9e5d2185652ba07f389dddf2d&_x_zm_rhtaid=329) with audio transcript.

To sum up, the path described the location of the file, naming every directory before the file (called .md). Relative paths are a way of indicating where the file is. The program that reads the relative paths interprets links from where it is at the moment, so we need to make sure to indicate if the directory is different to the one we are at the moment. 

Example:
If we are linking the Buddy program handbook page (handbook/people-ops/onboarding/buddy-program.md) to the Onboarding for hiring managers page (handbook/people-ops/onboarding/onboarding-for-hiring-managers.md) we will only need to say **buddy-program.md** because they share the same directory.
However, if we want to link the Buddy program handbook page to Engineering onboarding page (handbook/engineering/onboarding.md) we would need to use ../ to go back in the directory and then indicate the correct path: **../../engineering/onboarding.md**

**Why do we do this?**
While it is possible to use absolute URLs (ones that include the domain e.g. https://about.sourcegraph.com/handbook) to link to pages, if the domain changes, it is more difficult to update the URLs compared to using relative URLs.

*Remember that if the .md file name changes or the directory changes (because you’ve moved the file to another team’s page, for example) you will need to update the path.*

## Adding redirects

When you change the location of content in the handbook it's important to add a redirect rule so that old URL to the content will automatically take users to the new URL.

To add a redirect rule edit edit the following file: `/_resources/assets/redirects`

Redirect rules follows a simply syntax of: `from-path to-path 308`
E.g. `/handbook/ce/support/ /handbook/support/ 308`

The page that's being redirected _from_ must be deleted, or the build will break. 

## Running a local preview handbook site

> NOTE: This is optional.

See the [handbook section](https://github.com/sourcegraph/about#handbook) in the repository README.

## Handbook feedback

We're constantly iterating on what the best version of our Sourcegraph handbook might look like. Is it easy to use? Do you find what you're looking for? Let us know [here](https://docs.google.com/forms/d/e/1FAIpQLSfb0yU9xmnvK2namuUzUEKbB9IqZlNQF2IWw0OpLsGvBiW2oQ/viewform?usp=sf_link).
