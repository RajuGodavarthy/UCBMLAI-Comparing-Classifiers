# Comparing Classifiers

## Overview

The goal of this project is to compare the performance of various classifiers in predicting whether a client will subscribe to a bank term deposit. The classifiers evaluated include:

- **K-Nearest Neighbor (KNN)**
- **Logistic Regression**
- **Decision Tree**
- **Support Vector Machines (SVM)**

The binary classification task aims to predict the subscription to a bank term deposit (variable `y`).

## Data

- **Source:** UCI Machine Learning Repository
- **Collection Method:** Portuguese banking institution
- **Format:** Results from multiple marketing campaigns conducted over the telephone related to bank products.
- **Features:** The dataset contains 16 features categorized as follows:
  - **Categorical:** 5
  - **Numerical:** 6
  - **Binary:** 3
  - **Date:** 2
- **Labels:** `y` - Indicates whether the client subscribed to a term deposit ("yes" or "no").

## Deliverables

1. **Understand the Data:** Perform initial data exploration and feature engineering.
2. **Baseline Performance:** Establish baseline performance metrics to benchmark the effectiveness of machine learning models.
3. **Model Building:** 
   - Build a basic Logistic Regression model and evaluate its accuracy.
   - Compare performance metrics across different models.
4. **Hyperparameter Tuning:** Improve model performance through hyperparameter tuning and grid search.

## Findings

### Baseline Performance Metrics

| Model               | Train Time (s) | Train Accuracy | Test Accuracy |
|---------------------|-----------------|----------------|---------------|
| Logistic Regression | 0.218932        | 0.883479       | 0.884721      |
| Decision Tree       | 1.055883        | 0.982010       | 0.841546      |
| KNN                 | 0.039255        | 0.904595       | 0.878439      |
| SVM                 | 330.471341      | 0.894332       | 0.885606      |

#### Explanation of Baseline Metrics

1. **Logistic Regression**
   - **Train Time:** 0.22 seconds
   - **Train Accuracy:** 88.35%
   - **Test Accuracy:** 88.47%
   - **Interpretation:** Logistic Regression has a relatively short training time and similar training and test accuracies, indicating good generalization.

2. **Decision Tree**
   - **Train Time:** 1.05 seconds
   - **Train Accuracy:** 98.20%
   - **Test Accuracy:** 84.15%
   - **Interpretation:** Decision Tree shows high training accuracy but a lower test accuracy, suggesting potential overfitting.

3. **KNN (K-Nearest Neighbors)**
   - **Train Time:** 0.04 seconds
   - **Train Accuracy:** 90.46%
   - **Test Accuracy:** 87.84%
   - **Interpretation:** KNN has good accuracy on both training and test data, but its training time is significantly longer.

4. **SVM (Support Vector Machine)**
   - **Train Time:** 330.47 seconds
   - **Train Accuracy:** 89.43%
   - **Test Accuracy:** 88.56%
   - **Interpretation:** SVM has the highest training time but performs well in both training and test accuracies, indicating effective generalization.

### Improved Model Performance Metrics

| Model               | Train Accuracy | Test Accuracy | Train Time (s) |
|---------------------|----------------|---------------|----------------|
| Logistic Regression | 0.883449       | 0.884632      | 4.03           |
| Decision Tree       | 0.886045       | 0.884544      | 10.02          |
| KNN                 | 0.885455       | 0.885517      | 303.15         |

#### Interpretation of Improved Performance Metrics

1. **Logistic Regression**
   - **Train Accuracy:** 88.3%
   - **Test Accuracy:** 88.5%
   - **Train Time:** 4.03 seconds
   - **Interpretation:** The model performs consistently across training and test datasets with efficient training time.

2. **Decision Tree**
   - **Train Accuracy:** 88.6%
   - **Test Accuracy:** 88.5%
   - **Train Time:** 10.02 seconds
   - **Interpretation:** The Decision Tree shows slightly better training accuracy compared to Logistic Regression, with reasonable training time.

3. **KNN (K-Nearest Neighbors)**
   - **Train Accuracy:** 88.5%
   - **Test Accuracy:** 88.6%
   - **Train Time:** 303.15 seconds
   - **Interpretation:** KNN offers the highest test accuracy but has a significantly longer training time, making it less practical for large datasets.

## Summary

- **Logistic Regression** provides a balanced approach with good performance and efficiency.
- **Decision Tree** has slightly better training accuracy but is slower compared to Logistic Regression.
- **KNN** offers the best test accuracy but at the cost of high training time, which might be impractical for larger datasets or time-sensitive applications.


---

This README file summarizes the project's objectives, data sources, findings from the analysis of Compare Classifiers.It provides a clear and structured overview for stakeholders to understand the project's outcomes and implications effectively.
