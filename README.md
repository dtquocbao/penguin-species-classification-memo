# Penguin Species Classification Memo

STAT 692 Practice 1 — a short analytical memo that classifies an unidentified penguin specimen using the [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/) dataset.

## Overview

Dr. Sharma provided measurements from an unidentified penguin specimen:

| Measurement     | Value  |
|-----------------|--------|
| Bill length     | 45 mm  |
| Flipper length  | 220 mm |

This project compares those measurements to known Adelie, Chinstrap, and Gentoo penguins using exploratory visualization and a multinomial logistic regression model. The analysis concludes that the specimen is most likely a **Gentoo** penguin, driven primarily by its unusually long flipper length.

## Repository Contents

| File | Description |
|------|-------------|
| `stat692-practice1.Rmd` | R Markdown source for the memo (knits to PDF) |

## Requirements

- [R](https://cran.r-project.org/) (4.x recommended)
- [RStudio](https://posit.co/download/rstudio-desktop/) or another R Markdown-capable editor
- A LaTeX distribution with XeLaTeX (e.g. [TinyTeX](https://yihui.org/tinytex/)) for PDF output

Install the required R packages:

```r
install.packages(c("palmerpenguins", "tidyverse", "nnet", "knitr", "kableExtra"))
```

## Rendering the Memo

From the project directory in R:

```r
rmarkdown::render("stat692-practice1.Rmd")
```

Or open `stat692-practice1.Rmd` in RStudio and click **Knit** to produce `stat692-practice1.pdf`.

## Methods

1. **Data** — Palmer Penguins dataset; records with missing bill or flipper length are dropped.
2. **Exploratory analysis** — scatter plot of bill length vs. flipper length with the unidentified specimen marked.
3. **Classification** — multinomial logistic regression (`nnet::multinom`) using bill length and flipper length as predictors.
4. **Output** — species membership probabilities and a written recommendation.

## Author

Tran Quoc Bao Dang
