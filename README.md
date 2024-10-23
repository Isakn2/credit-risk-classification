# Credit Risk Analysis

## Overview of the Analysis

This analysis aims to predict credit risk by evaluating loan statuses as either healthy (low risk) or high risk (default-prone) using a logistic regression model. By applying machine learning techniques, we can assess the likelihood of a loan defaulting, thus helping lenders make informed decisions. 

The logistic regression model uses various loan features to predict whether a loan will be high risk (1) or healthy (0). This analysis is part of a broader effort to leverage data science tools for improving financial risk assessments.

## Results

The model was trained using a logistic regression algorithm on a dataset of loan information. The following performance metrics were obtained:

- **Accuracy**: The overall accuracy of the model was **99%**, indicating the model correctly predicts whether a loan is high risk or healthy in the vast majority of cases.
  
- **Precision**: 
  - Class 0 (healthy loans): **1.00** 
  - Class 1 (high-risk loans): **0.84**
  - This means that for healthy loans, the model is nearly perfect in predicting them correctly. However, for high-risk loans, there's an 84% chance that a loan flagged as high-risk actually is.

- **Recall**: 
  - Class 0 (healthy loans): **0.99**
  - Class 1 (high-risk loans): **0.94**
  - This shows the model is slightly better at catching high-risk loans (94% recall) but still almost perfect in recalling healthy loans (99%).

- **F1-Score**: 
  - Class 0 (healthy loans): **1.00**
  - Class 1 (high-risk loans): **0.89**
  - The F1 score combines both precision and recall, indicating the model has strong performance in both identifying healthy loans and detecting high-risk loans, but slightly weaker in the latter due to class imbalance.

## Summary and Recommendation

The logistic regression model shows strong overall performance with a 99% accuracy rate. It performs exceptionally well in identifying healthy loans (class 0), with precision and recall scores nearing perfection. However, it slightly struggles in accurately classifying high-risk loans (class 1), as seen by the lower precision for this class. This is likely due to the class imbalance—there are far fewer high-risk loans than healthy ones, which affects the model’s ability to generalize for the minority class.

Despite this, the model still demonstrates a high recall rate (94%) for high-risk loans, meaning it correctly identifies the majority of loans that are likely to default. Based on this, I recommend the model for use in credit risk assessments with an emphasis on further refinement or supplementary methods (e.g., oversampling, cost-sensitive learning) to improve performance on high-risk loan predictions.