MR-BRT
================
Wei-Ming Jiang
July 17, 2024

## Introduction

- MR-BRT (Meta-regression with Bayesian priors, Regularization and
  Trimming) is a meta-regression tool created by Sasha and Peng,
  refactored for GBD 2020.

- Meta-regression of all sorts (e.g. COVID analysis, GBD,
  cost-effectiveness, etc.).

- The R package mirrors the syntax of the Python package; use `help()`
  for R documentation and `py_help()` for Python documentation.

- Functions: `MRData` formats the data, `MRBRT` and `MRBeRT` are for
  running models, and `predict` is for making predictions.

- For uncertainty, `create_draws` uses fit-refit (slower) and
  `core$other_sampling$sample_simple_lme_beta` uses asymptotic
  statistics (faster but only accurate for certain models).

## Similarities with other R packages

- Think of MR-BRT as a combination of…

  - Linear regression like `lm()` – not `glm()`

  - Mixed models with `lme4`

  - Meta-analysis with `metafor`

  - Splines with `gam`

  - Bayesian priors like `INLA`

- Also includes:

  - “Ensemble knots” for splines

  - Outlier trimming and automated covariate selection

  - “The ratio model” for comparing exposure ranges

  - Bayesian spline cascade

## Reference

1.  <https://rpubs.com/rsoren/587724>

2.  <https://rpubs.com/rsoren/mrbrt_gbd2021>

3.  <https://ihmeuw-msca.github.io/>
