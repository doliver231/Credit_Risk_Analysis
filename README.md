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

![Naive Random Oversampling](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/NaiveRandomOverSampling.png)

* Balanced Accuracy Score:
* Precision:
* Recall:
-----------------------------------------------------------------

### SMOTE Oversampling

![SMOTE](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/SMOTEOverSampling.png)

* Balanced Accuracy Score:
* Precision:
* Recall:
-----------------------------------------------------------------

### Cluster Centroid Undersampling

![Cluster Centroid](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/ClusterCentroidUnderSampling.png)

* Balanced Accuracy Score:
* Precision:
* Recall:
-----------------------------------------------------------------

### SMOTEENN Combination Resampling

![SMOTEENN](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/SMOTEENNCombination.png)

* Balanced Accuracy Score:
* Precision:
* Recall:
-----------------------------------------------------------------

### Balanced Random Forest Classification

![Balanced Random Forest](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForest.png)

* Balanced Accuracy Score:
* Precision:
* Recall:
-----------------------------------------------------------------

### Easy Ensemble AdaBoost Classification

![Easy Ensemble AdaBoost](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleAdaBoost.png)

* Balanced Accuracy Score:
* Precision:
* Recall:
-----------------------------------------------------------------

## Conclusion

While resampling can attempt to address imbalance, it does not guarantee better results. In terms of this dataset, we find that the best overall model to use is the "Easy Ensemble AdaBoost Classifier" because not only does it have a high accuracy score, but it also has the best precision and sensitivity (recall) especially in terms of correctly identifying high-risk applicants. Therefore, we would reccomend using this model to predict credit risk.

The one downside to this model is a high false positive rate meaning that of the applicants that are predicted to be high risk, only a small amount of them will actually be high risk. In this scenario though, it is better for the model to have greater senstivity than precision because the credit card company would rather wrongly classify low risk applicants as high risk, than have high risk applicants classified as low risk thus approving them for a credit card or loan they are unable to repay. Also, the credit card company can further narrow down and examine these potential high risk individuals later on outside of the machine learning scope.