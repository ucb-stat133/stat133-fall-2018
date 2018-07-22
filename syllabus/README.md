# Syllabus, Stat 133

- __Notes__:
    + Tentative calendar (weekly topics), subject to changes depending on 
    the pace of the course.
    + Notes (:file_folder:) involves material discussed in class.
    + Reading (:book:) involves material that expands lecture topics, as well as coding examples that you should practice on your own.
    + Misc (:newspaper:) is supporting material that is worth taking a look at.


-----


## 0. Course Introduction

- :card_index: __Dates__: Aug 22-24
- :paperclip: __Topics__: Welcome to Stat 133. We begin with the usual review of the course policies/logistics, expectations, topics in a nutshell, etc. Then, we move on with an unconventional introduction to _computing with data_ using one of my favorite metaphores "Data Analysis is a lot like Cooking".
- :file_folder: __Notes__:
    + [Welcome to Stat 133](../slides/00-welcome.pdf) (slides)
    + [Data Analysis is a lot like cooking](../slides/01-dac-cooking.pdf) (slides)
- :book: __Reading__:
    + [Course policies](policies.md)
    + [Piazza etiquette](piazza.md)
    + [FAQs](faqs.md)
- :microscope: __Lab__: No lab
- :newspaper: __Misc__:
    + [What is Data Science?](../papers/what-is-data-science.pdf)
- :speaker: __To Do__: 
    + Install [__R__](https://cran.cnr.berkeley.edu/) 
    + Install [RStudio](https://www.rstudio.com/products/rstudio/download/#download) Desktop (open source version, free)


-----


## 1. The Big Picture and R Survival Skills

- :card_index: __Dates__: Aug 27-31
- :paperclip: __Topics__: First things first. At the conceptual level we'll discuss how data analysis projects usually start with a Research Question. Also, we'll describe how Data can actually be seen from a triangular perspective (i.e. my "3 Views of Data"). At the practical level, you'll begin learning basic survival skills for R, followed by an overall review of the RStudio workspace. Then we move on to discuss basic data types and their implementation in R around vectors and other data structures. 
- :file_folder: __Notes__:
    + [The Starting Point: Research Questions](../slides/02-research-question.pdf) (slides)
    + [The Three Views of Data](../slides/03-data perspectives.pdf) (slides)
    + Be the Boss of your Data (talk and chalk)
    + [Data Types and Vectors](../slides/04-R-vector-types.pdf) (slides)
- :book: __Reading__:
    + [First contact with R](../tutorials/01-intro-to-R.md) (tutorial)
    + [Intro to Rmd files](../tutorials/02-intro-to-Rmd-files.md) (tutorial)
- :microscope: __Lab__:
    + [Getting started with R and RStudio](../labs/lab01-R-basics.md)
- :newspaper: __Misc__:
    + [Introduction to R Markdown](http://rmarkdown.rstudio.com/lesson-1.html) (by RStudio)
- :bulb: __Cheat sheet__: 
    + [RStudio cheat sheet](../cheatsheets/rstudio-IDE-cheatsheet.pdf)
    + [R markdown cheat sheet](../cheatsheets/rmarkdown-cheatsheet-2.0.pdf)
- :dart: __WARM-UP 1__:
    + [Markdown practice](../hws/warmup01-markdown.pdf) (due Sep-04, open till Sep-18)


-----


## 2. More Data Structures: Arrays, Lists, and Dataframes

- :card_index: __Dates__: Sep 03-07 _(Holiday Sep-03)_
- :paperclip: __Topics__: In this week you'll keep learning more about R data structures like arrays and lists. More specifically, we'll focus on fundamental concepts like atomicity, vectorization, recycling, and subsetting. And given that we are studying vectors and its cousins, we'll briefly review the traditional _base_ graphics approach that is based on R vectors.
- :file_folder: __Notes__:
    + [Arrays and Factors](../slides/05-arrays-factors.pdf) (slides)
    + [Lists](../slides/06-lists.pdf) (slides)
    + [Data Frames](../slides/07-data-frames.pdf) (slides)
    + [Base Graphics I](../slides/08a-base-graphics1.pdf) (slides)
    + [Base Graphics II](../slides/08b-base-graphics2.pdf) (slides)
- :book: __Reading__:
    + [Intro to vectors](../tutorials/03-intro-to-vectors.md) (tutorial)
- :microscope: __Lab__:
    + [Getting started with vectors and factors](../labs/lab02-vector-basics.md)
- :newspaper: __Misc__:
    + [chapter 20: Vectors](http://r4ds.had.co.nz/vectors.html) (_R for Data Science_ by Grolemund and Wickham)
- :bulb: __Cheat sheet__: 
    + [Base R](../cheatsheets/base-r-cheatsheet.pdf)
- :dart: __WARM-UP 2__:
    + [Vectors and Factors](../hws/warmup02-vector-basics.pdf) (due Sep-11, open till Sep-18)


-----


## 3. Housekeeping: Filesystem and Bash Commands

- :card_index: __Dates__: Sep 10-14
- :paperclip: __Topics__: Data Analysis Projects (DAPs) are made of files and directories. Therefore, we need to review some fundamental concepts such as the file-system, the command line interface, and some basic shell commands. At the practical level, you will have the chance to practice some data manipulation operations on data frames.
- :file_folder: __Notes__:
    + [Filesystem Basics](../slides/09-filesystem-basics.pdf) (slides)
    + [Shell Basics](../slides/10-shell-basics.pdf) (slides)
    + [Working with files](../slides/11-working-with-files.pdf) (slides)
- :book: __Reading__:
    + [Linux Tutorial](https://ryanstutorials.net/linuxtutorial/) lessons 1-5 (by Ryan Chadwick)
    + [The Unix Shell](http://swcarpentry.github.io/shell-novice/) lessons 1-3 (by Software Carpentry)
- :microscope: __Lab__:
    + [Command Line Basics](../labs/lab03-command-line-basics.md)
- :newspaper: __Misc__:
    + [Linux Command Line tutorial](https://www.guru99.com/terminal-file-manager.html) (by Guru99)
- :bulb: __Cheat sheet__:
    + [command line cheat sheet](../cheatsheets/command-line-cheatsheet.pdf)
- :dart: __WARM-UP 3__:
    + [Data Frame Basics](../hws/warmup03-data-frame-basics.pdf) (due Sep-18)


-----


## 4. Housekeeping: Version Control with Git and GitHub

- :card_index: __Dates__: Sep 17-21
- :paperclip: __Topics__: We continue talking about filestructure topics, and we introduce basic notions of version control systems (VCS) using Git, and the companion hosting platform GitHub.
On the Data side, we begin our discussion about Tables: the most common form in which data is stored, handled, and manipulated. Consequently, we need to talk about the typical storage formats of tabular data, and the relationship between tables and R data frames.
- :file_folder: __Notes__:
    + [Git Basics](../slides/12-git-basics.pdf) (slides)
    + [Git Workflow](../slides/13-git-workflow.pdf) (slides)
    + [Data Tables](../slides/14-data-tables.pdf) (slides)
    + [Importing Tables in R](../slides/15-importing-tables.pdf) (slides)
- :book: __Reading__:
    + Read sections 4 to 9 in Part I [Installation](http://happygitwithr.com/installation-pain.html) (_Happy Git and GitHub for the useR_ by Jenny Bryan et al.)
    + [Basic manipulation of Data Frames](../slides/14-data-frame-basics.pdf) (slides)
- :microscope: __Lab__:
    + Work on episodes 2 to 7 of the tutorial [Version Control with Git](http://swcarpentry.github.io/git-novice/) (by Software Carpentry)
    + [Getting started with data frames](../labs/lab04-data-frame-basics.md)
- :newspaper: __Misc__:
    + [Data Import](http://r4ds.had.co.nz/data-import.html) (_R for Data Science_ by Grolemund and Wickham)
    + [Organizing data in spreadsheets](http://kbroman.org/dataorg/) (by Karl Broman)
- :bulb: __Cheat sheet__:
    + [Data import cheat sheet](../cheatsheets/data-import-cheatsheet.pdf)
    + [git cheat sheet](../cheatsheets/git-cheatsheet.pdf)
- :dart: __WARM-UP 4__:
    + [Data Frame Basics](../hws/warmup04-importing-tables.pdf) (due Sep-25)


-----


## 5. Transforming and Visualizing Tabular Data

- :card_index: __Dates__: Sep 24-28
- :paperclip: __Topics__: Because data tables are so uniquituos, it's important that you learn how to manipulate them via R data frames in a "modern" and syntactic way following the _data plying_ framework provided by the package `"dplyr"`. Likewise, we begin reviewing the visualization paradigm of `"ggplot2"` which is based on data frames.
- :file_folder: __Notes__:
    + ["dplyr" tutorial slides](../slides/17-dplyr-tutorial.pdf) (by Hadley Wickham)
    + [Grammar of Graphics framework](../slides/18-grammar-graphics.pdf) (slides)
- :book: __Reading__:
    + ["ggplot2" lecture](../slides/19-ggplot-lecture.pdf) (by Karthik Ram)
- :microscope: __Lab__:
    + [GitHub Classroom](../labs/lab03-github-classroom.pdf)
    + [Getting started with dplyr and ggplot2](../labs/lab05-dplyr-ggplot-basics.md)
- :newspaper: __Misc__:
    + [tibbles vignette](https://cran.r-project.org/web/packages/tibble/vignettes/tibble.html)
    + [Introduction to dplyr](https://cran.r-project.org/web/packages/dplyr/vignettes/dplyr.html) (by Hadley Wickham)
- :bulb: __Cheat sheet__:
    + [Data transformation cheat sheet](../cheatsheets/data-transformation-cheatsheet.pdf)
    + [Data visualization with ggplot2](../cheatsheets/ggplot2-cheatsheet-2.1.pdf)
- :dart: __WORK-OUT 1__:
    + [Data Wrangling and visualization](../hws/workout01-shot-charts.pdf) (due Oct-05)


-----


## 6. More Wrangling, Pipes, and Exporting Outputs

- :card_index: __Dates__: Oct 01-05
- :paperclip: __Topics__: We continue reviewing more aspects of `"dplyr"` and the famous pipe operator. 
- :file_folder: __Notes__:
    + [Pipes with `"dplyr"`](../tutorials/05-dplyr-pipes.md) (tutorial)
    + [Shell input/output redirection](../tutorials/07-shell-redirections.md) (tutorial)
    + [Shell filters](../tutorials/08-shell-filters.md) (tutorial)
- :book: __Reading__:
    + [Pipes](http://r4ds.had.co.nz/pipes.html) (_R for Data Science_ by Grolemund and Wickham)
- :microscope: __Lab__:
    + [More data wrangling, and exporting outputs](../labs/lab06-more-data-wrangling.md)
- :newspaper: __Misc__:
    + [Tidy Data](../papers/tidy-data-wickham) (by Hadley Wickham)
- :bulb: __Cheat sheet__:
    + [Data transformation cheat sheet](../cheatsheets/data-transformation-cheatsheet.pdf)
    + [Command line cheat sheet](../cheatsheets/command-line-cheatsheet.pdf)
- :mortar_board: __MIDTERM 1__: Friday Oct-05



-----


## 7. Transition to Programming Basics for data analysis (part 1)

- :card_index: __Dates__: Oct 08-12
- :paperclip: __Topics__: You don’t need to be an expert programmer to be a data scientist, but learning more about programming allows you to automate common tasks, and solve new problems with greater ease. We'll discuss how to write basic functions, the notion of R expressions, and an introduction to conditionals. 
- :file_folder: __Notes__:
    + [Creating functions](../tutorials/09-creating-functions.md) (tutorial)
    + [Introduction to functions](../tutorials/10-intro-to-functions.md) (tutorial)
    + [Introduction to R expressions and conditionals](../tutorials/11-intro-to-expressions-conditionals.md) (tutorial)
- :microscope: __Lab__:
    + [Getting started with functions and conditionals](../labs/lab07-simple-functions.md)
- :newspaper: __Misc__: 
    + [chapter 19: Functions](http://r4ds.had.co.nz/functions.html) (_R for Data Science_ by Grolemund and Wickham)
- :dart: __WARM-UP 5__:
    + [Function Basics](../hws/warmup05-function-basics.pdf) (due Oct-16)


-----


## 8. Programming Basics for data analysis (part 2)

- :card_index: __Dates__: Oct 15-19
- :paperclip: __Topics__: In addition to writing functions to reduce duplication in your code, you also need to learn about iteration, which helps you when you need to do the same operation several times. Namely, we review control flow structures such as `for` loops, `while` loops, `repeat` loops, and the `apply` family functions.
- :file_folder: __Notes__:
    + [Introduction to loops](../tutorials/12-intro-to-loops.md) (tutorial)
    + [More about functions](../tutorials/13-more-functions.md) (tutorial)
    + [Functions](http://adv-r.had.co.nz/Functions.html) (_Advanced R_ by H. Wickham)
- :microscope: __Lab__: 
    + [Getting started with loops](../labs/lab08-simple-loops.md)
- :newspaper: __Misc__:
    + [chapter 21: Iteration](http://r4ds.had.co.nz/iteration.html) (_R for Data Science_ by Grolemund and Wickham)
- :dart: __WARM-UP 6__:
    + [Pipelines and Programming Basics](../hws/warmup06-programming-basics.pdf) (due Oct-23)


-----
