# Penguin Species Classification Memo

STAT 692-701 Statistical Consulting - Practice 1. An analytical memo that classifies an unidentified penguin specimen using the [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/) dataset.

## Overview

Dr. Sharma provided measurements from an unidentified penguin specimen:

| Measurement     | Value  |
|-----------------|--------|
| Bill length     | 45 mm  |
| Flipper length  | 220 mm |

The analysis compares those measurements to known Adelie, Chinstrap, and Gentoo penguins using exploratory visualization and a multinomial logistic regression model. Both visual and statistical evidence indicate the specimen is most likely a **Gentoo** penguin, driven primarily by its unusually long flipper length.

## Repository Contents

| File | Description |
|------|-------------|
| `stat692-practice1_final_report.Rmd` | **Submission memo**: client-facing report and technical appendix (course template) |
| `stat692-practice1_final_report.pdf` | Rendered PDF of the template submission |
| `stat692-practice1_technical_report.Rmd` | Full standalone reproducible analysis memo |
| `stat692-practice1_technical_report.pdf` | Rendered PDF of the standalone memo |
| `Penguin Species Classification Memo.pptx` | Presentation slides |

### Deliverable Structure

The template submission (`stat692-practice1_final_report.Rmd`) has two parts:

1. **Part 1 - Client-Facing Report** - key finding, supporting visualization, and plain-language summary for Dr. Sharma
2. **Part 2 - Technical Appendix** - method justification, model results, reproducible code links, and personal reflection

The standalone memo (`stat692-practice1_technical_report.Rmd`) is the detailed reproducible analysis referenced in the technical appendix.

## Requirements

- [R](https://cran.r-project.org/) (4.x recommended)
- [RStudio](https://posit.co/download/rstudio-desktop/) or another R Markdown-capable editor
- A LaTeX distribution (e.g. [TinyTeX](https://yihui.org/tinytex/)) for PDF output

Install the required R packages:

```r
install.packages(c("palmerpenguins", "tidyverse", "nnet", "knitr", "kableExtra", "ggplot2"))
```

## Rendering the Reports

From the project directory in R:

```r
# Course template submission
rmarkdown::render("stat692-practice1_final_report.Rmd")

# Full standalone analysis memo
rmarkdown::render("stat692-practice1_technical_report.Rmd")
```

Or open either `.Rmd` file in RStudio and click **Knit** to produce the corresponding PDF.

## Methods

1. **Data** - Palmer Penguins dataset; records with missing bill or flipper length are dropped.
2. **Exploratory analysis** - scatter plot of bill length vs. flipper length with the unidentified specimen marked.
3. **Classification** - multinomial logistic regression (`nnet::multinom`) using bill length and flipper length as predictors.
4. **Output** - species membership probabilities and a written recommendation.

## Author

Tran Quoc Bao Dang - Texas A&M University
