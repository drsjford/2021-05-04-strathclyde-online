# r-lesson.md - 2021-05-04-strathclyde-online

**START THE SLIDES**

-----

## 1. DATA ANALYSIS

-----

## Data Analysis in the Scientific Cycle

- The **CYCLE OF SCIENCE** is often presented as:
  - Formulate a hypothesis
  - Test the hypotheses
  - Gather data
  - Analyse data
  - Update the hypothesis
  - and go round again

- But I'd like to suggest:
  - You **can't formulate a hypothesis without having first made some observations**
  - This scientific cycle has always started - if unacknowledged - with data collection and analysis
    - Darwin and Wallace had to make long journeys and many observations before they formed their hypotheses of descent with selection
  - **In the age of data-intensive research, the focus is very much on open-minded data analysis to formulate hypotheses *as a first step* in the cycle**
    - **It is especially important that your initial exploration is recorded, replicable and systematic**

- With the increasing amount of freely-available public data - especially genome data - you can get started on formulating hypotheses more easily than ever before

-----

## Data-Intensive Research

- You're probably here because you are doing, or maybe aim to do, data-intensive research
  - Science and the humanities are both becoming much more data-driven
  - Researchers who don't identify as "data scientists" are now having to work with large, complex data
- Early-career training may not have prepared everyone equally well for this
  - You may have had courses on basic statistical methods (t-tests, ANOVA), and specific software tools
  - Who has had training in developing a reproducible workflow, or coding a new analysis **ASK FOR HANDS/GET RESPONSES**

- Research workflows are central to systematic, replicable and reproducible research
  - But they're often left out of basic training
- The core skills that help us create these workflows are:
  - Design principles - what data is and how it is best processed
  - Software development methods - how to automate repetitive stuff with a computer 

-----

## Pipelines and Workflows

- We can distinguish between two terms that often get used interchangeably: "pipelines" and "workflows"

- "Pipelines" are a set of instructions - run by your computer - that take a dataset and *pipe* it through some processes, until a result emerges from the end.
- "Workflows" are the processes that researchers follow to investigate a problem
  - A workflow might involve using one or more pipelines
  - But it includes things like exploring your data, forming hypotheses, writing code, and interpreting your results

- In this course, we're concerned with the whole workflow

-----

## Explore, Refine, Produce (ERP)

- One way to think about your workflow is as an "Explore, Refine, Produce (ERP)" cycle.

- In the Explore phase, you process and interrogate your data to identify potential solutions
- In the Refine phase, you narrow down your focus to the most promising approaches
- The Produce phase is really a companion to the Explore and Refine phases
  - you should always be recording your work and preparing it for future consumption either by yourself or others

- You can think of:
  - The Explore phase as being centred on you, as a researcher, as you dig deep into your data
  - The Refine phase as being how you and your team move towards a satisfying solution
  - and the Produce phase as being how you communicate your results to teh wider community

- In this course, we'll be covering several aspects of this model
  - Our goal is to empower you to explore and get the most out of your data, in a replicable, reproducible, and systematic way
- We'll be covering cleaning, organising, managing, and visualising your data - covering the Explore and Refine phases
  - We'll also try to cover documentation and using RMarkdown to integrate documentation and code - to help support the Refine and Produce phases

- That's probably enough context - let's get to the code.

-----

## 2. WELCOME TO `R`

- Welcome to `R`!

-----

## Learning Objectives

Our goals today are:

- to introduce you to the fundamentals of `R` and `RStudio`, and of programming
- how to manage and process your data with an approach known as the `tidyverse`
- how to produce publication-quality data visualisations with the `ggplot2` package
- and how to combine documentation with analysis and code, using `RMarkdown`

- Working with a programming language (especially if it’s your first time) can be intimidating
  - But knowing even a little bit about `R` and how to manage and handle your own data is incredibly empowering
  - The rewards outweigh any frustrations.
   
- It's not a secret, but even experienced programmers find coding difficult and frustrating at times
  - I've been coding for 40 years and - though I know a bit more than when I started - every time a new language or technique turns up that I want to try, I'm a beginner all over again and feel like I know nothing.
  - So don't let intimidation stop you
  - With time and practice it just gets easier and easier to accomplish what you want.

- Learning to code opens up the full possibilities of computing for analysing your data and automating your work
  - Think of it this way: if you could only do biotechnology using kits you bought off Sigma, you could probably get a lot done.
  - But - if you don’t understand the biochemistry of the kit - how can you tell it's not working? How can you troubleshoot?
  - And how could you do experiments for which there are no kits?
  - Knowing a bit of code lets you troubleshoot, and go beyond kits to create new analyses

- R is one of the most widely-used and powerful programming languages, and it's popular in many areas.
  - R is specifically a statistical language
    - It's got a strong focus on data representation, as you'll see shortly
    - Particularly good for the generation of publication-quality graphs and figures.
  - It is a *general programming language*, though. Most of the concepts you will learn apply to Python and other programming languages.
    - Once you understand programming concepts in one language, it's easier to move across to other languages.

- However, R is not the easiest-to-learn programming language ever created.
  - Please don’t get too discouraged! Some bits and concepts *are* just a bit more difficult than others
  - Even with the modest amount of R we will cover today and tomorrow, you can start using some sophisticated R software packages, have a general sense of how to interpret an R script, and be able to get your own data into a workable form for more sophisticated exploration.
- Get through these lessons, and you will be on your way to being an accomplished R user!

- The other big “secret” of programming is that you can only learn so much by reading about it. You have to do it - and get things wrong - to learn.
  - Do the exercises in class, re-do them on your own, and then work on your own problems, and you'll be expert in no time!

- **Let's get started.**

-----

## What is `R`?

- `R` is a **PROGRAMMING LANGUAGE**, and the **SOFTWARE** that runs programs written in that language.
- `R` is **AVAILABLE ON ALL MAJOR OPERATING SYSTEMS**
- This can sometimes be confusing - **IF AT ANY POINT I AM UNCLEAR, PLEASE ASK!**

- **WHY DO WE USE AND TEACH `R`?**
    - `R` is **FREE AS IN "FREE SAMPLES AT THE SUPERMARKET"**, and very **WIDELY-USED** across a range of disciplines.
    - There are **MANY USEFUL PACKAGES** or data analysis and statistics, **WRITTEN By EXPERTS** at the cutting edge of their fields
    - It has excellent **GRAPHICS CAPABILITIES**
    - There is an international, friendly **COMMUNITY** across a range of disciplines, so it's easy to find local and online support

-----

## What is `RStudio`?

- `RStudio` is an **INTEGRATED DEVELOPMENT ENVIRONMENT** - which is to say it's a very powerful tool for writing, using and running `R`, and programs written in the `R` language.
    - It's available on **ALL MAJOR OPERATING SYSTEMS**
    - It's available as a webserver, too.

- On the left is a screenshot **TAKEN WHILE I WAS WRITING THIS PRESENTATION IN RSTUDIO** on a Mac
- On the right is the Windows version, with an **EXAMPLE ANALYSIS AND VISUALISATION**

- You can use it to **INTERACT WITH `R` DIRECTLY TO EXPERIMENT WITH DATA**
- It has a **CODE/SCRIPT EDITOR FOR WRITING PROGRAMS**
- It has tools for **VISUALISING DATA**
- It has built-in **GIT INTEGRATION FOR MANAGING YOUR PROJECTS**

-----

## Why not use `Excel`?

- I'm **NOT HERE TO CRITICISE `EXCEL`**. `Excel` is brilliant at what it's meant to do. It's **POWERFUL** and **INTUITIVE**.
- But **`R` HAS MANY ADVANTAGES FOR REPRODUCIBLE AND COMPLEX ANALYSIS**

- A key thing for reproducibility is that it **SEPARATES DATA FROM ANALYSIS**.
  - In `R`, when you do anything to the original data, that original data remains unmodified (unless you overwrite the file).
  - **POINT OF GOOD PRACTICE: RAW DATA SHOULD BE READ-ONLY**
  - In `Excel` however it's easy to overwrite data with copy-and-paste (and many bad things have happened as a result) - see Mike Croucher's talk for examples.

- Because **YOUR ANALYSIS IN `R` IS A PROGRAM**, every step is written down explicitly, and is transparent and understandable by someone else - and by the computer.
  - You can give your analysis to someone else and they can rerun it, or improve on it
  - In `Excel`, there is no clear record of where you moved your mouse, or what you copied and pasted, and it's not immediately obvious how your formulas work.

- `R` code is **EASY TO SHARE AND ADAPT**, and to apply again to a different or a modified input dataset. It's easy to publish the analyses via online resources.
- `R` code can also be **RUN ON EXTREMELY LARGE DATASETS**, quickly. That's much harder in `Excel`.

----

## `RStudio` overview - INTERACTIVE DEMO

- **START `RStudio`** (click icon/go into start menu and select RStudio/etc.)
    - **CHECK EVERYONE CAN START `RSTUDIO`**

![images/red_green_sticky.png](images/red_green_sticky.png)

- **REMIND PEOPLE THEY CAN USE RED/GREEN STICKIES AT ANY TIME**
- You should see **THREE PANELS**
    - Interactive `R` console: **you can type here and get instant feedback**
    - Environment/History window
    - Files/Plots/Packages/Help/Viewer: **interacting with files on the computer, and viewing help and some output**

- **REMEMBER THE WINDOWS ARE MOBILE AND PEOPLE COULD HAVE THEM IN ANY CONFIGURATION - THE EXACT ARRANGEMENT IS UNIMPORTANT**

- We're going to use `R` in the interactive console to get used to some of the features of the language, and `RStudio`. **DEMO CODE: ASK PEOPLE TO TYPE ALONG**
    - **THE RIGHT ANGLED BRACKET IS A PROMPT: `R` EXPECTS INPUT**
    - **TYPE THE CALCULATION, THEN PRESS RETURN**

```R
> 1 + 100
[1] 101
> 30 / 3
[1] 10
```

- **RESULT IS INDICATED WITH A NUMBER `[1]`** this indicates the line with output in it
- If you type an **INCOMPLETE COMMAND**, `R` will wait for you to complete it
    - **DEMO CODE**

```R
> 1 +
+
```

- The **PROMPT CHANGES TO `+` WHEN `R` EXPECTS MORE INPUT**
- You can either complete the line, or use `Esc` (`Ctrl-C`) to exit

```R
> 1 +
+ 6
[1] 7
> 1 +
+

>
```

- **ARROW KEYS RECOVER OLD COMMANDS**
- **THE `HISTORY` TAB SHOWS ALL COMMANDS USED**
- `R` will report in **SCIENTIFIC NOTATION**
    - **CHECK THAT EVERYONE KNOWS WHAT SCIENTIFIC NOTATION IS**

![images/red_green_sticky.png](images/red_green_sticky.png)

```R
> 2 / 1000
[1] 0.002
> 2 / 10000
[1] 2e-04
> 5e3
[1] 5000
```

- `R` has many **STANDARD MATHEMATICAL FUNCTIONS**
- **FUNCTION SYNTAX**
    - type the function name
    - open parentheses
    - type input value
    - close parentheses
    - press return
    - **DEMO CODE**

```R
> sin(1)
[1] 0.841471
> log(1)
[1] 0
> log10(10)
[1] 1
> log(10)
[1] 2.302585
```

- How do we learn more about a function, or the difference between `log()` and `log10()`?
- **USE `R` BUILT-IN HELP**
    - Type `?` then the function name
    - Scroll to the bottom of the page to find example code

```R
> ?log
```

- This brings up help in the **HELP WINDOW**
- You can also use the **SEARCH BOX** at the top of the help window (try `sin()`)
- If you're not sure about spelling, the editor has **AUTOCOMPLETION** which will suggest all possible endings for something you type (try `log`) - **USE TAB TO SEE AUTOCOMPLETIONS**

- We can do **COMPARISONS** in `R`
    - Comparisons return `TRUE` or `FALSE`. **DEMO CODE**
    - **NOTE:** when comparing numbers, it's better to use `all.equal()` (*machine numeric tolerance*) **ASK IF THERE'S ANYONE FROM MATHS/PHYSICS**

```R
> 1 == 1
[1] TRUE
> 1 != 2
[1] TRUE
> 1 < 2
[1] TRUE
> 1 <= 1
[1] TRUE
```

- `R` has many **STANDARD MATHEMATICAL FUNCTIONS**
- **FUNCTION SYNTAX**
    - type the function name
    - open parentheses
    - type input value
    - close parentheses
    - press return
    - **DEMO CODE**

```R
> sin(1)
[1] 0.841471
> log(1)
[1] 0
> log10(10)
[1] 1
```

- **THE ORDER/CONSTRUCTION OF MATHEMATICAL OPERATIONS CAN MATTER**
  - Write somewhere if possible: $a = \log(0.01^{200})$, $b = 200 \times \log(0.01)$
  - These two mathematical expressions are exactly equal: $a = b$
  - But computers are not mathematicians, they're machines. Numbers are susceptible to this *rounding error*, so what happens is this:

```R
> log(0.01^200)
[1] -Inf
> 200 * log(0.01)
[1] -921.034
```

- **COMPUTERS DO WHAT YOU TELL THEM, NOT NECESSARILY WHAT YOU WANT**

-----

## Variables

- **VARIABLES** are critical to programming in general, and also to working in `R`
- To do interesting and useful things, we need a way to label and refer to a piece of data
  - **We use *variables* for this**
  
- Variables are like **NAMED BOXES**
  - Like a box, they **HOLD THINGS**
  - When we make reference to a box's name, we **MEAN THE THING THE BOX CONTAINS**
- Here, the box is called `Name`, and it contains the word `Samia`
- When we refer to the box, we call it `Name`, and we might ask questions like:
  - "What is the length of `Name`?", meaning "What is the length of the word in the box called `Name`?" (answer: 5)
- Like boxes, a variable **CAN BE EMPTY**
- We can also take the contents out and replace them with something else, but **KEEP THE NAME**

-----

## Variables - INTERACTIVE DEMO

- This is a very important concept, so we're going to go through some practical examples, to reinforce it
    - In `R`, variables are assigned with the **ASSIGNMENT OPERATOR** `<-`
    - We will assign the value `1/40` to the variable `x`
    - **DEMO CODE**

```R
> x <- 1 / 40
```

- At first, nothing seems to happen, but we can see that the variable `x` now exists, and contains the value `0.025` - a **DECIMAL APPROXMATION** of the fraction `1/40`

```R
> x
[1] 0.025
```

- We can also print the output by putting the expression in parentheses

```R
> (x <- 1/40)
[1] 0.025
```

- **CLICK ON THE ENVIRONMENT WINDOW**
  - You should see that `x` is now defined there
  - The *Environment* window in `RStudio` tells you the name and content of every variable currently active in your `R` session.

- This **VARIABLE CAN BE USED ANYWHERE THAT EXPECTS A VALUE**

```R
> x + x
[1] 0.05
> 2 * x
[1] 0.05
> x ^ 2
[1] 0.000625
```

- such as an argument to a function

```R
> log(x)
[1] -3.688879
> sin(x)
[1] 0.0249974
```

- We can **REASSIGN VALUES TO VARIABLES**
    - **MONITOR THE VALUE OF `x` IN THE ENVIRONMENT WINDOW**
    - We can also assign a variable to itself, to modify the variable

```R
> x <- 100
> x <- x + 5
> x
[1] 105
```

- We can assign **ANY KIND OF VALUE** to a variable
    - Including **STRINGS** - i.e. sets of characters

```R
> name <- "Samia"
> name
[1] "Samia"
```

-----

## Naming Variables

- **VARIABLE NAMES ARE DOCUMENTATION**
  - they should describe what the data represents
    - I expect you can tell, just by reading, what all these variables represent
  - **This makes the code more readable** - you can track the operations on a specific bit of data
  - ("anonymous" variables are also helpful, e.g. `x` or `i`)

- There are some rules and guidelines for allowed and effective variable names
  - The variable names should be explicit, but not too long
  - In `R` names **cannot** start with a digit
  - `R` is also case sensitive, so `Weight` with a capital letter is not the same name as `weight` with a lower-case letter
  - Problems will arise if you call any variables by the name of an existing `R` function
  - You should use consistent styling to handle multiple words

-----

## Functions

- You've already used some **functions** (`log()`, `sin()`, etc.). These are like "canned scripts"
- Functions have **THREE MAIN PURPOSES**
  - They **ENCAPSULATE AND AUTOMATE COMPLEX TASKS** - you don't need to worry about how a sine is calculated, just that you give the function a value, and it tells you what the sine is.
  - They **MAKE CODE MORE READABLE** - by dividing code into logical operations, represented by short names that describe an action, the code is easier to read
  - They also **MAKE CODE MORE REUSABLE** - you don't need to write the routine for finding a square root every time you want one, you just need to call the `sqrt()` function

- Functions usually **TAKE ARGUMENTS** (input), e.g. `sqrt(4)` - the `4` is an argument
- Functions often **RETURN** values (output), e.g. `sqrt(4)` **returns** the value `2`

- **ALL THE FUNCTIONS YOU'VE SEEN SO FAR ARE BUILT-IN**, the so-called `base` functions
- **YOU CAN WRITE YOUR OWN FUNCTIONS**
- **OTHER FUNCTIONS FOR SPECIFIC TASKS CAN BE BROUGHT IN, THROUGH `libraries`**

-----

## Getting Help in `R`: INTERACTIVE DEMO

- **DEMO IN CONSOLE**

```R
> args(lm)
function (formula, data, subset, weights, na.action, method = "qr",
    model = TRUE, x = FALSE, y = FALSE, qr = TRUE, singular.ok = TRUE,
    contrasts = NULL, offset, ...)
NULL
> ?sqrt
> help(sqrt)
> ??sqrt
> help.search("sqrt")
> help.search("categorical")
> vignette(two-table)
Error in vignette(two - table) : object 'two' not found
> vignette("two-table")
```

-----

## Challenge 01

Link: [https://strathsci.qualtrics.com/jfe/form/SV_eG17F5atskDqbC6](https://strathsci.qualtrics.com/jfe/form/SV_eG17F5atskDqbC6)

Solution:

`mass <- 47.5`
This will give a value of 47.5 for the variable mass

`age <- 122`
This will give a value of 122 for the variable age

`mass <- mass * 2.3`
This will multiply the existing value of 47.5 by 2.3 to give a new value of 109.25 to the variable mass.

`age <- age - 20`
This will subtract 20 from the existing value of 122 to give a new value of 102 to the variable age.

![images/red_green_sticky.png](images/red_green_sticky.png)

-----

## 3. PROJECT MANAGEMENT IN `R`

-----

## How Projects Tend To Grow

- I'm sure you all recognise this situation

- Research tends to be incremental
  - Projects start out as random notes here, a bit of code there, some data over there
  - and eventually a manuscript is written

- There are many reasons why we should **ALWAYS** avoid working in a random manner, and naming files like they do in the cartoon.
  - Basically, good practice ensures reproducibility and makes everyone's lives easier.

-----

## Good Practice

- There is **NO SINGLE GOOD WAY TO ORGANISE A PROJECT**
  - It's important to find something that **WORKS FOR YOU**
  - But it's **ALSO IMPORTANT THAT IT WORKS FOR COLLABORATORS**
  - Some **PRINCIPLES MAKE THINGS EASIER FOR EVERYONE**

- Using a **SINGLE WORKING DIRECTORY PER PROJECT/ANALYSIS**
  - **NAME IT AFTER THE PROJECT**
  - **EASY TO PACKAGE UP** the whole directory and move it around, or share it - **OR PUBLISH ALONGSIDE YOUR PAPER**
  - **NO NEED TO HUNT AROUND THE WHOLE DISK** to find relevant or important files.
  - You can use **RELATIVE PATHS** that will always work, so long as you work within the project directory
- Treat your **RAW DATA AS READ-ONLY**
  - Establishes **PROVENANCE** and **ENABLES REANALYSIS**
  - Keep raw data in a **SEPARATE SUBFOLDER**
- **CLEAN THE DATA PROGRAMMATICALLY** (part of the analysis chain)
  - Most of the time, your data will be "dirty" - it won't be in the form necessary for your analysis.
  - It is often said that 80% of data analysis is spent on the process of cleaning and preparing the data
  - Remove/fill in null values, etc. - whatever is appropriate
  - **KEEP CLEANED DATA SEPARATE FROM RAW** - like food hygiene
- **GENERATED OUTPUT IS DISPOSABLE**
  - This means **ANYTHING GENERATED AUTOMATICALLY BY YOUR CODE/ANALYSIS**
  - If a file can be generated by scripts/code in your project, no need to put it under version control
  - keep in its own subdirectory

-----
## Example Directory Structure

- This is **ONE OF MANY WAYS TO STRUCTURE YOUR WORKING DIRECTORY**
    - It's a good starting point, but something else might be more appropriate for your own work

- **`WORKING DIR/`** is the *root* directory of the project.
    - Everything related to the project (subdirectories of data, scripts and figures; `git` files; configuration files; notes to yourself; whatever)
    - Name this after your project
- **`data/`** is a subdirectory for storing data
    - raw data only, or raw and intermediate data? **YOUR DECISION**
    - store data and metadata (data *about* the data) together
    - `data/raw`, `data/intermediate` - **USE SUBFOLDERS WHEN SENSIBLE**
- **`data_output/`** could be a place to write the analysis output (`.csv` files etc.)
- **`documents/`** is a place where notes, drafts, supporting material, and explanatory text could be stored
- **`fig_output/`** could be a place to write graphical output of the analysis (keep separate from tables)
- **`scripts`** might be where you would choose to keep the executable code that automates your analysis

- The important thing is that the structure is **AS SELF-EXPLANATORY AS POSSIBLE**

-----

## Project Management in `RStudio`

- `RStudio` **TRIES TO BE HELPFUL** and provides the 'Project' concept
    - Keeps **ALL PROJECT FILES IN A SINGLE DIRECTORY**
    - **INTEGRATES WITH `GIT`**
    - Enables switching between projects within `RStudio`
    - Keeps project histories

- We're going to create a **NEW PROJECT** in `RStudio`

- **INTERACTIVE DEMO**

- **CREATE PROJECT**
- Click `File` -> `New Project`
    - Options for how we want to create a project: brand new in a new working directory; turn an existing directory into a project; or checkout a project from `GitHub` or some other repository
- Click `New Directory`
    - Options for various things we can do in `RStudio`. Here we want `New Project`
- Click `New Project`
    - We are asked for a directory name. **ENTER `ibioic-r-lesson`**
    - We are asked for a parent directory. **PUT YOURS ON THE DESKTOP; STUDENTS CAN CHOOSE ANYWHERE SENSIBLE**
- Click `Create Project`
- **YOU SHOULD SEE AN EMPTY-ISH `RSTUDIO` WINDOW**

- **INSPECT PROJECT ENVIRONMENT**
- First, **NOTE THE WINDOWS**: editor; environment; files
- **EDITOR** is empty
- **ENVIRONMENT** is empty
- **FILES** shows
    - **CURRENT WORKING DIRECTORY** (see breadcrumb trail)
      - **CHANGE CWD IF NECESSARY**
      - **SHOW TERMINAL**
    - **ONE FILE**: `*.Rproj` - information about your project

- **CREATE DIRECTORIES IN PROJECT**
- **Create directoris called `scripts` and `data`**
    - Click on `New Folder`
    - Enter directory name (`scripts`)
    - Note that the directory now exists in the `Files` tab
    - Do the same for `data/`
- **NOTE THAT WE WILL NOW POPULATE THE DIRECTORY**

-----

## Working in RStudio

- `RStudio` offers **SEVERAL WAYS TO WRITE CODE**
    - We'll not see all of them today
    - You've seen **DIRECT INTERACTION IN THE CONSOLE** (entering variables)
    - `RStudio` also has an editor for writing scripts, notebooks, markdown documents, and Shiny applications (**EXPLAIN BRIEFLY**)
    - It can also be used to write plain text

- **INTERACTIVE DEMO OF `R` SCRIPT**

- Click on `File` -> `New File` -> `Text File`. **NOTE THAT THE EDITOR WINDOW OPENS**
- Enter the following text, and **EXPLAIN CSV**
    - plain text file
    - one row per line
    - column entries separated by commas
    - first row is header data
    - **NEEDS A BLANK LINE AT THE END**
    - **DATA DESCRIBES CATS**

```text
coat,weight,likes_string
calico,2.1,1
black,5.0,0
tabby,3.2,1
```

- **SAVE THE FILE AS `data/feline_data.csv`**
    - Click on disk icon
    - Navigate to `data/` subdirectory
    - Enter filename `feline_data.csv`
- **CLOSE THE EDITOR FOR THAT FILE**

- Click on `File` -> `New File` -> `R Script`.
- **EXPLAIN COMMENTS** while entering the code below
    - **COMMENTS ANNOTATE YOUR CODE**: reminders for you, and information for others
- **EXPLAIN `read.csv()`**
    - `read.csv()` is a **FUNCTION** that reads data from a **CSV-FORMAT FILE** into a variable in `R`

```R
# Script for exploring data structures

# Load cat data as a dataframe
cats <- read.csv(file = "data/feline_data.csv")
```

- **SAVE THE SCRIPT**
    - Click on `File` -> `Save`
    - Navigate to the `scripts/` subdirectory
    - Enter filename `data_structures` (**EXTENSION IS AUTOMATICALLY APPLIED**)
- **DO YOU SEE THE VARIABLE IN THE ENVIRONMENT?**
    - **NO** - because the code hasn't been executed, only written.

- **RUN THE SCRIPT**
    - Click on `Source` and **NOTE THIS RUNS THE WHOLE SCRIPT**
- Go to the `Environment` tab
    - **NOTE THE DATA WAS LOADED IN THE VARIABLE `cats`**
    - Note that there is a description of the data (3 obs. of 3 variables)
    - **CLICK ON THE VARIABLE AND NOTE THAT THE TABLE IS NOW VISIBLE** - this is helpful
    - **YOU CANNOT EDIT THE DATA IN THIS TABLE** - you can sort and filter, but not modify the data. This **ENFORCES GOOD PRACTICE** (compare to Excel).

-----

## 4. A FIRST ANALYSIS IN `RSTUDIO`

-----

## Our Task

- We've got some medical data relating to a new treatment for arthritis
- There are some measurements of patient inflammation, taken over a period of days post-treatment for each patient
- We've been **ASKED TO PRODUCE A SUMMARY AND SOME GRAPHS**

- **DOWNLOAD THE FILE FROM THE LINK TO `data/`**
- **EXPLAIN THE LINK IS ON THE ETHERPAD PAGE** (no need to type!)
- **DEMO THIS**
    - **NOTE:** A new directory is created *within* `data`, called `data`. **THIS IS UNTIDY, SO LET'S CLEAN**
    - **COPY ALL FILES BEGINNING WITH `inflammation` TO THE PARENT FOLDER**
    - **THEN DELETE THE SUBFOLDER AND ZIP FILE**

- **CHECK EVERYONE'S READY TO PROCEED**

![images/red_green_sticky.png](images/red_green_sticky.png)

----

## Loading Data - INTERACTIVE DEMO

- We've already created some cat data manually, but **THIS IS UNUSUAL** - most data comes in the form of plain text files

**START DEMO**

- **INSPECT DATA IN FILES WINDOW**
    - Click on filename, and select `View File`
    - Note: **THERE IS NO HEADER** and **THERE ARE NO ROW NAMES**
    - Ask: **IS THIS WELL-FORMATTED DATA?**
    - I happen to know that there is **one row per patient, and the columns are days, in turn, post-treatment**, and **measurements are inflammation levels**
      - **WE SHOULD RECORD THIS SOMEWHERE AS METADATA**
- **WHAT IS THE DATA TYPE**
    - Tabular, with **EACH COLUMN SEPARATED BY A COMMA**, so **CSV**
    - **IN THE CONSOLE** use `read.csv()` to read the data in
    - Note: **IF WE DON'T ASSIGN THE RESULT TO A VARIABLE WE JUST SEE THE DATA**
- **CREATE A NEW SCRIPT**
    - Click the **triangle next to the new document icon**
    - Add the code and **SAVE AS `scripts/inflammation`** (`RStudio` adds the extension)
    - See that the file appears in `Files` window

```R
# Preliminary analysis of inflammation in arthritis patients

# Load data (no headers, CSV)
data <- read.csv(file = "data/inflammation-01.csv", header = FALSE)
```

- **INSPECT THE DATA**
    - `Source` the script
    - Check the `Environment` window: 60 observations (patients) of 40 variables (days)
    - **CLICK ON `data`**
    - **COLUMN HEADERS ARE PROVIDED: `Vn`** for *variable n*
    - `dim()` - *dimensions* of data: rows X columns
    - `length()` - number of columns in the table
    - `ncol()` - number of columns in the table
    - `nrow()` - number of rows in the table

```R
> head(data, n = 2)
  V1 V2 V3 V4 V5 V6 V7 V8 V9 V10 V11 V12 V13 V14 V15 V16 V17 V18 V19 V20 V21 V22 V23 V24 V25 V26
1  0  0  1  3  1  2  4  7  8   3   3   3  10   5   7   4   7   7  12  18   6  13  11  11   7   7
2  0  1  2  1  2  1  3  2  2   6  10  11   5   9   4   4   7  16   8   6  18   4  12   5  12   7
  V27 V28 V29 V30 V31 V32 V33 V34 V35 V36 V37 V38 V39 V40
1   4   6   8   8   4   4   5   7   3   4   2   3   0   0
2  11   5  11   3   3   5   4   4   5   5   1   1   0   1
> dim(data)
[1] 60 40
> length(data)
[1] 40
> ncol(data)
[1] 40
> nrow(data)
[1] 60
```

-----

## Challenge 02

-*SOLUTION**

```R
read.csv(file='file.csv', sep=';', dec=',')
```

![images/red_green_sticky.png](images/red_green_sticky.png)

-----

## Indexing Data

- Our inflammation is in a **TABLE**, also known as an **ARRAY** or **MATRIX**
- There is a **SET OF CONVENTIONS FOR REFERRING TO THIS DATA**
  - `R` keeps to these conventions

- If we want to refer to a particular row (equivalent to a patient), we refer to the number down the side, in green
  - Patient 2 is row 2

- If we want to refer to a particular column (equivalent to a day of study), we refer to the number along the top, in magenta
  - Day 30 is column 30

- To refer to a specific combination of patient and day, we need to refer to the row first, then the column
  - Patient 3 on day 2 is the element *a32*, here.

-----

## Indexing Data - INTERACTIVE DEMO

- **HOW DO WE GET ACCESS TO A SUBSET OF THE DATA?**

- We can refer to an element in our dataset by *indexing* it
    - We **LOCATE A SINGLE ELEMENT as `[row, column]` in square brackets**

```R
> ncol(data)
[1] 40
> data[1,1]
[1] 0
> data[50,1]
[1] 0
> data[50,20]
[1] 16
> data[30,20]
[1] 16
```

- To get a **RANGE OF VALUES**, use the `:` separator to mean 'to':

```R
> data[1:4, 1:4]   # rows 1 to 4; columns 1 to 4
  V1 V2 V3 V4
1  0  0  1  3
2  0  1  2  1
3  0  1  1  3
4  0  0  2  0
> data[30:32, 20:22]
   V20 V21 V22
30  16  14  15
31  16  13   7
32   9  19  15
```

- To get a **WHOLE ROW OR COLUMN**, leave that entry blank

```R
> data[5,]
  V1 V2 V3 V4 V5 V6 V7 V8 V9 V10 V11 V12 V13 V14 V15 V16 V17 V18 V19 V20 V21 V22 V23 V24 V25 V26
5  0  1  1  3  3  1  3  5  2   4   4   7   6   5   3  10   8  10   6  17   9  14   9   7  13   9
  V27 V28 V29 V30 V31 V32 V33 V34 V35 V36 V37 V38 V39 V40
5  12   6   7   7   9   6   3   2   2   4   2   0   1   1
> data[,16]
 [1]  4  4 15  8 10 15 13  9 11  6  3  8 12  3  5 10 11  4 11 13 15  5 14 13  4  9 13  6  7  6 14
[32]  3 15  4 15 11  7 10 15  6  5  6 15 11 15  6 11 15 14  4 10 15 11  6 13  8  4 13 12  9
```

-----

## Summary Functions - INTERACTIVE DEMO

- **`R` was designed for data analysis**, so has many built-in functions for analysing and describing data
    - **TALK THROUGH CODE IN CONSOLE**

```R
> max(data)
[1] 20
> max(data[2,])
[1] 18
> max(data[,7])
[1] 6
> min(data[,7])
[1] 1
> mean(data[,7])
[1] 3.8
> median(data[,7])
[1] 4
> sd(data[,7])
[1] 1.725187
```

-----

## Repetitive Calculations - INTERACTIVE DEMO

- We might want to **CALCULATE MEAN INFLAMMATION FOR EACH PATIENT**, but doing it the way we've just seen is tedious and slow.
  - What we'd like to do is **APPLY THE SAME FUNCTION TO EACH ROW**
- Happily **COMPUTERS WERE INVENTED TO SAVE US THE HASSLE**
- We could automate this task in any of several ways available in `R`
  - `R` has an `apply()` function exactly for this
  - **IN THE CONSOLE**

- `apply()` takes three arguments:
  - `X` is your dataset
  - `MARGIN` is the *axis* of the dataset
    - rows are `1`
    - columns are `2`
    - datasets can be multidimensional, so the margins can go higher than 2
  - `FUN` is the function we want to apply
- So, here, we are applying the `mean()` function to each `row` in the dataset called `data`
  - This gives us the average inflammation per patient

```R
> apply(X = data, MARGIN = 1, FUN = mean)
 [1] 5.450 5.425 6.100 5.900 5.550 6.225 5.975 6.650 6.625 6.525 6.775 5.800 6.225 5.750 5.225
[16] 6.300 6.550 5.700 5.850 6.550 5.775 5.825 6.175 6.100 5.800 6.425 6.050 6.025 6.175 6.550
[31] 6.175 6.350 6.725 6.125 7.075 5.725 5.925 6.150 6.075 5.750 5.975 5.725 6.300 5.900 6.750
[46] 5.925 7.225 6.150 5.950 6.275 5.700 6.100 6.825 5.975 6.725 5.700 6.250 6.400 7.050 5.900
```

- **IN OUR ANALYSIS SCRIPT** we want to assign these values to a variable, and **ALSO CALCULATE AVERAGE BY DAY**
    - So long as we provide arguments in the correct order, **WE DON'T NEED TO PROVIDE ARGUMENT NAMES** - true for most `R` functions

```R
# Calculate average inflammation by patient and day
avg_inflammation_patient <- apply(X = data, MARGIN = 1, FUN = mean)
avg_inflammation_day <- apply(data, 2, mean)
```

- **RUN THE LINES**
    - Note that the values appear in the Environment tab
- Like many common operations, there's an `R` function that's a shortcut
    - **IN THE CONSOLE**

```R
> rowMeans(data)
 [1] 5.450 5.425 6.100 5.900 5.550 6.225 5.975 6.650 6.625 6.525 6.775 5.800 6.225 5.750 5.225
[16] 6.300 6.550 5.700 5.850 6.550 5.775 5.825 6.175 6.100 5.800 6.425 6.050 6.025 6.175 6.550
[31] 6.175 6.350 6.725 6.125 7.075 5.725 5.925 6.150 6.075 5.750 5.975 5.725 6.300 5.900 6.750
[46] 5.925 7.225 6.150 5.950 6.275 5.700 6.100 6.825 5.975 6.725 5.700 6.250 6.400 7.050 5.900
> colMeans(data)
        V1         V2         V3         V4         V5         V6         V7         V8         V9
 0.0000000  0.4500000  1.1166667  1.7500000  2.4333333  3.1500000  3.8000000  3.8833333  5.2333333
       V10        V11        V12        V13        V14        V15        V16        V17        V18
 5.5166667  5.9500000  5.9000000  8.3500000  7.7333333  8.3666667  9.5000000  9.5833333 10.6333333
       V19        V20        V21        V22        V23        V24        V25        V26        V27
11.5666667 12.3500000 13.2500000 11.9666667 11.0333333 10.1666667 10.0000000  8.6666667  9.1500000
       V28        V29        V30        V31        V32        V33        V34        V35        V36
 7.2500000  7.3333333  6.5833333  6.0666667  5.9500000  5.1166667  3.6000000  3.3000000  3.5666667
       V37        V38        V39        V40
 2.4833333  1.5000000  1.1333333  0.5666667
```

-----

## Base Graphics

- We're doing all this work to try to **GAIN INSIGHT INTO OUR DATA**
- **VISUALISATION IS A KEY ROUTE TO INSIGHT**

- `R` has many graphics packages - some of which produce extremely beautiful images, or are tailored to a specific problem domain

- The built-in graphics are known as **BASE GRAPHICS**
- They may not be as pretty, or as immediately suited for all circumstances as some other packages, but they are still very powerful
  - `ggplot2` is built out of base graphics

-----

## Plotting - INTERACTIVE DEMO

- **IN THE SCRIPT**
    - `R`'s **`plot()` FUNCTION IS GENERAL AND WORKS FOR MANY KINDS OF DATA**
    - **RUN EACH LINE IN TURN**
    - **NOTE WHERE PLOTS SHOW** (Plot window)
    - Opportunity to note: **VARIABLES HELP READABILITY**
    - **USE ARROW BUTTONS** to cycle through plots

```R
# Plot data summaries
# Average inflammation by patient
plot(avg_inflammation_patient)

# Average inflammation per day
plot(avg_inflammation_day)

# Maximum inflammation per day
max_inflammation_day <- apply(data, 2, max)
plot(max_inflammation_day)

# Minimum inflammation per day
plot(apply(data, 2, min))

# Show a histogram of average patient inflammation
hist(avg_inflammation_patient)
```

- **THE `hist()` FUNCTION PLOTS A HISTOGRAM OF INPUT DATA FREQUENCY/COUNT**
    - The choice of bin sizes/*breaks* could be improved
    - We need to **PROVIDE THE BOUNDARIES BETWEEN BINS**
    - **IN THE CONSOLE**

```R
hist(avg_inflammation_patient, breaks=c(5, 6, 7, 8))
```

- We'd have to **TYPE IN A LOT OF NUMBERS** to get smaller breaks, which is **SLOW**
    - The `seq()` function generates a sequence of numbers for us

```R
> seq(5, 8)
[1] 5 6 7 8
> hist(avg_inflammation_patient, breaks=seq(5, 8))
```

- We can **SET THE INTERVAL OF THE SEQUENCE**

```R
> seq(5, 8, by=0.2)
 [1] 5.0 5.2 5.4 5.6 5.8 6.0 6.2 6.4 6.6 6.8 7.0 7.2 7.4 7.6 7.8 8.0
> hist(avg_inflammation_patient, breaks=seq(5, 8, by=0.2))
```

- **IN THE SCRIPT**
    - Add a line with the histogram for average patient inflammation

```R
# Show a histogram of average patient inflammation
hist(avg_inflammation_patient, breaks=seq(5, 8, by=0.2))
```

- **IN THE SCRIPT**
    - Demonstrate changing the input file
    - **CHANGING FILENAME IN A SCRIPT IS QUICKER THAN RETYPING ALL THE COMMANDS**
    - **THE ANALYSIS IS REPRODUCIBLE ON NEW DATA**

-----

## Challenge 03 (5min)

```R
# Plot standard deviation by day
plot(apply(data, 2, sd))
hist(avg_inflammation_day, breaks=seq(5, 8, by=0.2))
```

![images/red_green_sticky.png](images/red_green_sticky.png)

-----

## 4. Data Types and Structures in `R`