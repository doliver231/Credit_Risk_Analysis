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

* Balanced Accuracy Score: 0.6371 - The model accurately predicts credit risk 63.7% of the time.
* Precision: 100% of the predicted low risk applicants are actually low risk, but only 1% of the predicted high risk applicants are actually high risk.
* Recall: Only 61% of high risk applicants and 66% of low risk applicants are predicted correctly.
-----------------------------------------------------------------

### SMOTE Oversampling

![SMOTE](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/SMOTEOverSampling.png)

* Balanced Accuracy Score: 0.6252 - The model accurately predicts credit risk 62.5% of the time.
* Precision: 100% of the predicted low risk applicants are actually low risk, but only 1% of the predicted high risk applicants are actually high risk.
* Recall: Only 60% of high risk applicants and 65% of low risk applicants are predicted correctly.
-----------------------------------------------------------------

### Cluster Centroid Undersampling

![Cluster Centroid](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/ClusterCentroidUnderSampling.png)

* Balanced Accuracy Score: 0.5292 - The model accurately predicts credit risk 52.9% of the time.
* Precision: 100% of the predicted low risk applicants are actually low risk, but only 1% of the predicted high risk applicants are actually high risk.
* Recall: Only 61% of high risk applicants and 45% of low risk applicants are predicted correctly.
-----------------------------------------------------------------

### SMOTEENN Combination Resampling

![SMOTEENN](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/SMOTEENNCombination.png)

* Balanced Accuracy Score: 0.6204 - The model accurately predicts credit risk 62.0% of the time.
* Precision: 100% of the predicted low risk applicants are actually low risk, but only 1% of the predicted high risk applicants are actually high risk.
* Recall: Only 69% of high risk applicants and 55% of low risk applicants are predicted correctly.
-----------------------------------------------------------------

### Balanced Random Forest Classification

![Balanced Random Forest](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForest.png)

* Balanced Accuracy Score: 0.7878 - The model accurately predicts credit risk 78.8% of the time.
* Precision: 100% of the predicted low risk applicants are actually low risk, but only 4% of the predicted high risk applicants are actually high risk.
* Recall: Only 67% of high risk applicants and 91% of low risk applicants are predicted correctly.
-----------------------------------------------------------------

### Easy Ensemble AdaBoost Classification

![Easy Ensemble AdaBoost](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleAdaBoost.png)

* Balanced Accuracy Score: 0.9254 - The model accurately predicts credit risk 92.5% of the time.
* Precision: 100% of the predicted low risk applicants are actually low risk, but only 7% of the predicted high risk applicants are actually high risk.
* Recall: Only 91% of high risk applicants and 94% of low risk applicants are predicted correctly.
-----------------------------------------------------------------

## Conclusion

While resampling can attempt to address imbalance, it does not guarantee better results. In terms of this dataset, we find that the best overall model to use is the "Easy Ensemble AdaBoost Classifier" because not only does it have a high accuracy score, but it also has the best precision and sensitivity (recall), especially in terms of correctly identifying high-risk applicants. It is better for the model to have greater senstivity than precision because the credit card company would rather wrongly classify low risk applicants as high risk, than have high risk applicants classified as low risk, thus approving them for a credit card or loan they are unable to repay.

If we were to combine the techniques of resampling the dataset as well as use an ensemble classifier, the following results would occur:

![Suggestion](https://github.com/doliver231/Credit_Risk_Analysis/blob/main/Images/Suggestion.png)

Out of all the resampling models, the Naive Random Oversampling model had the highest balanced accuracy score (and not by much). If we resampled our training data using this model, and then fit the resampled data into the Easy Ensemble Adaboost Classifier to then make our predictions, we would achieve improvements on our evaluations. Our balanced accuracy score would rise to 92.85%. Our precision rate for the predicted high risk applicants that are actually high risk rose to 14%. As far as sensitivity (true positive rate), 89% of the high risk and 97% of the low risk applicants would be predicted correctly. This shows that if we balance our training sets before using our best ensemble classifier (Easy Ensemble Adaboost), we can achieve better predictions.