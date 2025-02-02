# Module 12: Credit Risk Classification

## Overview of the Analysis

The purpose of this analysis is to build a supervised machine learning model that can identify the creditworthiness of borrowers by predicting if a loan is healthy (class 0) or high-risk (class 1). The analysis was conducted using data from a lending data CSV file. The CSV file contains 77,536 lines of financial data which specifically focused on loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. 

### The stages of the machine learning process

- Importing of libraries and dependencies 
- Splittingi the Data into Training and Testing Sets 
    1. Splitting data into labels and features assigning the loan status (healthy or high-risk) as labels and the remaining seven columns as features
    2. The data was then split into training and testing datasets
- The analysis tool used is Logistic Regression (LR).  LR, as a binary classifier, provides statistical method for predicting binary outcomes from the two loan classes, healthy (class 0) or high-risk (class 1)
- The model was then fit with the training data
- Predictions were made with the test data
- The model’s performance was evaluated using accuracy, precision, and recall scores

### Results

***healthy loan (0) evaluation:**

- **Precision**: 1.00 – The model is perfect in predicting healthy loans (no false positives)

- **Recall**: 1.00 – The model also correctly identifies all healthy loans (no false negatives)

- **F1-Score**: 1.00 – Since both precision and recall are perfect, the F1-score is also 1.00

***high-risk loan (1) evaluation:** 

- **Precision**: 0.87 – When the model predicts a loan as high-risk, it's correct about 87% of the time

- **Recall**: 0.95 – The model correctly identifies 95% of the actual high-risk loans

- **F1-Score**: 0.91 – The balance between precision and recall for high-risk loans is 0.91, which is a good value, although it's slightly lower than the perfect score for healthy loans

### Assessment of the Metrics:

- **Accuracy**: 0.99 – The model is highly accurate, correctly classifying 99% of all instances

- **Macro Average**: This is the average of precision, recall, and F1-score across all classes, without taking class imbalance into account

  - Precision: 0.94
  - Recall: 0.97
  - F1-Score: 0.95

- **Weighted Average**: This accounts for the class imbalance by weighting the scores by the number of instances in each class which in this case the model is more influenced by the healthy loans-the larger class

  - Precision: 0.99
  - Recall: 0.99
  - F1-Score: 0.99

### Summary:

- The model seems to perform very well on healthy loans (perfect precision, recall, and F1-score in class 0), but it performs a bit less well on high-risk loans. Precision for predicting class 1 is 87.3%, while recall for class 1 is 94.8%, indicating that the model is good at detecting positives, though there's room to improve in terms of how many of the predicted positives are truly positive (since precision is lower than recall). This suggests the model might be a little more conservative when predicting high-risk loans and may miss some, though it still has a high recall (95%) for those loans.

- Given that the class imbalance is likely (healthy loans significantly outnumber high-risk loans), the model might be biased towards predicting the larger class (healthy loans). This would explain the high accuracy but also why there is a noticeable gap in precision between the two classes.

- The model is performs well, with high accuracy (~99.5%). I recommend the model for use by the company.
