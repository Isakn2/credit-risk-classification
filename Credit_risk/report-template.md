# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to evaluate credit risk by predicting whether a loan is high risk (likely to default) or healthy (low risk) using machine learning techniques. The dataset contains financial information related to lending, including features like loan amount, income level, and interest rates. Our goal is to predict the `loan_status` column, which indicates whether a loan is high risk (`1`) or healthy (`0`).

The `loan_status` variable has the following distribution:
- Healthy loans (`0`): **18,765** instances 
- High-risk loans (`1`): **619** instances
*Based on the confusion matrix*

This shows that the data has more healthy loans than high-risk loans. 

The machine learning process included the following steps:
- **Data Preprocessing**: The dataset was split into features (X) and labels (y). The features include all columns except `loan_status`, which is used as the label.
- **Splitting the Data**: The data was divided into training and testing sets using `train_test_split`.
- **Logistic Regression Model**: A logistic regression model was trained on the training data (`X_train` and `y_train`) to predict the loan status.
- **Model Evaluation**: The model's performance was evaluated using a confusion matrix and classification report, with key metrics like accuracy, precision, recall, and F1-score.

## Results

### Logistic Regression Model:
- **Accuracy**: The model achieved an overall accuracy of **99%**, indicating that it correctly predicts whether a loan is high risk or healthy in most cases.
- **Precision**:
  - Healthy loans (`0`): **1.00**
  - High-risk loans (`1`): **0.84**
- **Recall**:
  - Healthy loans (`0`): **0.99**
  - High-risk loans (`1`): **0.94**
- **F1-Score**:
  - Healthy loans (`0`): **1.00**
  - High-risk loans (`1`): **0.89**

The model performs exceptionally well in predicting healthy loans, with precision and recall scores close to 100%. It also shows strong performance in predicting high-risk loans, though slightly lower precision (84%) suggests some false positives.

## Summary

The logistic regression model demonstrates strong overall performance with a high accuracy score of **99%**. It performs best when predicting healthy loans (`0`), with precision, recall, and F1-scores all being perfect or near-perfect. For high-risk loans (`1`), the model still performs well, particularly in terms of recall (94%), meaning it identifies most high-risk loans correctly.

However, due to the imbalanced nature of the dataset (many more healthy loans than high-risk ones), the model struggles slightly in predicting high-risk loans, as shown by the lower precision (84%) for this class. This imbalance means there are more false positives for high-risk loans than for healthy ones.

### Recommendation:

The logistic regression model is recommended for use, particularly due to its high recall for high-risk loans (94%). This is crucial in financial risk assessment, as correctly identifying loans likely to default is often more important than minimizing false positives. However, additional strategies like handling class imbalance (e.g., using oversampling techniques or adjusting class weights) could further improve its performance in identifying high-risk loans.

