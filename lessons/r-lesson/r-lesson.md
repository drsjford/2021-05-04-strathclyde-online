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