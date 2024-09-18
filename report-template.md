# Module 12 Report Template

## Overview of the Analysis

* The goal of this analysis was to assess the creditworthiness of borrowers using a logistic regression model, based on historical loan data. The dataset included financial information such as loan status (0 for healthy loans and 1 for high-risk loans) and various details about the borrowers and their loans.

* The dataset included financial information from loans issued by a peer-to-peer lending service. Important data points were the loan status, showing if a loan is healthy (0) or high-risk (1), and various features about each loan and borrower. These features likely included things like loan amount, annual income, debt-to-income ratio, and credit score.

* The main variable we wanted to predict was the loan status, which shows if a loan is healthy or high-risk. The loan status is a binary variable, meaning it has two values:

  - `0` for a healthy loan, meaning it will likely be repaid without default.
  - `1` for a high-risk loan, meaning there’s a higher chance of default.

Along with this target variable, the dataset had other features about the loans and borrowers, like loan amount, borrower income, credit score, and debt-to-income ratio. These features helped the model predict if a loan would be healthy or high-risk.

* The machine learning process for this analysis included the following main steps:

  **Data Preprocessing**:
  - The data was loaded into a Pandas DataFrame and split into two parts: features (X) and the target variable (y), which is the loan status.
  - The dataset was then split into training and testing sets using `train_test_split` to ensure the model could be trained and tested properly.

  **Model Training**:
  - A logistic regression model was created, and the training data was used to fit the model. Logistic regression was chosen because it works well for binary classification problems like predicting whether a loan is healthy or high-risk.

  **Model Prediction**:
  - Once the model was trained, it was used to make predictions on the testing data. These predictions were compared to the actual loan statuses to see how well the model performed.

  **Model Evaluation**:
  - The model's performance was measured using accuracy, precision, recall, and the F1-score. A confusion matrix was also created to show the number of correct and incorrect predictions for both healthy and high-risk loans.

These steps made sure the model was trained and tested effectively, giving a clear idea of how well it could predict loan risk.

* In this analysis, we used `LogisticRegression`, a common algorithm for binary classification tasks. We chose logistic regression because it’s good at predicting binary outcomes, like whether a loan is healthy (0) or high-risk (1).

We also used the `train_test_split` function to divide the data into training and testing sets. This way, the model could be trained on one part of the data and tested on another, helping to avoid overfitting. After training the model, we evaluated its performance using accuracy, precision, recall, and F1-score. We also created a confusion matrix to see how well the model predicted both healthy and high-risk loans.

## Results

### Machine Learning Model 1: Logistic Regression

* **Accuracy**: 99%
* **Precision**:
    - **Healthy loans (0)**: 1.00
    - **High-risk loans (1)**: 0.86
* **Recall**:
    - **Healthy loans (0)**: 0.99
    - **High-risk loans (1)**: 0.94
* **F1-Score**:
    - **Healthy loans (0)**: 1.00
    - **High-risk loans (1)**: 0.90

These metrics show that the model works very well for healthy loans, with almost perfect precision and recall. For high-risk loans, the model has a good balance between precision and recall, though the precision is a bit lower, but the recall is still strong.

## Summary

The logistic regression model performed very well, with a high overall accuracy of 99%. It was almost perfect at predicting healthy loans (0), with both precision and F1-scores of 1.00. For high-risk loans (1), the model also did well, with a precision of 0.86 and a recall of 0.94. This means the model is good at identifying high-risk loans, but sometimes it mistakenly classifies some healthy loans as high-risk.

Given its strong performance, the logistic regression model is recommended. It does a great job predicting healthy loans, and its performance on high-risk loans is also impressive, with a good balance between precision and recall.

Accurately predicting high-risk loans (minimizing false negatives) is very important in this case, as missing a high-risk loan could lead to financial losses. The model's high recall for high-risk loans (0.94) makes it well-suited for identifying loans that are likely to default.
