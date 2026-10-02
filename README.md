# Practical Statistics for Data Scientists

Code reproduction and chapter summaries for **_Practical Statistics for Data Scientists_** (Peter Bruce, Andrew Bruce & Peter Gedeck, O'Reilly).

Each chapter has its own Jupyter notebook in this repository containing:

1. a **chapter summary**,
2. a **theoretical explanation** of every concept (definitions, formulas, intuition, when to use it),
3. the **reproduced Python code** (pandas, SciPy, statsmodels, scikit-learn, XGBoost ...) with plots and outputs,
4. **key takeaways**.

## Chapters

| # | Notebook | Topic |
|---|----------|-------|
| 1 | [ch01_exploratory_data_analysis](ch01_exploratory_data_analysis.ipynb) | Exploratory Data Analysis |
| 2 | [ch02_data_and_sampling_distributions](ch02_data_and_sampling_distributions.ipynb) | Data and Sampling Distributions |
| 3 | [ch03_statistical_experiments_and_significance_testing](ch03_statistical_experiments_and_significance_testing.ipynb) | Statistical Experiments and Significance Testing |
| 4 | [ch04_regression_and_prediction](ch04_regression_and_prediction.ipynb) | Regression and Prediction |
| 5 | [ch05_classification](ch05_classification.ipynb) | Classification |
| 6 | [ch06_statistical_machine_learning](ch06_statistical_machine_learning.ipynb) | Statistical Machine Learning |
| 7 | [ch07_unsupervised_learning](ch07_unsupervised_learning.ipynb) | Unsupervised Learning |

## Chapter overviews

### Chapter 1 - Exploratory Data Analysis
EDA is the first step of every project: look at the data before modelling. The chapter introduces numeric vs. categorical data and the rectangular (data-frame) format, then the key summaries: **estimates of location** (mean, trimmed mean, weighted mean, median) and **variability** (variance, standard deviation, MAD, IQR, percentiles), emphasising **robust** statistics that are not distorted by outliers. It shows how to explore distributions (boxplots, histograms, density plots), binary/categorical data (mode, expected value, bar charts), **correlation** (matrix, heatmap, scatterplots) and relationships between two or more variables (hexbin, contour plots, contingency tables, violin plots, conditioning/facets).

### Chapter 2 - Data and Sampling Distributions
Data are usually a sample from a larger population. The chapter covers random vs. biased sampling, then the **sampling distribution** of a statistic, the **Central Limit Theorem** and the **standard error**. The **bootstrap** is presented as a distribution-free way to estimate uncertainty and build **confidence intervals**. It finishes with the distributions every data scientist should know: normal (and QQ-plots), long-tailed, Student's t, binomial, chi-square, F, Poisson, exponential and Weibull.

### Chapter 3 - Statistical Experiments and Significance Testing
How to design experiments (A/B tests) and decide whether an observed difference is real or chance. Covers hypothesis testing (null/alternative), **permutation (resampling) tests**, **p-values** and significance levels, t-tests, the **multiple-testing** problem, degrees of freedom, **ANOVA / F-statistic**, **chi-square** and Fisher's exact tests, **multi-arm bandits**, and **power & sample size**.

### Chapter 4 - Regression and Prediction
Predicting a numeric outcome. Starts with **simple linear regression** (least squares), then **multiple regression** (RMSE, RSE, R², t-statistics, model selection with AIC/stepwise), prediction and confidence/prediction intervals, **factor variables** (dummy coding, many-level factors), interpreting coefficients (correlated predictors, multicollinearity, confounders, **interactions**), **regression diagnostics** (outliers, leverage, Cook's distance, heteroskedasticity, partial residual plots), and non-linear models: **polynomial, spline regression and GAMs**.

### Chapter 5 - Classification
Predicting a categorical outcome using probabilities and a cutoff. Methods: **naive Bayes**, **discriminant analysis (LDA)** and **logistic regression** (log-odds, odds ratios, GLMs). Evaluation goes beyond accuracy: **confusion matrix, precision, recall, specificity, ROC/AUC and lift**. The chapter closes with **strategies for imbalanced data**: undersampling, oversampling, weighting, SMOTE and cost-based cutoffs.

### Chapter 6 - Statistical Machine Learning
Flexible, data-driven prediction methods: **K-nearest neighbours**, **decision trees** (recursive partitioning, Gini/entropy, pruning), **bagging and random forests** (OOB error, variable importance) and **boosting / XGBoost** (learning rate, regularisation, overfitting), plus **hyperparameter tuning with cross-validation**.

### Chapter 7 - Unsupervised Learning
Finding structure without a labelled outcome: **Principal Components Analysis**, **K-means**, **hierarchical clustering** (linkage, dendrograms), **model-based clustering** with Gaussian mixtures (EM, BIC), and the practical issues of **scaling** and **categorical variables** (Gower's distance).

## How to run

```bash
pip install -r requirements.txt
jupyter notebook
```

Each notebook is self-contained: the datasets are the ones published by the book's authors at
[gedeck/practical-statistics-for-data-scientists](https://github.com/gedeck/practical-statistics-for-data-scientists/tree/master/data),
and a small helper at the top of every notebook downloads each file the first time it is needed (internet connection required) into a local `data/` folder.
Use *Kernel -> Restart & Run All*.
## Notes

* Code follows the book's examples, updated for current library versions (e.g. `statsmodels`, `scikit-learn`, `pandas 2`). Some small adaptations are marked in the notebooks (for instance, the imbalanced-data demo in Chapter 5 builds its imbalance from the loan data).
* The notebooks are saved **without outputs**; run them to regenerate the results and figures.

## Reference

Bruce, P., Bruce, A., & Gedeck, P. (2020). *Practical Statistics for Data Scientists* (2nd ed.). O'Reilly Media.
