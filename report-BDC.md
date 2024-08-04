# Module 12 Report - Credit Risk Classification

## Overview of the Analysis

- The purpose of this analysis completed was to provide predictions on whether a loan is high-risk('1') or healthy('0') based on a number of finacial measures related to the borrower.

- The finacial measures utilized were a borrower's loan size, interest rate, income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. These values helped to assess the risk associated with a loan.

- Essentially, the value we were trying to predict was the target variable 'loan_status' which indicated which classification category the loan fell into - either 'Healthy' or 'High-risk'. The data showed 75,036 instances of Healthy Loans and 2,500 instances of High-Risk Loans.

- The stages of the Machine Learning Process used were as follows:

  1. Data Preprocessing:

     - Identified the target variable and features.
     - Checked for data types and null values (none found).

  2. Model Selection:

     - Chose Logistic Regression for binary classification due to its simplicity and interpretability.

  3. Data Splitting:

     - Split the data into training and testing sets with an 80-20 split.

  4. Model Training:

     - Trained the logistic regression model on the training data.

  5. Model Evaluation:
     - Evaluated the model using a confusion matrix and classification report.

- Using the `LogisticRegression` Algorithm

  1. The Logistic regression algorithm calculates a linear combination of the input values, assigning weight to each feature and computing the weighted sum + bias.

  2. Then, the linear function is passed through a sigmoid function which classifies the output to a probability between 0 and 1.

  3. Once this is done, the model is training and testing, with an 80-20 split.

  4. Once the model is used for predictions, conclusions are drawn from the readily-interpretable data that has been produced.

  ## Results

- Data from the model based on classification report and confusion matrix:
  - Accuracy: 99%
  - Precision:
    - Class 0 (Healthy Loan): 1.00
    - Class 1 (High-Risk Loan): 0.86
  - Recall:
    - Class 0 (Healthy Loan): 1.00
    - Class 1 (High-Risk Loan): 0.91
  - F1-score:
    - Class 0 (Healthy Loan): 1.00
    - Class 1 (High-Risk Loan): 0.88
  - Support:
    - Class 0: 15,001 instances
    - Class 1: 507 instances

## Summary

The logistic regression model performed exceptionally well for predicting healthy loans (0) with 100% precision, recall, and F1-score. This indicates that the model almost always correctly identified healthy loans and made very few mistakes regarding false positives or false negatives.

For high-risk loans (1), the model is also good, but doesn't perform as well as healthy loans, achieving a precision of 0.86 and a recall of 0.91. This which indicated it is generally effective at identifying high-risk loans but does have some false positives and false negatives. The F1-score of 0.88 shows a good balance between precision and recall.

Given the results, the logistic regression model is recommended for use, given its high accuracy and ability to correctly predict high-risk loans with reasonably high precision and recall. But the class imbalance may have swayed the model towards predicting healthy loans more accurately. If predicting high-risk loans accurately is more critical, recall and precision for the class should be improved.
Given the results, the logistic regression model is suitable for this classification task, especially given its high accuracy and ability to correctly predict high-risk loans with reasonably high precision and recall.
