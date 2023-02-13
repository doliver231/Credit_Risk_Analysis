# Credit_Risk_Analysis

## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Credit card companies must evaluate new customer credit applications to assess the applicant's credit risk.

The goal of this project is to build a classification model that can predict if an applicant is likely to have low or high credit risk. The credit card company can use this information to determine whether or not an applicant should be approved. We will employ different techniques to train and evaluate models with unbalanced classes and evaluate models using resampling. We will then evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Resources

* Data Source: [Loan Statistics](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv)
* Jupyter Notebooks: [Resampling Model Algorithms](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb), [Ensemble Classifiers](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb)
* Software/Languages: Scikit-Learn Package, Imbalanced-Learn Package, Python, Jupyter Notebook

## Analysis

1. Balanced Accuracy Score - a measure of how likely a model is to label all predictions correctly when dealing with imbalanced data.
2. Precision - the quality of a positive prediction made by the model; it refers to the number of true positives divided by the total number of positive predictions.
3. Recall (Sensitivity) - true positive rate; the proportion of real positives that are correctly predicted out of all positive predictions that could be made by the model.

### Naive Random Oversampling

![Naive Random Oversampling]()

### SMOTE Oversampling

![SMOTE]()

### Cluster Centroid Undersampling

![Cluster Centroid]()

### SMOTEENN Combination Resampling

![SMOTEENN]()

### Balanced Random Forest Classification

![Balanced Random Forest]()

### Easy Ensemble AdaBoost Classification

![Easy Ensemble AdaBoost]()

## Conclusion