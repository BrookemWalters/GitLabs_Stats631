Day 3 - RStudio and R
================

In this repository/directory you should see one item:

- `README.md` - this document.
- `activity01-slr.Rmd`

This activity will hopefully serve as a re-introduction to foundational
R programming processes and the statistical modeling method called
*simple linear regression*. Note that I use the `{tidyverse}` R package
when teaching as I believe this to be a consistent framework that aligns
with how I (and other data professionals) think. You are welcome to use
base R and our text, *ISL*, provides examples using base R and some
different packages (i.e., `{MASS}` and `{ISLR2}`). I will do my best to
support you if you choose to use base R, but my help might be more
higher-level than being able to help you with specific functions.

<!--
## Task 1: Set up Git in RStudio

We will be alternating between GitHub and RStudio throughout this activity.
If you are fortunate enough to have multiple monitors/screens to be working on, I strongly recommend that you keep this page isolated on one screen so you can easily view these directions.
If you only have one screen, it might be helpful to move this tab/window to one half of your screen and then have another browser open on the other half of your screen.

If you have the resources, I find having access to a second monitor/screen to be extremely beneficial when doing work at home.
GVSU's [Surplus Store](https://www.gvsusurplusstore.com/) sometimes has relatively inexpensive monitors - I got a couple for some of my research assistants a couple of years ago for $25 per monitor.
When I looked at their website while creating this activity, it did not appear that they had any in stock.
However, you can always call or stop by to see if the have a new stock in.
I am not sure how up-to-date their site is.

1. Verify that you are in your copy of this activity repo.
  The top of your screen should display `<username>/activity01-course-tools`, where `<username>` is your GitHub username.
2. Open a new browser tab and login to GVSU's [RStudio Workbench](https://rstudio.gvsu.edu/) using your GVSU username and password.
  After you login, verify that you are in an RStudio session and not the RStudio Workbench Sessions/Project screen.

There are a couple of ways to configure Git in RStudio, but we will use `{usethis}`.
Note that when you see something like `{thing}` in my documents, I mean, "the R package called `thing`".
We will use the `edit_git_config` function from `{usethis}`.
Throughout the semester, I will shorten this to be `usethis::edit_git_config` or, "from the R package `usethis`, use the function `edit_git_config`" (in general, `package::function`).

3. In your **Console** pane (this should be either the left-hand pane or the bottom left-hand pane), type the following and press Enter/Return:
  
  
  ```r
  usethis::edit_git_config()
  ```
  
  A file should open in a pane above your **Console** that is called `.gitconfig`.
  In this file, copy-and-paste the information provided below (replacing anything that is currently in this file).
  Then, update it with your preferred name (or pseudonym) and email address (can be any email, but it would probably be helpful to use the same one that you used to signup for GitHub with to avoid any confusion).
  Remember, this information will be publicly available to anyone that happens upon your repo.
  
  ```
  [user]
    name = "preferred_name"
    email = "user@subdomain.domain"
  [credential]
    helper = cache --timeout=10000000
  ```

Note that in the information above, we are also instructing RStudio to remember your GitHub credentials for 10,000,000 seconds (or roughly 16 weeks) - the `[credential]` portion.
RStudio is not remembering your credentials, yet, but we will resolve this shortly.

4. Click on the <img src="../README-img/save-icon.png" alt="save" width = "20"/> icon and you can close this `.gitconfig` file.

## Task 2: Connect RStudio and GitHub

Now that you have Git set up within RStudio, we can enable RStudio and GitHub to communicate.
To do this, we will need your GitHub username and a Personal Access Token (PAT).
PATs are designed to be more secure than your password when communicating between your computer session and GitHub.
Conveniently, `{usethis}` has a function for this!

1. To create a PAT, type the following in your **Console** and press Enter/Return:
  
  
  ```r
  usethis::create_github_token()
  ```

2. You will be directed to a "New personal access token" page on GitHub in your browser.
  Since I work on multiple machines (i.e., my personal laptop, my work laptop, my personal desktop, and the RStudio Workbench), I like to provide a unique name for each PAT.
  For example, in the **Note** text field, I called this token "GVSU RStudio Workbench".
  Most of the other options you will accept the default selections.
  However, you might want to change the **Expiration** date.
  A suggestion is to have this PAT expire at the end of this semester (i.e., Apr 29, 2023).
  After choosing a PAT expiration, scroll down and click on the green **Generate Token** button.
3. After clicking on **Generate Token**, you will be taken to a "Personal access tokens" page that has a seemingly random string presented to you beginning with `ghp_`. 
  Keep this page open for a bit (I will tell you when it is safe to close it), as once you close this page you will never be able to view this PAT again!
  I recommend that you store this PAT somewhere safe (e.g., a password manager tool).
  If you do lose this PAT, you can go through this process again to create a new one.
4. Now we need to specify in RStudio that you have a GitHub PAT so that RStudio can connect to your GitHub account.
  Back in your RStudio **Console**, type the following and press Enter/Return after each line:
    
  
  ```r
  gitcreds::gitcreds_set()
  ```

5. In your **Console** you will be asked to `? Enter password or token:`
  Copy-and-paste your PAT here (not your GitHub password) and press Enter/Return.
  You should see a message similar to:

  ```
  -> Adding new credentials...
  -> Removing credentials from cache...
  -> Done.
  ```

Note that anytime RStudio asks for your GitHub username and password, you need to provide your GitHub username and PAT.
-->

## Task 1: Clone GitHub repo

You connected RStudio and GitHub for Day 2 of this activity. If you are
experiencing issues, get a hold of me or verify that you have
succesfully set up RStudio and GitHub to communicate by redoing [this
preparation](https://github.com/gvsu-sta518/preparation02).

Now that RStudio and GitHub are communicating, we can clone your repo!
In GitHub language, *cloning* means to make a copy of your GitHub repo
on your local computer (i.e., your RStudio/RStudio Workbench session).

![check-in](README-img/noun-magnifying-glass.png) **Check in**

Answer each of these questions:

- What does *forking* in GitHub mean? Hint, it is not the prank you
  might have done in high school where you stuck a bunch of diningware
  forks into someone’s front yard.
- How do *forking* and *cloning* differ?

Now, follow these directions to clone your GitHub repo:

1.  In RStudio, click on the
    <img src="../README-img/rproj-icon.png" alt="RStudio Project" width = "20"/>
    icon (the icon below the Edit drop-down menu).
2.  Click on **Version Control** on the *New Project Wizard* pop-up.
3.  Click on **Git** and you should be on a “Clone Git Repository” page.
4.  Back to your `activity01-course-tools` GitHub repo (you might need
    to go back a page), click on the green **Code** button near the top
    of the page.
5.  Verify that **HTTPS** is underlined in orange/red on the drop-down
    menu, then copy the URL provided.
6.  Back in RStudio, paste the URL in the “Repository URL” text field.
7.  The “Project directory name” text field should have automatically
    populated with `activity01-course-tools`. If yours did not, click
    into this box and press Ctrl/Cmd (this is usually an issue on Macs);
8.  In the “Create project as subdirectory of” field, click on
    **Browse…**. Create a **New Folder** called “STA 631”, then within
    this folder, create a **New Folder** called “Activities”, think
    click **Choose**. Note that I am forcing you to use my opinionated
    file system management style.
9.  Click on **Create Project**.

Your screen should refresh and the **Files** pane should say that you
are currently in your `activity01-course-tools` folder that currently
has the same files and folders as your GitHub repo. If you are asked for
your GitHub credentials, provide your GitHub username and your PAT (not
your password).

## Task 5: Create, Edit, Commit, and Push

Before we wrap-up, we will create a new file (well, open a new-to-you
file) and see how to commit these changes and view the commit history
using RStudio’s graphical user interface.

1.  In the **Files** pane in RStudio (lower right-hand pane), navigate
    to within the `day03-rstudio-r` folder and click on to open the
    Rmarkdown file named `activity01-day03-slr.Rmd`.
2.  Follow the directions in the **Introduction** section, then return
    to these steps to finish the process of committing and pushing to
    GitHub.
3.  In the **Git** pane (upper right-hand pane), check the box next to
    **all** items listed (under the “Staged” column) and click on
    <img src="../README-img/commit-icon.png" alt="commit" width = "20"/>
    **Commit**.
4.  In the pop-up, provide an informative commit message, like
    `Adding some calculations`, then click on **Commit**.
5.  In this same pop-up, switch from **Changes** to **History**
    (upper-left corner). Reflect on how this way of looking through your
    commit history compares to GitHub. Feel free to add more to your R
    script, save, and commit.
6.  To update GitHub with these changes, in the **Git** pane of RStudio
    click on
    <img src="../README-img/push-icon.png" alt="push" width = "20"/>
    **Push**. When/if asked for your GitHub credentials, provide your
    GitHub username and GitHub PAT (not your password). This should,
    hopefully, be the last time you need your GitHub PAT, but I again
    encourage you to keep this in a secure place.
7.  Go back to your `activity01-course-tools` GitHub repo and verify
    that your `activity01-day03-slr.Rmd` AND `activity01-day03-slr.md`
    files are here (you knitted your document, correct?)

**You can now focus on the Rmarkdown document for the rest of today’s
activity.**

## What is next?

Now our workflow is:

![Blackboard icon to fork icon to clone icon to edit icon to commit icon
to push icon](../README-img/updated-workflow.svg)

Or in words:

1.  I will post a link to an activity repo on Blackboard,
2.  You will make your own copy of (fork) this repo,
3.  You will create an RStudio Project and Clone this repo,
4.  You will edit and work on the activity,
5.  You will commit your changes, and
6.  You will push your changes back to GitHub.

Next week we will expand our knowledge of Simple Linear Regression
models.
