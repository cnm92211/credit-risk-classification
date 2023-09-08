

## Overview of the Analysis

### Purpose of the Analysis
The purpose of this exercise is to assess the creditworthiness of borrowers. The study uses historical lending data as the primary data source. Utilizing machine learning techniques, the exercise aims to create a predictive model that can accurately identify the risk associated with two types of loans: "healthy" (`0`) or "high-risk" (`1`).

### Financial Information
The dataset is composed of a vast array of financial metrics and attributes of borrowers. The predictions in the models will primarily focus on the "loan_status" variable.

### Variables
- The `loan_status` column contains the labels:
  - 0: Healthy loan
  - 1: High-risk loan

### Stages and Methods
The machine learning process involved the following stages:
1. Data Preparation: Reading the data, splitting into features (X) and labels (y).
2. Data Splitting: Dividing the dataset into training and testing sets.
3. Model Training: Using Logistic Regression to fit the training data.
4. Model Evaluation: Analyzing performance using metrics like accuracy, precision, and recall.

## Results

### Logistic Regression Model with Original Data
- **Accuracy**: 99%
- **Precision**: 
  - High-risk: 1.00
  - Low-risk: 0.87
- **Recall**: 
  - High-risk: 1.00
  - Low-risk: 0.89

### Logistic Regression Model with Oversampled Data
- **Accuracy**: 100%
- **Precision**: 
  - High-risk: 1.00
  - Low-risk: 0.87
- **Recall**: 
  - High-risk: 1.00
  - Low-risk: 1.00

## Summary

### Best Performing Model
The second model using oversampled data seemed to be the most accurate. When compared to the first iteration, it improved accuracy and recall for the smaller class (i.e., the High-Risk Loan, or 1, class) without lowering it for the larger class (i.e., the 'Healthy Loan", or 0 class). 

### Problem-Specific Performance
Given the nature of credit risk, it is critical to correctly identify high-risk loans (`1`s) to mitigate potential financial loss. A model that routinely passed high risk loan as a healthy loan could have catastrophic results for a financial institution. In this instance, the higher recall scores for high-risk loans in the oversampled model makes it ideal.
### Recommendation
I would recommend the Logistic Regression Model with oversampled data for predicting the credit risk due to its high accuracy and recall scores for high-risk loans. However, I would also recommend further testing of the model to ensure that the accuracy and recall scores are consistent.
