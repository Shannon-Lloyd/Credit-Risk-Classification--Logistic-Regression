# credit-risk-classification
Supervised Machine Learning

# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

### Explain the purpose of the analysis.
The purpose of this is to see how well the logistical regression model can predict the credit risk of potential lenders.

### Explain what financial information the data was on, and what you needed to predict.
The target value that we are using is the loan status. The features used to predict the target are loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks,and total_debt

### Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The value counts lets us know how large the data set is before splitting into training and testing sets so we can have an idea of how the data is divided when we compare it to the confusion matrix.  It also lets us know how balanced our data set is. With this data set we can see that 75036 healthy loans vs 2500 high risk loans should produce results that are far less accurate for high risk loans since there is such a large difference in the amount of data.

### Describe the stages of the machine learning process you went through as part of this analysis.
 * Decide what you want to predict and seperate that out as the target data to create a label. Remove the target data from the rest of the data to declare the features used to predict the target.
 * Split the target and feature data into training and testing sets.
 * Create a logistic regression model and fit the training data to it.
 * Use the trained model to make predictions
 * Use balanced accuracy score to compare the test data to the predictions since the data is very heavily weighted towards healthy loans
 * Generate a confusion matrix to see the true positive, false positive, false negative, and true negative results.
 * Compare the models predictions to the test data in a classification report to evaluate the model for precision, recall, f1-score, accurracy, macro avg, and weighted avg. 

### Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
We only used Logistical Regression which is widely used for classification problems with binary values.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

### Machine Learning Model 1:
 #### Description of Model 1 Accuracy, Precision, and Recall scores. 
      *  Acurracy is 99% based on the results of testing on a data set of 19384 values.
      *  Precision is 100% for predicting healthy loans with a test data set of 18765 healthy loans and 85% on high risk loans with a test data set of only 619
      *  Recall is 99% for healthy loans and 91% for high risk loans so it is more accurate at recording true positives for healthy loans than high risk loans
 



### Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
 This is omitted per Brett Payne
 Per Joanna,
 Brett mentioned in the instructor/TA channels the
 "Predict a Logistic Regression Model with Resampled Training Data" 
 section in the notebook is not required. 
 It used to be taught in this class but isn't anymore.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

## Regarding Model 1:
The logistic regression model has a precission of 100%  on predicting healthy loans but only 85% on predicting high risk loans. This can be seen in the recall and f1-scores which also have lower values for the high risk loans vs the healthy loans. Therefore all of the loans predicted as healthy are healthy but 15% of the predicted high risk loans were actually healthy.  The low number of high risk loans tested (619) could reduce the precision of the model for high risk loans. Hopefully as more data is gathered the model will improve on it's ability to predict high risk loans.

## Regarding Model 2:
 This is omitted per Brett Payne
 Per Joanna,
 Brett mentioned in the instructor/TA channels the
 "Predict a Logistic Regression Model with Resampled Training Data" 
 section in the notebook is not required. 
 It used to be taught in this class but isn't anymore.

If you do not recommend any of the models, please justify your reasoning.
With an overall accuracy of 99% would not recommend model 1, but would point out that there will be loans incorrectly predicted as high risk and therefore losing potential lenders.
