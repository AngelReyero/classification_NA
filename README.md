# Linear Classifiers Adapted to Missing Values

This repository compares adapted linear classifiers for handling missing values, specifically **Perceptron, Logistic Regression, and Linear Discriminant Analysis (LDA)**. Two main approaches are considered for adapting to missing data: **imputation methods** and **pattern-by-pattern methods**.

## Approaches to Handling Missing Values

### 1. Imputation Methods
- **Constant imputation**: Replacing missing values with a fixed value (e.g., 0).
- **Iterative imputation**: Using `IterativeImputer` from Scikit-learn to estimate missing values.

### 2. Pattern-by-Pattern Methods
- These methods decompose the **Bayes classifier** for each missingness pattern, training a separate classifier for each observed pattern.
- In the **LDA setting**, this decomposition allows leveraging distributional assumptions:
  - When missingness is **not informative**, it is possible to average over all observed data.
  - When missingness is **informative**, it is possible to only estimate the most frequently observed patterns.

## Experimental Analysis
Multiple experiments are conducted to analyze:
- **Convergence rates** and **robustness** to misspecifications in the joint distribution and missingness model.
- The impact of **correlation between input covariates**.
- The effects of **signal-to-noise ratio, missingness probability, and dimensionality**.

## Reference
For more details, refer to the paper:  
[https://arxiv.org/abs/2405.09196](https://arxiv.org/abs/2405.09196)


