Lab 3: Command Line Basics and Data Importing
================
Gaston Sanchez

> ### Learning Objectives
> 
>   - Practicing with the command line
>   - Navigating the filesystem and managing files
>   - Practice basic manipulation of data files
>   - Importing Data Tables in R
>   - Default reading-table functions

### General Instructions

  - Write your descriptions, explanations, and code in an `Rmd` (R
    markdown) file.
  - Name this file as `lab03-first-last.Rmd`, where `first` and `last`
    are your first and last names (e.g. `lab03-gaston-sanchez.Rmd`).
  - Knit your `Rmd` file as an html document (default option).
  - Submit your `Rmd` and `html` files to bCourses, in the corresponding
    lab assignment.
  - Due date displayed in the syllabus (see github repo).

-----

## Basic Bash shell commands

The first part of the lab involves navigating the file system and
manipulating files (and directories) with the following basic shell
commands:

  - `pwd`: print working directory
  - `ls`: list files and directories
  - `cd`: change directory (move to another directory)
  - `mkdir`: create a new directory
  - `touch`: create a new (empty) file
  - `cp`: copy file(s)
  - `mv`: rename file(s)
  - `rm`: delete file(s)

If you are using git-bash (i.e. your OS is Windows) you don’t have the
`man` command to see the manual documentation of other commands. In this
case you can check the *man* pages online:

<http://man7.org/linux/man-pages/index.html>

### Your turn

Write your bash commands inside a chunk that is NOT evaluated. One way
to do this is to add the option `eval = FALSE` inside the curly braces
of the chunk (see image below)

![](lab03-images/unevaluated-chunk.png)

  - Open (or launch) the command line
  - Use `mkdir` to create a new directory `stat133-lab03`
  - Change directory to `stat133-lab03`
  - Use the command `curl` to download the following text file:

<!-- end list -->

``` bash
# the option is the letter O (Not the number 0)
curl -O http://textfiles.com/food/bread.txt
```

  - Use the command `ls` to list the contents in your current directory
  - Use the command `curl` to download these other text files:
      - <http://textfiles.com/food/btaco.txt>
      - <http://textfiles.com/food/1st_aid.txt>
      - <http://textfiles.com/food/beesherb.txt>
      - <http://textfiles.com/food/bakebred.txt>
  - Use the command `curl` to download the following csv
        files:
      - <http://archive.ics.uci.edu/ml/machine-learning-databases/forest-fires/forestfires.csv>
      - <http://web.pdx.edu/~gerbing/data/cars.csv>
      - <http://web.pdx.edu/~gerbing/data/color.csv>
      - <http://web.pdx.edu/~gerbing/data/snow.csv>
      - <http://web.pdx.edu/~gerbing/data/mid1.csv>
      - <http://web.pdx.edu/~gerbing/data/mid2.csv>
      - <http://web.pdx.edu/~gerbing/data/minutes1.csv>
      - <http://web.pdx.edu/~gerbing/data/minutes2.csv>
  - Now try `ls -l` to list the contents in your current directory in
    long format
  - Look at the `man` documentation of `ls` to find out how to list the
    contents in reverse order
  - How would you list the contents in long format arranged by time?
  - Find out how to use the wildcard `*` to move list all the files with
    extension `.txt`
  - Use the wildcard `*` to move list all the files with extension
    `.csv` in reverse order
  - Find out how to use the wilcard `?` to list `.csv` files with names
    made of 4 characters (e.g. `mid1.csv`, `snow.csv`)
  - Inside `stat133-lab03` create a directory `data`
  - Change directory to `data`
  - Create a directory `txt-files`
  - Create a directory `csv-files`
  - Use the command `mv` to move the `bread.txt` file to the folder
    `txt-files`
  - Use the wildcard `*` to move all the text files to the directory
    `txt-files`
  - Use the wildcard `*` to move all the `.csv` files to the directory
    `csv-files`
  - Go back to the parent directory `stat133-lab03`
  - Create a directory `copies`
  - Use the command `cp` to copy the `bread.txt` file (the one inside
    the folder `txt-files`) to the `copies` directory
  - Use the wildcard `*` to copy all the `.txt` files in the directory
    `copies`
  - Use the wildcard `*` to copy all the `.csv` files in the directory
    `copies`
  - Change to the directory `copies`
  - Use the command `mv` to rename the file `bread.txt` as
    `bread-recipe.txt`
  - Rename the file `Fisher.csv` as `iris.csv`
  - Rename the file `btaco.txt` as `breakfast-taco.txt`
  - Change to the parent directory (i.e. `stat133-lab03`)
  - Rename the directory `copies` as `copy-files`
  - Find out how to use the `rm` command to delete the `.csv` files that
    are in `copy-files`
  - Find out how to use the `rm` command to delete the directory
    `copy-files`
  - List the contents of the directory `txt-files` displaying the
    results in reverse (alphabetical) order

### Optional challenge

If you are already familiar with the basic bash commands to navigate the
filesystem (or if you want to expand your R skills), use the R functions
to manipulate files and directories to perform the exact same tasks from
within R. See `?files` for more information.

  - `getwd()`
  - `setwd()`
  - `download.file()`
  - `dir.create()`
  - `list.files()`
  - `list.dirs()`
  - `file.create()`
  - `file.copy()`
  - `file.rename()`
  - `file.remove()`

-----

## Abalone Data Set

The second part of the lab involves importing the **Abalone Data Set**
that is part of the [UCI Machine Learning
Repository](http://archive.ics.uci.edu/ml/datasets/Abalone)

The location of the data file
is:

<http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.data>

The location of the data dictionary (description of the data)
is:

<http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.names>

Look at both the dataset file, and the file with its description, and
answer the following questions:

  - What’s the character delimiter?
  - Is there a row for column names?
  - Are there any missing values? If so, how are they codified?
  - What is the data type of each column?

One basic way to read this file in R is by passing the url location of
the file directly to any of the `read.table()`
functions:

``` r
url <- "http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.data"
abalone <- read.table(url, sep = ",")
```

### Getting a Local Copy of the Data

My suggestion when reading datasets from the Web, is to always try to
get a local copy of the data file in your machine (as long as you have
enough free space to save it in your computer). To do this, you can use
the function `download.file()` and specify the url address, and the name
of the file that will be created in your computer. For instance, to save
the abalone data file in **your working directory**, type the following
commands directly on the R console:

``` r
# do NOT include this code in your Rmd file
# download copy to your working directory
origin <- 'http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.data'
destination <- 'abalone.data'
download.file(origin, destination)
```

## Some Bash Commands

Before describing some of the reading-table functions in R, let’s
practice some basic bash commands to inspect the downloaded data file.
Include the commands in your Rmd file inside an unevaluated code chunk.

### Your turn

  - Use the `file` command to know what type of file is `abalone.data`.

  - Use the *word count* command `wc` to obtain information about: 1)
    newline count, 2) word count, and 3) byte count, of the
    `abalone.data` file.

  - See the `man` documentation of `wc` and learn what option you should
    use to otabin only the number of lines in `abalone.data`.

  - Use `head` to take a peek at the first lines (10 lines by default)
    of `abalone.data`

  - See the `man` documentation of `head` and learn what option you
    should use to display only the first 5 files in `abalone.data`.

  - Use `tail` to take a peek at the last lines (10 lines by default) of
    `abalone.data`

  - See the `man` documentation of `tail` and learn what option you
    should use to display only the last 3 files in `abalone.data`.

  - Use the `less` command to look at the contents of `abalone.data`
    (this command opens a *paginator* so you can move up and down the
    contents of the file). Press the key `q` to exit the paginator.

-----

## Basic Importing

Now that you have a local copy of the dataset, you can read it in R with
`read.table()` like so:

``` r
# reading data from your working directory
abalone <- read.table("abalone.data", sep = ",")
```

Once you read a data table, you may want to start looking at its
contents, usually taking a peek at a few rows. This can be done with
`head()` and/or with `tail()`:

``` r
# take a peek of first rows
head(abalone)

# take a peek of last rows
tail(abalone)
```

Likewsie, you may also want to examine how R has decided to take care of
the storage details (what data type is used for each column?). Use the
function `str()` to check the structure of the data frame:

``` r
# check data frame's structure
str(abalone, vec.len = 1)
```

### Detailed information about the columns

So far we have been able to read the data file in R. But we are missing
a few things. First, we don’t have names for the columns. Second, it
would be nice if we could specify the data types of each column instead
of letting R guess how to handle each data type.

Look at the data description (see “Attribute information”) in the
following
link:

<http://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.names>

According to the description of the Abalone data set, we could assign
the following data types to each of the columns as:

| Name           | Data Type  |
| -------------- | ---------- |
| Sex            | character  |
| Length         | continuous |
| Diameter       | continuous |
| Height         | continuous |
| Whole weight   | continuous |
| Shucked weight | continuous |
| Viscera weight | continuous |
| Shell weight   | continuous |
| Rings          | integer    |

  - Create a vector `column_names` for names of each column. Use the
    names displayed in the section “7. Attributes Information”.

  - Create another vector `column_types` with R data types (e.g.
    `character`, `real`, `integer`). Match the R data types with the
    suggested type in “7. Attributes Information” (nominal =
    `character`, continuous = `real`, integer = `integer`).

  - Optionally, you could also specify a type “factor” for the variable
    `sex` since this is supposed to be in nominal scale (i.e. it is a
    categorical variable). Also note that the variable `rings` is
    supposed to be integers, therefore we can choose an `integer` vector
    for this column.

  - Look at the documentation of the function `read.table()` and try to
    read the `abalone.data` table in R. Find out which arguments you
    need to specify so that you pass your vectors `column_names` and
    `column_types` to `read.table()`. Read in the data as `abalone`, and
    then check its structure with `str()`.

  - Now re-read `abalone.data` with the `read.csv()` function. Name this
    data as `abalone2`, and check its structure with `str()`.

  - How would you read just the first 10 lines in `abalone.data`? Name
    this data as `abalone10`, and check its structure with `str()`.

  - How would you skip the first 10 lines in `abalone.data`, in order to
    read the next 10 lines (lines 11-20)? Name this data as `abalone20`,
    and check its structure with `str()`.

  - Use R functions to compute descriptive statistics, and confirm the
    following statistics. Your output does not have to be in the same
    format of the table below. The important thing is that you begin
    learning how to manipulate columns (or vectors) of a data.frame.

<!-- end list -->

``` 
       Length Diam  Height  Whole  Shucked  Viscera    Shell    Rings
Min    0.075  0.055 0.000   0.002    0.001    0.001    0.002        1
Max    0.815  0.650 1.130   2.826    1.488    0.760    1.005       29
Mean   0.524  0.408 0.140   0.829    0.359    0.181    0.239    9.934
SD     0.120  0.099 0.042   0.490    0.222    0.110    0.139    3.224
```
