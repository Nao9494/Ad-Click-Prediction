# Ad Click Prediction | Analytics | XGBoost 97%
This project aims to predict whether users will click on ads using machine learning techniques. Through exploratory data analysis (EDA) and model training, this project demonstrates how to extract insights from the dataset and build a predictive model.

### Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Technical Tools](#technical-tools)
4. [Analysis Process](#analysis-process)
5. [Hyperparameter Tuning](#hyperparameter-tuning)
6. [Results and Conclusion](#results-and-conclusion)
7. [How to Run the Project](#how-to-run-the-project)

---

## Introduction

This project builds a predictive model by analyzing user behavior data to determine whether a user will click on an advertisement. The analysis includes data cleaning, exploratory data analysis, feature engineering, and machine learning model training and hyperparameter tuning.

## Dataset

The dataset contains user ad click behavior with the following key fields:
- **user_id**: Unique identifier for the user
- **age**: Age of the user
- **gender**: Gender of the user
- **device**: Type of device used (desktop, mobile, etc.)
- **ad_position**: Position of the ad (top, side, etc.)
- **ad_category**: Category of the ad (shopping, education, etc.)
- **time_of_day**: Time when the ad was displayed (morning, afternoon, evening, etc.)
- **click**: Whether the ad was clicked (1 for clicked, 0 for not clicked)

> **The dataset used in this project is sourced from Kaggle**: https://www.kaggle.com/datasets/marius2303/ad-click-prediction-dataset

## Technical Tools

This project utilizes the following technical tools:
- **Python 3.12**: Programming language used for development and data processing
- **Pandas**: For data manipulation and cleaning
- **NumPy**: For numerical operations and matrix computations
- **Matplotlib / Seaborn / Plotly Express**: For data visualization and exploratory data analysis
- **Scikit-learn**: For model training and evaluation, including cross-validation and hyperparameter tuning
- **XGBoost**: Gradient Boosting Decision Tree model used for building the ad click prediction model
- **ADASYN**: Synthetic oversampling technique used to address data imbalance

## Analysis Process

1. **Data Cleaning**: Handling missing values and removing irrelevant columns (such as `user_id`).
2. **Exploratory Data Analysis (EDA)**:
   - Using visualization tools to explore the data distribution
   - Analyzing the relationship between click behavior and variables such as age, gender, and device
   - Using KNNImputer to fill in missing age values
3. **Feature Engineering**:
   - Converting categorical variables to numerical codes
   - Using KNNImputer to impute missing age values, followed by mapping categorical variables back to original categories
4. **Model Construction and Evaluation**:
   - Using `XGBoost` to build the model
   - Evaluating the model performance using confusion matrix, classification report, and metrics like accuracy, recall, and F1-score

## Hyperparameter Tuning

We used `GridSearchCV` to tune the hyperparameters of the XGBoost model. The main hyperparameters we tuned include:
- `learning_rate`: Learning rate of the model
- `n_estimators`: Number of trees in the model
- `max_depth`: Maximum depth of the trees

After performing 5-fold cross-validation, the best parameters were found to be:
Best Parameters: { 'learning_rate': 0.2, 'n_estimators': 200, 'max_depth': 7 }
## Results and Conclusion

The model's performance was evaluated using a classification report and confusion matrix. The final model achieved an accuracy of 97%. Based on the model’s predictions, it can effectively distinguish between users who clicked on ads and those who did not. The use of the XGBoost model allowed us to capture key features of ad click behavior, improving prediction accuracy.

## How to Run the Project
1. Clone the repository:
- git clone https://github.com/Nao9494/Ad_Click_Prediction.git
2. Install required dependencies:
- pip install -r requirements.txt 
3. Run the Jupyter Notebook for data analysis:
- jupyter notebook Ad_Click_Prediction.ipynb

---
# README.md
- en [English](README.md)
- zh_TW [繁体中文](README.zh_TW.md)

