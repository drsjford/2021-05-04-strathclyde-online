# r-lesson.md - 2021-05-04-strathclyde-online

**START THE SLIDES**

-----

## 1. DATA ANALYSIS

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

-----

## 2. WELCOME TO `R`

- Welcome to `R`!
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