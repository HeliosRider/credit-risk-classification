# Module 12: Credit Risk Classification

## Overview of the Analysis

The purpose of this analysis is to build a supervised machine learning model that can identify the creditworthiness of borrowers by predicting if a loan is healthy (class 0) or high-risk (class 1). The analysis was conducted using data from a lending data CSV file. The CSV file contains 77,536 lines of financial data which specifically focused on loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. 

### The stages of the machine learning process

- Importing of libraries and dependencies 
- Splitting the Data into Training and Testing Sets 
    1. Splitting data into labels and features assigning the loan status (healthy or high-risk) as labels and the remaining seven columns as features
    2. The data was then split into training and testing datasets
- The analysis tool used is Logistic Regression (LR).  LR, as a binary classifier, provides statistical method for predicting binary outcomes from the two loan classes, healthy (class 0) or high-risk (class 1)
- The model was then fit with the training data
- Predictions were made with the test data
- The model’s performance was evaluated using accuracy, precision, and recall scores

### Results

***healthy loan (class 0) evaluation:**

- **Precision** (1.00)
    The model is perfect in predicting healthy loans (no false positives)

- **Recall**: (1.00)
    The model correctly identifies all healthy loans (no false negatives)

- **F1-Score**: (1.00)
    Since both precision and recall are perfect, the F1-score is also 1.00

***high-risk loan (class 1) evaluation:** 

- **Precision** (0.87)
    The model is correct 87% of the time when prediciting loan's as high-risk

- **Recall** (0.95)
    The model correctly identifies 95% of the actual high-risk loans. Leaving a small percentage of high-risk loans it didn’t identify (5%).

- **F1-Score** (0.91)
    The balance between precision and recall slightly lower than the perfect score for healthy loans at 91%, which is a good value

### Assessment of the Metrics

- **Accuracy** (0.99)
    The model is highly accurate, correctly classifying 99% of all instances

- **Macro Average**: 
    The macro average is the average of the precision, recall, and F1-score across both classes, giving equal weight to both. The macro average is solid, with values close to 1

    - Precision: 0.94
    - Recall: 0.97
    - F1-Score: 0.95

- **Weighted Average**: 
    The Weighted Average takes into account the proportion of each class in the dataset. Since healthy loans are much more common, the weighted averages are very close to 1, which is expected

    - Precision: 0.99
    - Recall: 0.99
    - F1-Score: 0.99

### Summary

- The model seems to perform perfectly with the healthy loan class, but slightly less with the high-risk loan class, as indicated by the lower precision and recall. However, the overall performance remains quite strong

- Depending on the use case, the company may want to focus on improving recall for the high-risk loan class, especially if false negatives (missing high-risk loans) could lead to significant financial problems

- Overall results indicate that the model has performed well, evident by the high accuracy score of 99%. Based on the high accurracy score of the model, I deem the model a success and recommend it for use by the company
