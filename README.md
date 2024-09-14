# Home-Credit-Default-Risk-Analysis

This repository contains an in-depth analysis and model implementation for the [Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk) dataset. The goal of this project is to predict the probability that a customer will experience difficulties in repaying a loan.

## Project Overview

In this project, I explored various machine learning models to tackle the classification task. The project involved:

- **Data Preprocessing and Exploratory Data Analysis (EDA)**
- **Feature Selection** to identify the most important features
- **Model Training** using LightGBM, CatBoost, and Ridge Regression
- **Hyperparameter Tuning** to optimize model performance
- **Model Evaluation** based on accuracy, AUC score, and other relevant metrics.

## Dataset

The dataset is sourced from the [Kaggle Home Credit Default Risk competition](https://www.kaggle.com/c/home-credit-default-risk/data). It contains detailed information on client loan applications, credit history, and financial status.

### Key Files
- `EDA.ipynb`: Contains the exploratory data analysis and feature engineering steps.
- `Catboost.ipynb`: CatBoost model implementation, hyperparameter tuning, and evaluation.
- `LightGBM.ipynb`: LightGBM model implementation, feature selection, and evaluation.
- `Ridge.ipynb`: Ridge regression model implementation and initial experiments.

## Models Used

### Ridge Regression
- Initial attempts using Ridge regression showed that it was not the best model for this dataset, as it performed poorly compared to gradient boosting models.
- The accuracy and AUC score did not meet expectations, leading to the decision to focus on tree-based models.

### LightGBM
- LightGBM was one of the best-performing models on this dataset.
- After feature selection and hyperparameter optimization, the model achieved an AUC score of over **77%**.
- It proved to be efficient in handling large datasets and categorical features.

### CatBoost
- CatBoost also performed well, comparable to LightGBM, with a similar AUC score of over **77%**.
- CatBoost was particularly effective in dealing with categorical variables without requiring extensive preprocessing.

## Feature Selection

During the model training process, feature selection was applied to improve model performance. Techniques like **LOFO (Leave-One-Feature-Out) importance** were used to identify the most impactful features, which significantly contributed to boosting the model's performance.

## Hyperparameter Optimization with Optuna

I used **Optuna**, a framework for hyperparameter optimization, to fine-tune both LightGBM and CatBoost models. Optuna’s efficient search space exploration allowed me to find the best combination of hyperparameters, which maximized the AUC score.

### Key Results

- The Ridge regression model was not suitable for this dataset.
- Both LightGBM and CatBoost achieved an AUC score of **77%** or higher after feature selection and hyperparameter tuning.

## How to Run the Notebooks

1. Clone this repository:
   ```bash
   git clone https://github.com/beyzasenoll/Home-Credit-Default-Risk-Analysis.git
   cd Home-Credit-Default-Risk-Analysis
