# Regression Model Comparison for Housing Price Prediction

## Overview

Developed and evaluated multiple regression models for residential housing price prediction using a real estate dataset. Compared Ordinary Least Squares (OLS), Ridge Regression, and Nadaraya-Watson Kernel Regression to assess the impact of regularization and nonparametric methods on predictive performance.

The project focused on model selection, hyperparameter tuning, and performance evaluation using cross-validation and test set error metrics.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Jupyter Notebook
* Git/GitHub

## Skills Demonstrated

* Regression Analysis
* Predictive Modeling
* Statistical Learning
* Ridge Regression
* Regularization
* Hyperparameter Tuning
* Cross Validation
* Model Selection
* Nonparametric Regression
* Data Preprocessing
* Data Visualization
* Performance Evaluation

## Project Highlights

* Implemented and compared three regression approaches: OLS, Ridge Regression, and Nadaraya-Watson Kernel Regression
* Performed 4-fold cross-validation to select optimal hyperparameters
* Tuned Ridge Regression regularization strength using validation error
* Implemented Gaussian kernel regression from scratch
* Evaluated model performance using Mean Squared Error (MSE)
* Identified OLS as the best-performing model on the test dataset

## Objective

The goal of this project was to compare the predictive performance of multiple regression techniques for housing price estimation. The analysis investigated how regularization and nonparametric methods affect model accuracy and generalization performance.

## Dataset

The dataset contains residential housing information used to predict property sale prices.

Features included:

* Property Area
* Housing Characteristics
* Categorical Property Features
* Structural Attributes
* Price Information

Categorical variables were transformed into numerical features using one-hot encoding prior to model training.

## Methodology

### Data Preparation

* Loaded housing data
* Separated predictors and target variable
* Applied one-hot encoding to categorical features
* Split data into training and testing sets using an 80/20 train-test split
* Fixed random state for reproducibility

### Ordinary Least Squares (OLS)

* Trained a baseline linear regression model
* Evaluated predictive performance on the test set
* Computed test Mean Squared Error (MSE)

### Ridge Regression

* Applied L2 regularization to reduce model complexity
* Evaluated multiple regularization strengths using 4-fold cross-validation
* Selected the optimal lambda value based on validation error
* Retrained the model using the selected hyperparameter

Optimal hyperparameter:

* Lambda = 4

### Nadaraya-Watson Kernel Regression

Implemented a Gaussian kernel regression model from scratch.

Steps included:

* Defined Gaussian kernel weighting function
* Computed weighted predictions using neighboring observations
* Tuned bandwidth parameter using 4-fold cross-validation
* Selected the optimal bandwidth based on validation error

Optimal hyperparameter:

* Bandwidth (h) = 400

### Model Evaluation

Models were compared using Mean Squared Error (MSE) on the test dataset.

Evaluation metrics:

* OLS Test MSE
* Ridge Regression Test MSE
* Kernel Regression Test MSE

## Results

### Model Performance

| Model             |     Test MSE |
| ----------------- | -----------: |
| OLS Regression    | 1.754 × 10¹² |
| Ridge Regression  | 1.763 × 10¹² |
| Kernel Regression | 3.808 × 10¹² |

### Key Findings

* OLS achieved the lowest test MSE and best predictive performance.
* Ridge Regression produced similar results, indicating that regularization provided limited benefit for this dataset.
* Kernel Regression performed significantly worse than the linear models.
* Using only a single feature for kernel regression likely contributed to underfitting and reduced predictive accuracy.

## Repository Structure

```text
├── README.md
├── Project_Report.pdf
└── regression_model_comparison.py
```

## Key Takeaways

* Cross-validation is an effective method for selecting model hyperparameters.
* Regularization does not always improve predictive performance when overfitting is not a major concern.
* Model complexity should be balanced against available information and feature richness.
* Nonparametric methods may underperform when limited features are used for prediction.
* Comparing multiple modeling approaches provides valuable insight into model selection and predictive performance.
