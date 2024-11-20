# Predicting Drilling Performance Using Machine Learning

This repository contains a project that predicts PP Zamora Method, a critical parameter in drilling operations, using machine learning models trained on historical drilling data. The goal is to optimize drilling performance and enhance decision-making by accurately estimating this parameter based on other key drilling parameters.

## Features

- **Input Feature:**
   - ROP (Rate of Penetration)
   - ROP.1 (Alternative ROP representation)
   - WOB.1 (Weight on Bit)
   - BIT_RPM (Bit Rotations Per Minute)
   - MWI (Drilling fluid property - Inflow)
   - MWO (Drilling fluid property - Outflow)
- **Target**
   - PP Zamora Method: A critical drilling parameter we aim to predict.

## Data Challenges

1. **Skewed Features**
  - Some features, like ROP and BIT_RPM, have uneven distributions.
  - **Solution:** Applied a log transformation to compress large ranges and reduce skewness.
2. **Outliers**
  - Features like ROP and BIT_RPM contained extreme values.
  - **Solution:** Used Robust Scaler to normalize the data and reduce the impact of outliers.

## Machine Learning Models
Three machine learning models were trained to predict the PP Zamora Method:

1. **Linear Regression:**
A simple and interpretable model for linear relationships.

2. **Ridge Regression:**
A regularized version of Linear Regression to prevent overfitting.

3. **Random Forest Regressor:**
A flexible model that handles nonlinear relationships and outliers effectively.

## Training and Evaluation:
Train/test split: 70% training, 30% testing.
**Metrics used:**
  - **Mean Squared Error (MSE):** Measures error (lower is better).
  - **R² Score:** Measures how much variance is explained by the model (closer to 1 is better).

## Results
**Linear Regression:**
    Excellent performance with minimal overfitting.
    Best balance of simplicity and accuracy.
    
**Ridge Regression:**
    Robust and stable, with no overfitting.
    
**Random Forest:**
    Slight overfitting but good at handling outliers and nonlinear patterns.
