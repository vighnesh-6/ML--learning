# Wine Quality Prediction using Linear Regression

## Overview

This project uses Linear Regression to predict wine quality based on its
physicochemical properties.

The project covers the complete Machine Learning workflow, including data
cleaning, exploratory data analysis, preprocessing, model training,
evaluation, and interpretation.

## Objective

The main objective is to understand whether the physicochemical properties
of wine can be used to predict its quality score using a Linear Regression
model.

## Dataset

The dataset contains physicochemical properties of wine along with a
`quality` score, which is the target variable.

### Features

- Fixed Acidity
- Volatile Acidity
- Citric Acid
- Residual Sugar
- Chlorides
- Free Sulfur Dioxide
- Total Sulfur Dioxide
- Density
- pH
- Sulphates
- Alcohol

### Target

- `quality`

## Machine Learning Workflow

1. Data loading and inspection
2. Data cleaning
3. Checking for missing values
4. Checking and handling duplicate values
5. Exploratory Data Analysis
6. Feature relationship analysis
7. Train-test split
8. Data preprocessing using a Pipeline
9. Linear Regression model training
10. Making predictions
11. Model evaluation
12. Coefficient analysis
13. Actual vs Predicted visualization
14. Residual analysis

## Model

### Linear Regression

Linear Regression was used to model the relationship between the wine's
physicochemical properties and its quality score.

The model learns a coefficient for each feature and uses these coefficients
to make predictions of wine quality.

## Evaluation Metrics

The model was evaluated using:

- Mean Squared Error (MSE)
- R² Score

### Mean Squared Error

MSE measures the average squared difference between the actual and predicted
values. A lower MSE indicates smaller prediction errors.

### R² Score

R² measures the proportion of variation in the target variable that is
explained by the model.

## Model Analysis

### Coefficient Analysis

The regression coefficients were analyzed to understand the direction and
relative influence of the different physicochemical features on predicted
wine quality.

### Actual vs Predicted Plot

The actual vs predicted plot was used to compare the model's predictions with
the actual wine quality values.

### Residual Analysis

Residuals represent the difference between the actual and predicted values.
A residual plot was used to examine the model's prediction errors and check
for systematic patterns.

## Key Learning Outcomes

Through this project, I learned and practiced:

- Data cleaning and exploratory data analysis
- Handling duplicate observations
- Feature and target separation
- Train-test splitting
- Machine Learning preprocessing pipelines
- Linear Regression
- Regression evaluation metrics
- Interpreting model coefficients
- Actual vs predicted analysis
- Residual analysis
- Using Git and GitHub to document Machine Learning projects

## Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Project Structure

```text
01-linear-regression/
│
├── wine-quality.ipynb
└── README.md
