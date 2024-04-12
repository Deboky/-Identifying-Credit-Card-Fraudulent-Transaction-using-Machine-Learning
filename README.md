# Identifying Credit Card Fraudulent Transactions using Machine Learning

## Overview
This project utilizes machine learning techniques to identify fraudulent transactions from credit card data, aiming to enhance financial security by detecting and preventing potential fraud.

## Data Selection

The credit card dataset used for this analysis is sourced from [Kaggle](https://www.kaggle.com/), a platform hosting various open-source datasets. Due to confidentiality, most features in the dataset are anonymized (labeled V1 to V28), with the exceptions of `Time` and `Amount`.

- **Time**: Time elapsed between the current transaction and the first transaction in the dataset (in seconds).
- **Amount**: Transaction amount.

## Data Pre-processing

Efficient data pre-processing is crucial in any machine learning workflow:

- **Handling Missing Values**: No missing values were detected in the dataset.
- **Removing Duplicates**: Duplicate entries were identified and removed to ensure data quality.
- **Feature Scaling**: Utilized `ColumnTransformer` from Scikit-Learn to scale `Time` and `Amount` features independently, facilitating uniform data treatment across all inputs.

Refer to the [Scikit-Learn documentation](https://scikit-learn.org/stable/modules/generated/sklearn.compose.ColumnTransformer.html) for more details on `ColumnTransformer`.

## Data Transformation

To address class imbalance:

- **SMOTE (Synthetic Minority Over-sampling Technique)**: This method is used to generate synthetic samples from the minority class (fraudulent transactions) by interpolating between existing samples.

## Model Evaluation

The machine learning models were evaluated using the following metrics:

- **Accuracy**: Proportion of total correct predictions.
- **Precision**: Proportion of positive identifications that were actually correct.
- **Recall**: Proportion of actual positives that were identified correctly.
- **F1 Score**: Harmonic mean of Precision and Recall, providing a balance between them.

### Confusion Matrix Terms

- **True Positive (TP)**: Fraudulent transactions correctly identified as fraudulent.
- **False Positive (FP)**: Legitimate transactions incorrectly identified as fraudulent.
- **False Negative (FN)**: Fraudulent transactions incorrectly identified as legitimate.
- **True Negative (TN)**: Legitimate transactions correctly identified as legitimate.

## Comparison of Machine Learning Algorithms

- **Random Forest, XGBoost, and Decision Tree Classifier**: All models achieved an accuracy of 0.99.
- **Precision**: Random Forest outperformed other models, indicating a higher relevance rate of the results.
- **Recall**: Logistic Regression showed the highest recall, indicating a lower rate of false negatives.
- **F1 Score**: Highest for the Random Forest Classifier, signifying superior overall performance.

## Conclusion

The Random Forest Classifier demonstrates exceptional effectiveness in detecting fraudulent transactions, surpassing other models in both accuracy and F1 score. This project highlights the potential of machine learning in enhancing transaction security and preventing financial fraud.

