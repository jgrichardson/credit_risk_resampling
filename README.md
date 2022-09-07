# Report on Credit Risk Resampling Analysis

## Overview of the Analysis

In this application, we performed credit risk analysis using supervised machine learning techniques.

The purpose of the analysis was to to build a model that can predict the creditworthiness of borrowers using a dataset of historical lending activity.

* For this analysis, we used a dataset of historical lending activity from a peer-to-peer lending services company.

* We used a variable called loan_status to analyze and predict our outcomes. A "0" was used to indicate a loan that was paid back, and a "1" was used to indicate a loan that was defaulted on. Using the value_counts function on the loan_status column, we could determine that 75,036 loans were paid back, and 2,500 loans were defaulted.

* We used the model-fit-predict pattern to perform our analysis. First, we split the data into training and testing datasets by using `train_test_split` function. Then we fit a logistic regression model by using the training data (X_train and y_train). Finally, we evaluated the model’s performance by calculating the accuracy score of the model, generating a confusion matrix, and printing a classification report.

* We used the LogisticRegrssion module initially. Then, we used the RandomOverSampler module from the imbalanced-learn library to resample the data -- to transform our data so that the labels had an equal number of data points.

## Results

Machine Learning Model 1 (Using Baseline Data):

  * The balanced accuracy score of our initial work was 99.28%.
  
  * The precision and the recall for the 0 class (the "healthy loan" transactions) was much better than that for the 1 class (the "high risk loan" transactions).
  
  * This was in part due to the fact that our initial data was imbalanced -- with a much higher percentage of healthy loans than hig risk loans.


Machine Learning Model 2 (Using Resampled Data):

* The balanced accuracy score of our resampled data was 99.34% (similar to the first analysis).

* The precision of the resampled analysis was roughly the same as the initial analysis.

* The recall for the resampled analysis for the 1 class (the "high risk loan" transactions) was substantially improved over the initial analysis (99% instead of 90%).

## Summary

* The resampled analysis performed much better. By resampling the data to produce the same number of data points between the 0 class and 1 class loans, we improved the recall.

* Performance does depend on the problem we are trying to solve -- it is more important to predict the `1`'s (the high risk loans) than it is to predict the `0`'s? (the healthy loans) -- due to the capital risk to the lender of being "wrong".

* We recommend using the second analysis/model to evaluate loans going forward for the lender.
