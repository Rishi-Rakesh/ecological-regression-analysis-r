# ecological-regression-analysis-r

Statistical analysis of goldcrest chick calling intensity using R,
tidyverse, regression, GAMs, and mixed-effects models.

## Project Overview

This project investigates whether goldcrest chick calling intensity is associated with food availability, parent sex, foraging duration, and nest size. The response variable, AveChickCalls, represents the average number of calls per chick during the 15 minutes before a parent returns to the nest. The dataset contains 599 observations across multiple nests. The analysis combines exploratory visualisation, linear regression, interaction modelling, generalised additive models, and linear mixed-effects modelling to account for repeated observations from the same nest.

## Research Question

Which ecological and parental factors are associated with the calling
intensity of goldcrest chicks?

## Methods

- Exploratory data analysis with `ggplot2`
- Distribution and group comparisons
- Interaction analysis
- Linear regression
- LOESS-versus-linear comparisons
- Generalised additive modelling with `mgcv`
- Linear mixed-effects modelling with `lme4`
- AIC, BIC, and likelihood-ratio model comparisons
- Marginal effect plots

## Key Findings

- Calling intensity was higher under scarce food conditions.
- The relationship between food availability and parent sex was
  investigated using an interaction term.
- Foraging duration and nest size were evaluated as continuous predictors.
- Observations from the same nest were modelled using a random intercept.
- Between-nest variability was considered when selecting the final model.

## Repository Contents

```text
.
├── README.md
├── chick_calling_analysis.Rmd
├── chick_calling_analysis.html
├── data/
│   └── chicks.rda
├── figures/
│   ├── response_distribution.png
│   ├── food_parent_interaction.png
│   ├── continuous_effects.png
│   └── nest_variation.png
└── .gitignore
```

## Reproducibility

The analysis was conducted in R using:

- tidyverse
- ggplot2
- patchwork
- broom
- kableExtra
- modelr
- lme4
- mgcv
- scales

To reproduce the analysis, open the `.Rmd` file in RStudio and knit
the document to HTML.

## Limitations

The data are observational, so the results describe associations rather
than causal effects. The response is bounded below by zero, and the
Gaussian error assumption may not fully represent its distribution.
The mixed model includes a random intercept for nest but does not model
random slopes or possible temporal autocorrelation.
