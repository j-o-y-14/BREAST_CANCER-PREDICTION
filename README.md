# Breast Cancer Prediction using Machine Learning

# Project Overview

This project aims to build a classification model to predict whether a breast tumor is malignant (cancerous) or benign (non-cancerous) based on features computed from breast cell nuclei (such as radius, texture, smoothness).

The dataset used is the Breast Cancer Wisconsin Diagnostic Dataset (WBCD), a popular dataset for machine learning in healthcare.

# Dataset Description

Target variable:

diagnosis → M = Malignant, B = Benign

Features:

30 numeric features describing cell characteristics (radius, texture, perimeter, area, smoothness, compactness, symmetry, etc.).

Example features include:

radius_mean: Mean of distances from center to points on perimeter

texture_mean: Standard deviation of gray-scale values

area_mean: Area of the cell nuclei

smoothness_mean: Local variation in radius lengths

# Project Workflow
1️⃣ Data Preparation

Handle missing values (if any).

Encode target variable (M → 1, B → 0).

Scale numerical features using StandardScaler.

2️⃣ Exploratory Data Analysis (EDA)

Countplot of target distribution (balanced vs imbalanced).

Histograms of numerical features.

Correlation heatmap of features.

Boxplots to detect outliers.

3️⃣ Model Training

Implemented multiple classification models using pipelines:

Logistic Regression

Decision Tree

Random Forest

Gradient Boosting

Support Vector Machine (SVM)

4️⃣ Model Evaluation

Metrics used:

Accuracy

Precision, Recall, F1-Score

ROC-AUC Score

Confusion Matrix

# Results
Model	Accuracy	ROC-AUC
Logistic Regression	~97%	~0.99
Decision Tree	~93%	~0.94
Random Forest	~96%	~0.98
Gradient Boosting	~97%	~0.99
Support Vector Machine	~97%	~0.99

 Best Model: Logistic Regression → all achieved high accuracy and strong ROC-AUC.

# Key Insights

The dataset is relatively balanced (benign > malignant, but both present).

Certain features like mean radius, mean texture, and mean perimeter are highly predictive.

Logistic Regression worked very well because the dataset is linearly separable.

Ensemble methods (Random Forest, Gradient Boosting) provide robust performance.

# Requirements

Python 3.8+

pandas, numpy

matplotlib, seaborn

scikit-learn

# Conclusion

This project demonstrates how machine learning models can achieve high accuracy in predicting breast cancer. The insights can support doctors in diagnosis, though such models should always be used as decision support tools alongside professional medical expertise.