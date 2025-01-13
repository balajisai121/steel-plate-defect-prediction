# steel-plate-defect-prediction
A machine learning project for predicting defects in steel plates using advanced models like XGBoost, CatBoost, Random Forest, and SVM. Features robust preprocessing, EDA, and feature engineering for high AUC scores.

# Steel Plate Defect Prediction

This repository contains a comprehensive machine learning project aimed at predicting defects in steel plates. It includes data preprocessing, exploratory data analysis (EDA), feature engineering, and advanced model training using techniques like XGBoost, CatBoost, Random Forest, and SVM.

## Project Overview
- **Objective**: Predict different classes of defects on steel plates with high accuracy.
- **Key Metric**: Area Under the ROC Curve (AUC), which provides a balanced measure of model performance.

## Dataset Description
- **Training Data**: 21,160 rows, 35 columns
- **Test Data**: 12,814 rows, 28 columns
- **Defect Types**:
  - Pastry, Z-Scratch, K-Scratch, Stains, Dirtiness, Bumps, Other Faults

## Features and Insights
- Significant features: `X_Maximum`, `Y_Maximum`, `Luminosity Index`, `Steel Plate Thickness`, etc.
- Distribution patterns:
  - Gaussian-like features: `Edges Y Index`
  - Skewed features: `Pixels Areas`, `X Perimeter`, `Y Perimeter`
- Correlation analysis reveals strong and weak dependencies among features.

## Models and Performance
- **Models Trained**:
  - XGBoost
  - CatBoost
  - Random Forest
  - SVM (with kernel trick)
- **Results**:
  - Best AUC score: 0.8481 (Stacked Model)
  - ROC curves generated for all defect categories.

## Preprocessing Techniques
- Normalization using Quantile Transformer.
- Handling skewed distributions and outliers.
- Feature scaling for improved model performance.

## Repository Structure
```plaintext
steel-plate-defect-prediction/
├── data/                 # Raw and cleaned datasets
│   ├── train.csv
│   ├── test.csv
│   └── submission.csv
├── notebooks/            # Jupyter notebooks for EDA and model training
│   ├── preprocessing.ipynb
│   ├── eda.ipynb
│   ├── model_training.ipynb
│   └── stacked_model.ipynb
├── visualizations/       # Plots and charts
│   ├── roc_curves.png
│   ├── correlation_matrix.png
│   └── feature_distributions.png
├── results/              # Model outputs and evaluation metrics
│   ├── classification_report.txt
│   └── predictions.csv
├── README.md             # Project overview
├── LICENSE               # License file
└── requirements.txt      # Python dependencies
