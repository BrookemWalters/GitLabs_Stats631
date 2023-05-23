Activity 01 - Course Tools
================

This activity is intended to be completed in over three class sessions,
including outside of class preparation work and three class meetings.

In this repository/directory, you should see six items:

- `README-img` - a folder containing images that I am embedding within
  this `README.md` file. You do not need to do anything with this.
- `.gitignore` - a file that is used to specify what Git can ignore when
  pushing to GitHub. You do not need to do anything with this.
- `README.md` - the document you are currently reading.
- `day01-github-markdown` - a folder that contains items for you to
  complete during the first class meeting.
- `day02-rstudio-rmarkdown` - a folder that contains items for you to
  complete during the second class meeting.
- `day03-rstudio-r` - a folder that contains items for you to complete
  during the third class meeting.

We will explore most of these items over these next class sessions.
Before doing that, you will first make your own copy of this repository.
Note that I will refer to “repositories” as “repos” (or a single
“repository” as a “repo”) for the rest of the semester.

## Day 1

**Do not proceed in this document until you have minimally**:

1.  Completed this short (5-10 minutes) interactive [Markdown
    tutorial](https://commonmark.org/help/tutorial/).
2.  Created a free GitHub account if you do not already have one.

### Task 1: Forking the Repository

Read these directions first, then work through them. In this GitHub repo
(i.e., my repo):

1.  Click on the ![fork](README-img/fork-icon.png) **Fork** icon near
    the upper-right-hand corner. You will be taken to a **Create a new
    fork** screen.
2.  Verify that your GitHub username is selected under **Owner** and
    that the **Repository name** is `activity01-course-tools` with a
    green check mark (this verifies that you do not already have a
    GitHub repository with this name).
3.  You may provide a **Description** if you would like. This is a way
    to provide some additional, more descriptive, meta information
    related to the things you did. I like to provide a brief description
    of what happened.
4.  Verify that **Copy the `main` branch only** is selected.
5.  Click on the green **Create fork** button at the bottom of this
    page.

You should be taken a copy of this repo that is in your GitHub account.
That is, your page title should be `username/activity01-course-tools`,
where `username` is replaced with your GitHub username. Directly below
this, you will see the following message:

> forked from
> [gvsu-sta631/activity01-course-tools](https://github.com/gvsu-sta631/activity01-course-tools)

You will complete the rest of this activity in **your** forked copy of
the `activity01-course-tools` repo.

![check-in](README-img/noun-magnifying-glass.png) **Check in**

Take a moment to reflect on what this process is like compared to other
methods you have used for sharing documents with others. Talk through
these with your group members.

- Can you sketch out a diagram that relates that previous method/process
  to this GitHub method?
- What was easier about this GitHub method?
- What was more difficult about this GitHub method?

### Task 2: Exploring a GitHub Repository

The last time that I taught STA 518 I had students complete this
[Preparation](https://github.com/gvsu-sta518/preparation01) that
includes videos that provide more details on what Git and GitHub are.
You may find this preparation helpful to complete outside of class. Note
that these videos are somewhat old and things in current GitHub are
different. For our work this semester, we will not worry about Branches
or Issues.

When you view repos on github.com, most will have a similar set up.
There are a lot of icons, text, regions, etc. in every repo and it can
be confusing what exactly you need to do. Whenever we will use a new
feature on GitHub, I will provide you with details of what to do and
what is happening. For the time being, you can focus on two regions of
your new repo.

First, if you are currently reading this text that means that you are
viewing the `README.md` file. Folks use this file for various reasons,
but I will use it to describe what is in the repo and provide getting
started directions for how you should interact with it. Here is an
example of information the Posit (formerly RStudio) team provides in
their README files: [`{ggplot2}`
repo](https://github.com/tidyverse/ggplot2#ggplot2) README files take
information written in Markdown (`.md` files) and formats it to look
nice on a webpage.

Second, directly above the displayed `README.md` document is an area
that looks similar to a folder/directory that you would interact with on
your computer. In fact, once we start to work between RStudio and
GitHub, your directory will be identical to your repo! I like to think
of a GitHub repo as a folder system that others can view/copy/edit (with
permission) rather than needing to zip up a folder on my computer and
then email it to another person to work with. Repos can contain multiple
types of files that use various syntax/text and also include subfolders,
sub-subfolders, etc. Read these directions first, then work through
them.

1.  In your `activity01-course-tools` repo folder/directory, locate and
    click into the `day01-github-markdown` subfolder.
2.  In the `day01-github-markdown` subfolder, you will be greeted by a
    new `README.md` file. Do your best to complete the tasks/directions
    provide in this subfolder by **11:59 pm (EST) on Tue, Jan 17**.
3.  In our Teams workspace (linked on Blackboard), find the **General**
    channel and post what was muddiest from these tasks. If someone else
    already posted what you though was muddy, add any clarification to
    their post and give them a “+ 1” 👍. Remember that this space is for
    conversations as well as posting questions. Read through your peers’
    muddy posts and do your best to provide help.

The rest of this `README` document <!--contains--> will contain
tasks/directions for the next class meetings.

## Day 2

**Do not proceed in this document until you have minimally**:

1.  Verified that you can login to GVSU’s [RStudio
    Workbench](https://rstudio.gvsu.edu/). Or (more advanced and I note
    that I may not be able to assist you with problem solving on your
    machine), you have installed R, RStudio, and Git on your computer
    and enabled RStudio and GitHub to communicate. If you choose have R,
    RStudio, and GitHub setup on your personal computer, I recommend
    following the directions from [Dr. Jenny Bryan *et
    al*](https://happygitwithr.com/).
2.  Completed [this
    preparation](https://github.com/gvsu-sta518/preparation02) to
    connect your RStudio Workbench instance and GitHub so they
    communicate with one another. Note that this is a preparation that I
    created for STA 418/518 and am reusing here - the process is the
    same so why create multiple copies of the same document.

### Task 1: Updating your forked GitHub repo

You will need to start reading these directions back at my
`gvsu-sta631/activity01-course-tools` GitHub repo **and** have your
forked `username/activity01-course-tools` GitHub repo handy. I recommend
that you have my repo opened on one half of your screen and your repo
opened on the other half. Read these directions first, then work through
them.

1.  At the top of your `username/activity01-course-tools` repo (above
    the repo contents section), verify that you see a message that looks
    something like:

> This branch is X commits behind gvsu-sta631:main.

2.  Click on the hyperlinked “X commits behind” portion of that message
    to be taken to a **Comparing changes** page.
3.  Verify that your drop-down menu options specify:
    - base repository: username/activity01-course-tools
    - base: main
    - head repository: gvsu-sta631/activity01-course-tools
    - compare: main
4.  Also verify that you have a message directly below this that says:

> ✓ Able to merge. These branches can be automatically merged.

Flag me if you see something different.

5.  Click on the green **Create pull request** button under this
    previous message. Note you can look at the changes that I made, if
    you so desire, by scrolling down. However, this is not necessary.
6.  On the next page, provide a short descriptive message in the “Title”
    box (e.g., “Adding Day 2 materials”). You can also provide a more
    detailed message in the “Leave a comment” box if you choose.
7.  Click on the green **Create pull request** button.
8.  On the next screen which is titled the same thing as what you
    provided in the “Title” box on the previous screen, you will be
    presented with a bunch of information. If you scroll down a little,
    you should see a green check mark with a message that specifies:

> This branch has no conflicts with the base branch

And you can click on the green **Merge pull request**.

9.  You will be provided with with an opportunity to provide another
    meaningful message (or accept the default message). Finally, click
    on the green **Confirm merge** button. You can now work directly
    from your `username/activity01-course-tools` repo.

In summary, what you just did is pulled my changes into your repository.
Git and GitHub refer to this as a “pull request” because you are asking
to pull items into your repo.

### Task 2: Authoring in RStudio

In your `username/activity01-course-tools` repo, go into the
`day02-rstudio-rmarkdown` subfolder and follow the tasks listed in the
`README`. You will follow these directions for today’s activity of
building your own Distill website!

## Day 3

**Do not proceed in this document until you have affirmed these items**:

- What the main uses for each region/pane in RStudio:
  <https://r4ds.had.co.nz/introduction.html#rstudio>.
- What an Rmarkdown file is, how to run code in an Rmarkdown file or
  Console, and how RStudio helps notify you of potential problems in
  your code: <https://r4ds.had.co.nz/workflow-scripts.html> and
  <https://r4ds.had.co.nz/r-markdown.html>.
- What RStudio Projects are, determining where things “live” in RStudio,
  and the benefits of beginning each R session from a “vanilla”
  (sessions that do not retain information from previous sessions):
  <https://r4ds.had.co.nz/workflow-projects.html>.

I think it incredibly **important** that you force RStudio to start from
a clean session everytime that you start it up, that I kindly ask that
you follow the recommendations in [Section
8.1](https://r4ds.had.co.nz/workflow-projects.html#what-is-real) of R
for Data Science by updating your **Global Options**.

![check-in](README-img/noun-magnifying-glass.png) **Check in**

Verify that you can access GVSU’s [RStudio
Workbench](https://rstudio.gvsu.edu/). Then, see if you can affirm each
of these questions:

- I can create an RMarkdown document.
- I can run a simple calculation (e.g., `2 + 2`) in an R Script, an
  RMarkdown document, and the R Console.
- I can load an R package in an R Script, an RMarkdown document, and the
  R Console (e.g., like `{ggplot2}`)
- I can create a simple data visualization using `{ggplot2}` in an R
  Script, an RMarkdown document, and the R Console (e.g., like a
  scatterplot using the
  [`msleep`](https://ggplot2.tidyverse.org/reference/msleep.html)
  dataset).

### Updating your forked GitHub repo again

These are the same directions that you used to update your forked GitHub
for Day 2 - practice, practice, practice.

You will need to start reading these directions back at my
`gvsu-sta631/activity01-course-tools` GitHub repo **and** have your
forked `username/activity01-course-tools` GitHub repo handy. I recommend
that you have my repo opened on one half of your screen and your repo
opened on the other half. Read these directions first, then work through
them.

1.  At the top of your `username/activity01-course-tools` repo (above
    the repo contents section), verify that you see a message that looks
    something like:

> This branch is X commits behind gvsu-sta631:main.

2.  Click on the hyperlinked “X commits behind” portion of that message
    to be taken to a **Comparing changes** page.
3.  Verify that your drop-down menu options specify:
    - base repository: username/activity01-course-tools
    - base: main
    - head repository: gvsu-sta631/activity01-course-tools
    - compare: main
4.  Also verify that you have a message directly below this that says:

> ✓ Able to merge. These branches can be automatically merged.

Flag me if you see something different.

5.  Click on the green **Create pull request** button under this
    previous message. Note you can look at the changes that I made, if
    you so desire, by scrolling down. However, this is not necessary.
6.  On the next page, provide a short descriptive message in the “Title”
    box (e.g., “Adding Day 2 materials”). You can also provide a more
    detailed message in the “Leave a comment” box if you choose.
7.  Click on the green **Create pull request** button.
8.  On the next screen which is titled the same thing as what you
    provided in the “Title” box on the previous screen, you will be
    presented with a bunch of information. If you scroll down a little,
    you should see a green check mark with a message that specifies:

> This branch has no conflicts with the base branch

And you can click on the green **Merge pull request**.

9.  You will be provided with with an opportunity to provide another
    meaningful message (or accept the default message). Finally, click
    on the green **Confirm merge** button. You can now work directly
    from your `username/activity01-course-tools` repo.

In summary, what you just did is pulled my changes into your repository.
Git and GitHub refer to this as a “pull request” because you are asking
to pull items into your repo.

### Task 2: Authoring in RStudio

In your `username/activity01-course-tools` repo, go into the
`day03-rstudio-r` subfolder and follow the tasks listed in the `README`.
You will follow these directions for today’s activity of working through
a simple linear regression analysis.

## Attribution

This document is based on David Keyes’ tutorial at [R for the Rest of
Us](https://rfortherestofus.com/2021/02/how-to-use-git-github-with-r/)
and [Happy Git with R](http://happygitwithr.com/) by Jenny Bryan et al.
