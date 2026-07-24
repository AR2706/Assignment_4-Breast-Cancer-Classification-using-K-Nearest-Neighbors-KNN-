# Breast Cancer Prediction using K-Nearest Neighbors (KNN)

This notebook demonstrates a complete workflow for predicting breast cancer using a K-Nearest Neighbors (KNN) classifier. The process covers data exploration, preprocessing, model training, and evaluation.

## Table of Contents

*   [1. Data Exploration](#1.-Data-Exploration)
*   [2. Preprocessing](#2.-Preprocessing)
*   [3. Model Training](#3.-Model-Training)
*   [4. Evaluation Metrics](#4.-Evaluation-Metrics)
*   [Conclusion](#Conclusion)

## 1. Data Exploration

In this section, the dataset is loaded using `kagglehub` and `pandas`. We perform an initial inspection of the data, including viewing the first few rows, identifying target and feature attributes, and examining the dataset's summary statistics (`info()` and `describe()`). This helps in understanding the structure, data types, and basic statistical properties of the dataset.

## 2. Preprocessing

This phase prepares the data for model training. The steps involved are:

*   **Checking for missing data:** Verifying the presence of any null values.
*   **Dropping unneeded columns:** Removing irrelevant columns such as 'id' and 'Unnamed: 32'.
*   **Target encoding:** Converting the categorical 'diagnosis' target variable (Malignant/Benign) into numerical format (1/0) using `LabelEncoder`.
*   **Train/Test split:** Dividing the dataset into training and testing sets (80/20 split) to evaluate the model's performance on unseen data.
*   **Feature Standardization:** Scaling the numerical features using `StandardScaler` to ensure that all features contribute equally to the distance calculations in the KNN algorithm.

## 3. Model Training

Here, a K-Nearest Neighbors classifier is initialized and trained. The model is configured with `n_neighbors=5` and `weights='uniform'`. The `fit` method is used to train the model on the scaled training features and corresponding target labels. After training, predictions are generated on the scaled test data.

## 4. Evaluation Metrics

This section assesses the performance of the trained KNN model using several key classification metrics:

*   **Accuracy Score:** Measures the overall correctness of the model.
*   **Precision Score:** Indicates the proportion of positive identifications that were actually correct.
*   **Recall Score:** Measures the proportion of actual positives that were identified correctly.
*   **F1-Measure:** The harmonic mean of precision and recall, providing a balanced measure.
*   **Confusion Matrix:** A table that describes the performance of a classification model on a set of test data for which the true values are known.

The model achieved a high accuracy of 0.9649, indicating strong performance in classifying breast cancer cases.

## 5. Conclusion

This notebook successfully demonstrates the process of building a K-Nearest Neighbors (KNN) classifier for breast cancer prediction. We performed the following key steps:

1.  **Data Exploration:** Loaded and understood the dataset, identifying features and the target variable.
2.  **Preprocessing:** Handled missing values, dropped unneeded columns, encoded the target variable, split the data into training and testing sets, and standardized features.
3.  **Model Training:** Initialized and trained a KNN model with `K=5` on the scaled training data.
4.  **Evaluation:** Evaluated the model's performance using accuracy, precision, recall, F1-score, and a confusion matrix, achieving a high accuracy of 0.9649
