# House Price Prediction - Project Analysis

This repository contains the data science workflow, trained machine learning models, and key findings for the house price prediction task.

## Project Summary
1. The `Housing.csv` file dataset consists of 545 rows and 13 columns. The features include Price, Area, parking lots, bathrooms, furniture details, and more.
2. The data contains no missing or duplicate values and was clean prior to modeling.
3. Categorical data was converted into numerical data using one-hot encoding, resulting in 21 feature columns instead of the original 13.

## Model Evaluation & Metrics
After an 80-20 train-test split, the data was trained using a Linear Regression model and a Random Forest model (configured with `n_estimators=200` for maximum precision). The performance metrics are detailed below:

| Measures | Linear Regression | Random Forest |
| :--- | :--- | :--- |
| **Mean Absolute Error (MAE)** | 970043.40 | 1015097.17 |
| **Root Mean Squared Error (RMSE)** | 1324506.96 | 1398658.02 |
| **R² Score** | **0.652924** | 0.612975 |

## Key Findings
* **Feature Relationships:** The feature correlation map supports that key features like `Area` and `airconditioning` have a clear straight-line relationship with the price, making the target trend inherently linear.
* **Model Selection:** Since linear regression works exceptionally well with simpler data displaying clear linear trends over complex models on a smaller dataset like this, it achieved higher performance, making it the preferred choice for this task.
