# Prostate Cancer Tumor Classification

This project builds a machine learning model to classify prostate cancer tumors based on clinical features, moving from raw data to evaluation and insights.

## Project Overview

- **Goal:** Predict whether a prostate tumor belongs to a specific class (e.g., malignant/benign or risk group) using patient and tumor characteristics.
- **Type:** Supervised classification (machine learning).
- **Tools:** Python (Jupyter Notebook), pandas, NumPy, scikit-learn, matplotlib/seaborn

## Problem Statement
Our objective is to predict whether a cancer is benign or malignant using various measurements of the tumor. The dataset includes the following columns:
- **id**
- **radius**
- **texture**
- **perimeter**
- **area**
- **smoothness**
- **compactness**
- **symmetry**
- **fractal_dimension**
- **diagnosis_result(target variable)**

## Dataset

- **File:** `Dataset_Prostate_Cancer-1.csv`
- **Description:** Tabular dataset of prostate cancer cases with multiple clinical features and a target label.
- **Typical columns:** Tumor attributes (e.g.radius, texture,perimeter) and a target column indicating tumor class.  
- **Preprocessing steps:**
  - Handled missing or inconsistent values.
  - SMOTE (perform smote to balance the data set with the target variable)
  - Encoded categorical variables
  - Scaled/normalized numerical features as needed.
  - Split data into training and test sets.
