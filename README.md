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

## Methodology

All steps are implemented in the notebook:

- **Exploratory Data Analysis (EDA):**
  - Summary statistics and data distribution.
  - Correlation analysis and basic visualizations.
- **Feature Engineering:**
  - Feature selection and transformation steps.
- **Modeling:**
  - Trained classification models .•	Applied various models: Logistic Regression, Decision Tree, Random Forest, SVM, Naive Bayes, Gradient Boost, and XGBoost.
  - Tuned hyperparameters where applicable.
- **Evaluation:**
  - Train/test split.
  - Metrics such as accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC.
  - Interpretation of model results and important features.

## Model Results and Final Conclusion

### Initial accuracy scores (test set)

- Logistic Regression: 0.8667
- CART (Decision Tree): 0.7000
- Random Forest: 0.8667
- SVM: 0.8000
- KNN: 0.8667
- Naive Bayes: 0.7667

Since Logistic Regression, Random Forest, and KNN showed relatively high initial accuracies, hyperparameter tuning was applied to these three models to check whether performance could be improved further. However, the accuracies of Logistic Regression and KNN did not increase even after using tuned parameters.

For Random Forest, hyperparameter tuning **did** improve performance: the tuned test accuracy reached **93.33%**, which is higher than the default Random Forest accuracy of about **86%**. In addition, the classification report for the tuned Random Forest model shows the lowest number of false positives and false negatives among the three shortlisted models, along with the best F1-score and overall accuracy.

**Final conclusion:** Random Forest with hyperparameter tuning is the best-performing model for this problem, and the tuned predictions (e.g., `y_pred_rf2_best`) should be used for final tumor class prediction.

## Files in this Repository

- `Prostate-Cancer_Final-Notebook-1.ipynb`  
  Jupyter Notebook with EDA, preprocessing, model training, and evaluation.

- `Dataset_Prostate_Cancer-1.csv`  
  Dataset used to train and evaluate the model.

- `Prostate-Cancer-Tumor-Classification.docx`  
  Written report describing the problem, approach, results, and conclusions.


## How to Run

1. **Clone this repository:**
   ```bash
   git clone https://github.com/your-username/prostate-cancer-tumor-classification.git
   cd prostate-cancer-tumor-classification


## Disclaimer

This analysis is for educational purposes only.  
The models and results are not validated for clinical use and should not be used for real medical decisions.
