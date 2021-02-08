---
title:  "SYS 5581 Time Series and Forecasting"
author: "Computing setup and guide"
date:   "Version of 2021-02-03"

output: 
#   pdf_document:
# #   keep_tex: true
#     fig_caption: yes
#     latex_engine: pdflatex

  html_document:
    keep_md: true

urlcolor: blue
geometry: margin=1in

fontfamily: mathpazo
fontsize: 11pt
header-includes:
   - \linespread{1.05}
---







The course relies on computing resources. Please install the software as indicated on your local machine, and familiarize yourself with the associated documentation. 

# The R programming language, and related resources

We will do our coding in R, a programming language especially well-suited to statistical computing. 

* [Download and install R](https://cran.rstudio.com/), v. 3.0.1+.

[R Studio](https://rstudio.com/products/rstudio/) is an integrated development environment (IDE) for R. It offers a variety of utilities to enhance the experience of coding and generating documents.

* [Download and install R Studio](https://rstudio.com/products/rstudio/download/#download), v. 1.4.1+. 

[Tidyverse](https://www.tidyverse.org/) is a collection of packages that extend the capabilities of R for doing data science.

* Install the Tidyverse: From the Console tab in R Studio (or from R running in a Terminal window), enter: `install.packages("tidyverse")`.

[Tidyverts](https://tidyverts.org/) is a collection of R packages for time series analysis designed to work well with the Tidyverse packages.

* Each package in the tidyverts suite needs to be installed individually. From the Console tab in R Studio (or from R running in a Terminal window), enter: `install.packages(c("tsibble", "tsibbledata", "feasts", "fable"))`.
  - You don't need to install the `tsibbletalk` and `fable.prophet` packages; we probably won't use them in this course. 
  

# Git and Github

[Git](https://git-scm.com/) is software for version control. Github is a web service that provides remote storage and access to files via git. This setup greatly facilitates collaboration between multiple individuals working on the same code base.

First watch this short YouTube video to get an orientation to git and Github: [Git and GitHub for an Organized Project (STAT 545 Episode 2-A)](https://www.youtube.com/watch?v=l2ftm-YwJs8) from the University of British Columbia.

Then install git on your machine and link it to your R Studio instance and your file repository on Github:

* [Follow these instructions](https://jennybc.github.io/2014-05-12-ubc/ubc-r/session03_git.html) to [download and install git](https://git-scm.com/downloads) and to link git with R Studio.

A collection of files associated with a single project is in git-speak called a "repository" or *"repo"*. You should already have a basic repo set up for you on the course site on Github. The next step is to copy ("clone") this remote repo to your local machine.

* Clone your course repo on Github to a new R Studio project on your local machine.
  - Navigate to [the course website on Github](https://github.com/uva-eng-time-series-sp21). Select your repo.
  - Click on the green button labeled "Code". Copy the URL.
  - In the R Studio window, from the pull-down menu in the upper-right corner, select `New Project...`, `Version Control`, `Git`. Paste the URL into the dialog box labeled `Repository URL`.
  - Optional: Change the name of the project folder, and the location of this folder on your local directory tree.
  - Click on `Create Project`. The files from your remote repo should be copied to your local machine in a new folder with the name you chose.
  
* Optional: [Download and install the Github desktop client](https://git-scm.com/downloads/guis), or an alternative GUI client.
  - The git operations you need for this course can be managed within R Studio, from the `Git` tab. Some more advanced operations require using either a Terminal window, or a Git desktop client. 
  
As you get going, you will likely want to learn more about how to work with git and Github. [Review the documentation for git](https://git-scm.com/) and [this Github Guide](https://guides.github.com/introduction/flow/). Learn the basics.



# Markdown and R Markdown

Markdown is a markup language: a set of formatting instructions for rendering documents. R Markdown is an extension of Markdown that allows for embedding chunks of R code into a Markdown document. In this course, we will write our work in R Markdown within the R Studio environment, then use the `knitr` package to generate HTML and PDF output files.

For a nice introduction to Markdown and R Markdown, watch the short YouTube video [Reproducible Reports with R Markdown (STAT 545 Episode 3-A)](https://www.youtube.com/watch?v=ZzDSkBgt9xQ) from the University of British Columbia.

As you proceed in creating your documents, you will probably want to access additional resources:

* From within R Studio, you can access an R Markdown Cheat Sheet via `Help/Cheatsheets`.

* Markdown reference: https://www.markdownguide.org/

* R Markdown reference: https://rmarkdown.rstudio.com/


# Bibliographic resources: Zotero and Bibtex

[Coming soon...]

# General course web resources

  * [Collab class site](https://collab.its.virginia.edu), for basic course information, assignments, office hours sign-up, links to online textbook and other resources.
  * [Github class site](https://github.com/uva-eng-time-series-sp21), for posting and sharing code.
  * Zoom, for class sessions, recordings, and office hours.


