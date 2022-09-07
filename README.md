# Report on Credit Risk Resampling Analysis

## Overview of the Analysis

In this application, we performed credit risk analysis using supervised machine learning techniques.

The purpose of the analysis was to to build a model that can predict the creditworthiness of borrowers using a dataset of historical lending activity.

* For this analysis, we used a dataset of historical lending activity from a peer-to-peer lending services company. 

* We used a variable called loan_status to analyze and predict our outcomes. A "0" was used to indicate a loan that was paid back, and a "1" was used to indicate a loan that was defaulted on. Using the value_counts function on the loan_status column, we could determine that 75,036 loans were paid back, and 2,500 loans were defaulted.

* We used the model-fit-predict pattern to perform our analysis. First, we split the data into training and testing datasets by using `train_test_split` function. Then we fit a logistic regression model by using the training data (X_train and y_train). Finally, we evaluated the model’s performance by calculating the accuracy score of the model, generating a confusion matrix, and printing a classification report.

* We used the LogisticRegrssion module initially. Then, we used the RandomOverSampler module from the imbalanced-learn library to resample the data -- to transform our data so that the labels had an equal number of data points.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
