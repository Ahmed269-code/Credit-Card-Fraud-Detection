# Credit Card Fraud Detection Project

## Overview

This project focuses on detecting fraudulent transactions using a dataset from credit card transactions. The dataset contains information about transactions made by credit card users, including features derived from transaction details and anonymized variables.

## Dataset

The dataset has 284,807 transactions with 31 features, including:
- `Time`: Time of transaction
- `V1` to `V28`: Anonymized features derived from transaction data
- `Amount`: Transaction amount
- `Class`: Fraud label (0 for non-fraudulent, 1 for fraudulent)

## Data Exploration

1. **Descriptive Statistics**:
   - Non-fraudulent transactions (`Class` = 0) have a mean amount of $88.29, while fraudulent transactions (`Class` = 1) have a mean amount of $122.21.
   - The standard deviation of amounts is much higher for fraudulent transactions, indicating larger variations in transaction amounts.

2. **Class Distribution**:
   - The dataset is highly imbalanced, with a significant majority of non-fraudulent transactions compared to fraudulent ones. To address this imbalance, a sample of non-fraudulent transactions was used to match the number of fraudulent transactions.

## Data Preprocessing

- **Normalization**: Data was normalized to ensure that all features contribute equally to the model training.
- **Balancing**: Non-fraudulent transactions were downsampled to create a balanced dataset for model training.

## Model Training

A Support Vector Machine (SVM) with a linear kernel was used to classify transactions as fraudulent or non-fraudulent. The model was trained on a balanced dataset, and the following metrics were evaluated:

- **Accuracy**: The model achieved an accuracy of approximately 95.94%.
- **Confusion Matrix**: The confusion matrix showed that the model correctly identified 89 fraudulent transactions with 6 false negatives and 2 false positives.

## Conclusion

The SVM model performed well on the balanced dataset, achieving high accuracy and demonstrating the ability to effectively identify fraudulent transactions. Future work could include exploring other models or techniques to further improve performance and handle data imbalance.
