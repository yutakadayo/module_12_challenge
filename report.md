# Module 12 Report

## Overview of the Analysis

* This analysis is build to compare raw data and oversampled data.
* Original data contains loan profiles and risk of the loans.
* Variable `0` is lower risk loan and variable `1` is higher risk loan
* Since the data contains answers (0 and 1), it is practical to use supervised learning. In this analysis, Logistic Regression is choosed to perform the prediction.

## Results

* Logistic Regression - raw data
  * Accuracy Score: 0.952
  * Precision for `0` (low risk): 1.00
  * Recall for `0` (low risk): 0.99
  * Precision for `1` (high risk): 0.85 
  * Recall for `1` (high risk): 0.91



* Logistic Regression - Oversampled data
  * Accuracy Score: 0.993
  * Precision for `0` (low risk): 1.00
  * Recall for `0` (low risk): 0.99
  * Precision for `1` (high risk): 0.84 
  * Recall for `1` (high risk): 0.99

## Summary

* For `0` category, both prediction performed great.
* For `1` category, prediction with oversampled data performed better on recall. Since `1` category indicates "high risk loan", it is better to have higher score on recall instead of precision. 
  * `Recall = High risk loans / (High risk loans + high risk loans categorized as low risk)`
  * `Precision = High risk loans / (High risk loans + low risk loans categorized as high risk)`

If the purpose of application is to detect high risk loans, it would be better to use oversampled data to make prediction.
