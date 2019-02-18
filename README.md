<!---

TASK LIST:

  * Use cp -rf *.* to copy all of the files and directories in this repository
    to the starter repository for this assignment
  * Change into the directory for the starer repository
  * Update the header (e.g., #) to only give the name of the assignment
  * Update the first paragraph to include the commented-out content
  * Change the link in the # Problems section to point to this lab's starter
  * Create the assignment in the GitHub Classroom, noting the URL
  * Test the assignment by accepting it with your own GitHub account
  * Check to ensure that your GitHub repository is created correctly
  * Share the assignment link with all of the students using email or Slack

PROBLEMS?

  * Contact Gregory M. Kapfhammer by email or Slack
  * Raise an issue in the GitHub repository for this assignment

-->

# cs302-S2019-lab4-solution

Designed for use with [GitHub Classroom](https://classroom.github.com/), this
repository contains the starter for Laboratory 4 in Computer Science 302.
Since the Travis builds for this repository will initially fail (as evidenced
by a red &#x2717; appearing in the commit logs instead of a green &#x2714;),
the programmer is responsible for completing all of the steps needed to satisfy
the requirements for the assignment, thus causing a &#x2714; to instead appear
in the commit logs.

## Introduction

This assignment requires a programmer to implement a static web site using the
HTML and CSS programming languages. Specifically, you will extend and style a
travel photography web site that is an extension of the one in Figure 3.9 of the
textbook. For this laboratory assignment, you will link to a locally stored
image that was downloaded from the Flickr Archive of photographs under a
Creative Commons license. You will also learn how to program in HTML5 using
tags. Next, you will learn how to reference local cascading style sheet (CSS)
files and include an emoji in your web site. As an extension to your previous
laboratory and practical assignments, you will also style the fonts and HTML
elements in your web site with a local CSS file. Then, you will run a web server
to provide local access to the static web site, specifically loading the default
document. Finally, you will continue to practice using the
[HTMLHint](http://htmlhint.com/) static analysis code tool that can check HTML
files for potential errors.

The programmer is also responsible for writing a reflection, stored in the file
`writing/reflection.md`, that responds to the questions in the assignment sheet
and explains the challenges that you faced and the solutions you developed.
Please note that this is also a Markdown file that must adhere to the standards
described in the [Markdown Syntax
Guide](https://guides.github.com/features/mastering-markdown/). Remember, you
can preview the contents of a comitted Markdown file by clicking on the name of
the file in your GitHub repository. Finally, don't forget that your
`writing/reflection.md` file and the file mentioned in the previous paragraph
should both adhere to the Markdown standards established by the [Markdown
linting tool](https://github.com/markdownlint/markdownlint) and the writing
standards set by the [Proselint tool](http://proselint.com/).

The source code in the `index.html` file must also pass additional tests set by
the [GatorGrader tool](https://github.com/GatorEducator/gatorgrader). GatorGrader
will check to ensure that your main file contains the required header and that,
for instance, it contains the correct number of `time` tags. GatorGrader will
also check elements of your CSS and ensure that you made the required number
of commits to your repository and that your writing contains detailed answers
to the stated questions. More details about the GatorGrader checks are
included later in this document and in the assignment sheet.

When you use the `git commit` command to transfer your source code to your
GitHub repository, [Travis CI](https://travis-ci.com/) will initialize a build
of your assignment, checking to see if it meets all of the requirements. If both
your source code and writing meet all of the established requirements, then you
will see a green &#x2714; in the listing of commits in GitHub. If your
submission does not meet the requirements, a red &#x2717; will appear instead.
The instructor will reduce a programmer's grade for this assignment if the red
&#x2717; appears on the last commit in GitHub immediately before the
assignment's due date.

A carefully formatted assignment sheet for this project provides more details
about the steps that a computer scientist should take to complete this
assignment. You can view this assignment sheet by visiting the listing of
laboratories on the course web site.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com)
and [GitHub Classroom](https://classroom.github.com/). Finally, to learn more
about how to include emojis in an HTML file, please read the documentation for
the [Emoji CSS library](https://afeld.github.io/emoji-css/).

To do well on this assignment, you should also review Chapters 1 through 4 of
the course textbook, paying close attention to Sections 4.1 through 4.7 and
Figures 3.9, 4.3, 4.18, 4.20, and 4.31 and Table 4.9. Please see the course
instructor or one of the teaching assistants or tutors if you have questions
about any of these reading assignments.

## Commands

To get started in using the GatorGrader tool, you can change into the directory
for this assignment and type the command `gradle grade` in your terminal.
Running this command will produce a lot of output that you should carefully
inspect. If the output indicates that GatorGrader judges that there are no
mistakes in the assignment, then this means that your source code and writing
are passing all of the automated baseline checks. However, if the output
indicates that there are mistakes, then you will need to understand what they
are and then try to fix them. Finally, remember that you must run the `gradle
grade` command from the main (or "home base") directory for this assignment
where the `build.gradle` file is located. Then, you can type the command in
the terminal and study the output.

## Checking

In addition to making the checks that were previously mentioned in the
introduction to this document, your final submission must meet the following
requirements.

- src/www/travels.html:
  - Passes the checks performed by the HTML linting tool, reporting `no errors found`
  - Contains exactly one use of a `title` tag with `Share Your Travels` as content
  - Contains exactly one use of an `h1` tag with `Share Your Travels` as content
  - Contains exactly one use of an `h3` tag with `Photograph Reviews` as content
  - Contains exactly one use of an `h3` tag with `Travel Tips` as content
  - Contains at least fifteen uses of an `p` tag with the appropriate content
  - Contains at least five uses of a `time` tag with the appropriate content
  - Contains at least five uses of a `blockquote` tag with the appropriate content
  - Contains at least three uses of a `a href` tag with the appropriate link content
  - Contains exactly one reference to `site.css` in the header of the web site
  - Contains exactly one reference to `emoji.css` in the header of the web site
  - Contains exactly one use of the `ol` and `li` tags
  - Contains exactly one use of the `html` and `head` and `body` tags
  - Contains exactly zero references of the marker used to designate unfinished work

- src/www/css/site.css:
  - Contains exactly two references to `font-family` to style the site's fonts
  - Contains exactly one reference to appropriate rules for styling the border of a `blockquote`

- images/travels_submission.png:
  - The file exists in the correct directory with a screenshot of your final web site

- writing/reflection.md:
  - Passes the checks performed by the Markdown linting tool
  - Passes the checks performed by the Prose linting tool
  - Contains exactly five contiguous paragraphs of formatted text
  - The contiguous paragraphs contain at least 100 words

- GitHub repository:
  - Contains five commits beyond the repository's starting number of commits

The following image gives you an example of the formatting and content that your
final web site should exhibit. Specifically, your web site should display the
provided local image and include five comments that feature a bold-faced label
and a descriptive emoji. Your web site should also feature a CSS file that
applies all of the styles that you see in the image at the following link.
Please note that you should open this image in a new browser tab so that you can
closely inspect it for the required features.

[Travel Web Site Example](images/travels_example.jpg)

## Updates

If the course instructor updates the provided material for this assignment and
you would like to receive these updates, then you can type this command in the
main directory for this assignment:

```
git remote add download git@github.com:Allegheny-Computer-Science-302-S2019/cs302-S2019-lab4-starter.git
```

You should only need to type this command once; typing the command additional
times may yield an error message but will not negatively influence the state of
your repository. Now, you are ready to download the updates provided by the
course instructor by typing:

```
git pull download master
```

This second command can be run whenever the course instructor needs to provide
you with new source code for this assignment. However, please note that, if you
have edited the files that the course instructor updated, running the previous
command may lead to Git merge conflicts. If this happens, you may need to
manually resolve them with the help of the instructor or a teaching assistant.

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository, and the course instructor enables Travis for it. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub.

## Requirements

The GatorGrader software that supports the checking of this assignment was
developed for the following software and versions:

- Gradle 4.6
- Java 1.8.0
- MDL 0.4.0
- Proselint 0.8.0
- Python 3.6

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 302 Lab 5
Starter](https://github.com/Allegheny-Computer-Science-302-S2019/cs302-S2019-lab4-starter)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. If you have found a problem with the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) and the way that it checks you
assignment, then you can follow the aforementioned steps to create an issue in
its repository. To ensure that your issue is properly resolved, please provide
as many details as is possible about the problem that you experienced. If you
discover a problem with the laboratory assignment sheet, then please raise an
issue in the
[cs302-S2019-sheets](https://github.com/Allegheny-Computer-Science-302-S2019/cs302-S2019-sheets)
repository and mention this assignment.

Students who find, and use the appropriate GitHub issue tracker to correctly
document, a mistake in any aspect of this laboratory assignment will receive
free laptop stickers and extra credit towards their grade for it.

## Assistance

If you are having trouble completing any part of this project, then please talk
with either the course instructor or a teaching assistant during the laboratory
session. Alternatively, you may ask questions in the Slack team for this
course. Finally, you can schedule a meeting during the course instructor's
office hours.
