# Module 12 Report Template

The factors considered inthe analysis are:

* size of the loan
* borrower income
* interest rate
* DTI ratio
* Number of accounts held by borrower
* Derogatory marks on the borrower
* debt

The dataset (77,536 data points) was split into training and testing sets. The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. Logistic Regression Model 1 was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.

This intial model was drawing from a dataset that had 75,036 low-risk loan data points and 2,500 high-risk data points. To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module from imbalanced-learn. This generated 56,277 data points for both low-risk (0) and high-risk (1) loans, based on the original dataset.

The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). The purpose of Logistic Regression Model 2 was to determine whether a loan to the borrower in the testing set would be low- or high-risk. The results are summarized below.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * 93% Precision. This is an average between low-risk loans and high-risk loans. low-risk being 100% andhigh being 87%
  * 94% Accuracy
  * 95% Recall. An average between 100% low-risk and 89% high-risk predictions.

* Machine Learning Model 2:
  * 93% precision. Average between low-risk 100% and 87% high-risk
  * 100% Accuracy
  * 100% Recall

## Summary

Model 2 predicted more false positives, meaning low-risk when the actual was high-risk based on confusion matrices. However, model 2 is less likely to predict false negatives.

Model 2 had fewer false predictions and would be the best one to use however neither model scored above 90% precision. That said, I would suggest model 2 as it predicted less false positives.


