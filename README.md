# Crop Recommendation System: A Comparative Study

## Abstract

Agriculture is a critical sector that depends heavily on data-driven decision-making to improve productivity, reduce uncertainty, and optimize resource usage. Crop recommendation systems assist farmers in selecting suitable crops based on environmental and soil conditions, helping them make more informed decisions regarding cultivation. This project presents a comparative study of several machine learning algorithms for crop classification using agronomic parameters such as soil pH, phosphorus, potassium, urea, temperature, and related variables.

The study investigates the effectiveness of Decision Tree, Random Forest, Naive Bayes, Support Vector Machine (SVM), and a Soft Voting ensemble classifier. After preprocessing the dataset, including the removal of irrelevant attributes, outlier detection using the IQR method, class balancing through undersampling, and feature normalization, the models are evaluated using accuracy, precision, recall, F1-score, and confusion matrix analysis. The experimental results demonstrate that the Soft Voting ensemble provides the best predictive performance among the evaluated models.

## Keywords

Crop recommendation, machine learning, comparative study, agricultural analytics, classification, ensemble learning, precision agriculture.

---

## 1. Introduction

Modern agriculture faces the challenge of increasing food production while preserving soil health and minimizing wastage of fertilizer and water resources. A crop recommendation system can help reduce this uncertainty by predicting suitable crops based on soil and climate characteristics. In recent years, machine learning has become an effective tool for building such systems because it can model complex relationships between agricultural features and crop suitability.

This research focuses on building a crop recommendation classifier that selects the most appropriate crop for a given set of soil and environmental conditions. A comparative analysis is performed across multiple state-of-the-art classification models to identify the most reliable algorithm for this domain.

## 2. Problem Statement

The agricultural decision-making process is often based on expert knowledge, field experience, and manual observation. However, such methods may be inconsistent and limited. There is a need for an intelligent system that can assess agronomic conditions and recommend the most suitable crop automatically.

This project addresses the following question:

- Which machine learning model provides the most accurate and robust crop recommendation for the available dataset?

---

## 3. Dataset Description

The project uses a crop-related dataset containing soil and environmental features associated with different plant classes. The dataset contains variables such as:

- pH
- Soil EC
- Phosphorus
- Potassium
- Urea
- T.S.P
- M.O.P
- Moisture
- Temperature
- Plant Type

The target variable is the plant type or crop category. The dataset is initially explored to understand class distributions, missing values, and feature relationships before model training.

### Dataset Characteristics

- Total attributes: 10
- Target variable: Plant Type
- Data type: mixed numeric and categorical values
- Class imbalance was identified during exploratory analysis

---

## 4. Objectives

The main objectives of this work are:

1. To analyze agricultural dataset characteristics and identify relevant attributes for crop classification.
2. To perform data cleaning, feature selection, outlier handling, and balancing techniques.
3. To implement and compare several machine learning classifiers.
4. To evaluate model performance using appropriate classification metrics.
5. To identify the best performing model for crop recommendation.

---

## 5. Methodology

### 5.1 Data Exploration

The dataset is analyzed using descriptive statistics and visualizations to understand:

- feature distribution,
- null values,
- class frequency,
- trend of crop categories,
- correlation between features.

### 5.2 Feature Selection

Irrelevant or redundant attributes such as Soil EC, T.S.P, M.O.P, and Moisture were removed during preprocessing to improve model performance and reduce noise. This step focused the model on the most informative agronomic parameters.

### 5.3 Outlier Removal

Outliers were identified using box plots and removed using the Interquartile Range (IQR) method. The variables considered for outlier removal included:

- pH
- Urea
- Potassium

This step reduces distortion in model learning caused by extreme values.

### 5.4 Class Balancing

The dataset was imbalanced across different crop classes. To avoid bias toward majority classes, undersampling was applied so each class contained a comparable number of samples. The resulting balanced dataset was saved as undersampled_dset1.csv.

### 5.5 Normalization

Z-score standardization was used for selected numerical features to bring them into a consistent scale before training the classifiers. This improves convergence and reduces the impact of varying feature scales.

### 5.6 Train-Test Split

The dataset was divided into training and testing sets using an 80:20 split to evaluate generalization performance on unseen data.

---

## 6. Machine Learning Models

This study compares the following models:

### 6.1 Decision Tree Classifier

A Decision Tree model was used with entropy as the criterion and a depth constraint to create interpretable decision rules based on feature thresholds.

### 6.2 Random Forest Classifier

A Random Forest model was trained using multiple decision trees and aggregated their results to improve robustness and reduce overfitting.

### 6.3 Naive Bayes Classifier

Gaussian Naive Bayes was implemented as a probabilistic classifier, useful for handling continuous numerical features and quick training.

### 6.4 Support Vector Machine (SVM)

The SVM classifier was trained using a polynomial kernel to capture nonlinear relationships among agronomic features.

### 6.5 Soft Voting Ensemble

A Soft Voting ensemble combined the predictions of the Decision Tree, Random Forest, Naive Bayes, and SVM models. This ensemble aggregates class probabilities and is expected to improve stability and accuracy.

---

## 7. Evaluation Metrics

The models were evaluated using standard classification metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Cross-validation accuracy

These metrics provide a complete picture of predictive quality, especially in multi-class crop recommendation tasks.

---

## 8. Experimental Results



The Soft Voting ensemble achieved the highest accuracy and competitive precision, recall, and F1-score. This indicates that combining multiple models improves predictive reliability and generalization. Random Forest also performed strongly, suggesting that ensemble-based tree learning is highly suitable for this domain.

The confusion matrices and visual comparisons further confirm that the ensemble model produced the most balanced classification results across crop categories.

---



## 15. Acknowledgement

This project was developed as a comparative study in machine learning for crop recommendation and demonstrates the practical application of data-driven decision-making in agriculture.

