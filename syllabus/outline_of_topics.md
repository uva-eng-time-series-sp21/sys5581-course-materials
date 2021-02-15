---
title: "SYS 5581 Time Series and Forecasting"
subtitle:    "Outline of topics"
author: "Instructor: Arthur Small"
date:   "University of Virginia Engineering, Spring 2021"

output: 
  pdf_document:
    keep_md: true
    fig_caption: yes
    latex_engine: pdflatex
    toc: true
    number_sections: true

  # html_document:
  #   keep_md: true

urlcolor: blue
geometry: margin=1in

fontfamily: mathpazo
fontsize: 11pt
header-includes:
   - \linespread{1.05}

bibliography: /Users/Arthur/GitRepos/Teaching/time-series/tseries.bib
---



----

FPP = Hyndman, R.J., & Athanasopoulos, G. [-@robjhyndmanForecastingPrinciplesPractice2021] [*Forecasting: principles and practice, 3rd edition*](https://otexts.com/fpp3/), OTexts: Melbourne, Australia. OTexts.com/fpp3

# Part I: Introduction

## Course introduction

Topics:

* What is time series analysis?

Readings: 

* FPP, Ch. 1


## The project

Readings: FPP, Section 5.1.

Assignment: Write a concept note for a potential project.

## Computing setup

Topics: R, R Studio, git, Github, Markdown, R Markdown, Tidyverse and tidyverts packages for R

Assignment: Follow instructions in the course [Computing setup guide](https://github.com/uva-eng-time-series-sp21/sys5581-course-materials/blob/master/computing_setup_guide.pdf).

## Other helpful resources


# Part 2: Data

## Finding and acquiring a dataset for your project

The UVA Libraries offer excellent [data services](https://www.library.virginia.edu/services), including resources for [data discovery and access](https://data.library.virginia.edu/datasources/). If you haven't settled on your own dataset to analyze for your project, you may find one by browsing their [recommended top data sources](https://data.library.virginia.edu/datasources/find-data/) and [licensed data](https://data.library.virginia.edu/datasources/licensed/). If you need personal assistance, you are invited to contact UVA's Data Librarian, Jenn Huck, at data@virginia.edu to schedule an appointment. 

Some data sources you might check out:

* The [Cross-National Time-Series Data Archive](https://data.library.virginia.edu/datasources/licensed/cnts/) provides more than 200 years of annual data from 1815 onward for over 200 countries. It consists of 196 data variables used by academia, government, finance and media.
* [U.S. Energy Information Administration](https://www.eia.gov/tools/). Diverse datasets on energy.
* "[Awesome Public Datasets](https://github.com/awesomedata/awesome-public-datasets)".
* [Flowing Data](https://flowingdata.com/category/statistics/data-sources/) data sources.
* [The Stanford Open Policing Project](https://openpolicing.stanford.edu/). "On a typical day in the United States, police officers make more than 50,000 traffic stops. Our team is gathering, analyzing, and releasing records from millions of traffic stops by law enforcement agencies across the country."
* [Open U.S. Federal Government Data](https://www.data.gov/opendata/).
* [New York City 311 Data](https://portal.311.nyc.gov/article/?kanumber=KA-02893).
* [Charlottesville, Virginia open data](https://opendata.charlottesville.org/)


## Data extraction, transformation, and loading

Topics:

* Tidy data
* `tsibble` objects for storing, manipulating, and visualizing time series data. Frequency of time series: the `index` parameter. `key` parameter(s).
* Applying `dplyr` verbs to `tsibble` objects: `filter`, `select`, `mutate`, `group_by`, `summarize`
* Periodicity. Seasonal periods.


Readings:

* FPP, Section 2.1
* Optional: To learn how to wrangle and visualize data using the Tidyverse packages, you may find it useful to go through the [Tidyverse Fundamentals with R](https://learn.datacamp.com/skill-tracks/tidyverse-fundamentals) modules on [Datacamp](https://learn.datacamp.com/). Datacamp also offers [a range of other learning modules for developing data science skills in R](https://learn.datacamp.com/career-tracks/data-scientist-with-r). 

Assignment: [Extract, transform, and load your data](https://github.com/uva-eng-time-series-sp21/sys5581-course-materials/blob/master/assignments/assignment_data_etl.pdf).

# Part 3: Exploratory data analysis

Topics:

* Time series plots.
* Trends. Seasonal (periodic) patterns. Cycles.
* Seasonal plots. Seasonal sub-series.
* Investigating relationships between two variables. Scatterplots. Correlation. Scatterplot matrices.

Readings: FPP, Sections 2.2--2.6. 

Assignment: Explore your data.


# Part 4: Modeling the data-generating process

## The normal linear model

$$ y_t = \beta_0 + \beta_1 x_t + \varepsilon_t $$

### Assumptions of the linear model

* Relationship between predictor $x$ and predictand $y$ is linear.
* Both $x$ and $y$ are known, observed without error.

* Errors have mean zero.
* Errors are independent of each other.  
* Errors are uncorrelated with predictor variables $x_t$.

Often, assume stronger additional conditions that errors are *independent, identically normally distributed*: for all $t$, $\varepsilon_t \sim N(0, \sigma^2)$. for a constant $\sigma^2$.

In compact vector and matrix notation, we may write: 

$$ Y = X \beta + \varepsilon $$ 
$$\varepsilon \sim N(0, \sigma^2 I_T) $$


Readings: FPP, Section 7.1

### Examples of the normal linear model


## Ordinary least squares estimation

Regression coefficients $\beta$ and error variance $\sigma^2$ are unobserved: their values must be estimated from the data. Various estimation techniques may be used.





----
# References {-}
