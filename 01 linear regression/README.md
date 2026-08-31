# Student Performance Prediction using Linear Regression

## Overview

This project uses Linear Regression to predict students' final exam scores
(G3) based on various academic, demographic, and other student-related
features.

The project follows a complete Machine Learning workflow, including data
understanding, data cleaning, exploratory data analysis, preprocessing,
model training, evaluation, and interpretation.

## Objective

The main objective of this project is to understand whether information about
a student's academic performance and other characteristics can be used to
predict their final exam score (G3).

## Dataset

The dataset contains **649 student records and 33 columns**.

The target variable is:

- `G3` - Final exam score

Some important features explored in the project include:

- `G1` - First period grade
- `G2` - Second period grade
- `studytime` - Weekly study time
- `failures` - Number of past class failures
- `absences` - Number of school absences
- Other demographic, social, and academic features

## Machine Learning Workflow

The project follows these steps:

1. Importing required libraries
2. Loading the dataset
3. Understanding the dataset
4. Checking data types and summary statistics
5. Checking for missing values
6. Checking for duplicate values
7. Identifying potential outliers
8. Exploratory Data Analysis
9. Analyzing relationships between features and final score
10. Creating a correlation matrix
11. Separating features and target variable
12. Splitting the data into training and testing sets
13. Identifying numerical and categorical features
14. Building a preprocessing pipeline
15. Training the Linear Regression model
16. Making predictions
17. Evaluating model performance
18. Analyzing regression coefficients
19. Actual vs Predicted analysis
20. Residual analysis

## Exploratory Data Analysis

Several relationships were explored to understand the factors associated
with students' final scores.

### Study Time vs Final Score

The relationship between weekly study time and final exam score was
visualized using a scatter plot.

The analysis suggests that higher study time may be associated with better
scores, although the relationship is not perfectly linear and there is
considerable variation within each study-time group.

### G1 and G2 vs G3

The relationships between previous period grades (`G1` and `G2`) and the
final grade (`G3`) were analyzed.

`G2` shows a particularly strong positive linear relationship with `G3`,
while `G1` also has a strong positive relationship.

### Correlation Analysis

A correlation matrix was created to examine relationships between numerical
features.

The strongest positive relationships with `G3` were observed for `G2` and
`G1`. Previous failures showed a moderate negative relationship with final
performance, while many other variables had relatively weaker relationships
with `G3`.

## Data Preprocessing

A Scikit-learn preprocessing pipeline was used to handle numerical and
categorical features separately.

### Numerical Features

The numerical preprocessing pipeline includes:

- Median imputation for missing values
- Standardization using `StandardScaler`

### Categorical Features

The categorical preprocessing pipeline includes:

- Most-frequent imputation
- One-hot encoding
- Dropping the first encoded category
- Handling previously unseen categories using `handle_unknown="ignore"`

`ColumnTransformer` was then used to combine both numerical and categorical
preprocessing steps.

## Model

### Linear Regression

Linear Regression was used to predict the final exam score (`G3`).

The model learns coefficients for the input features and uses them to
estimate the student's final score.

The model was implemented together with the preprocessing steps using a
Scikit-learn `Pipeline`.

## Train-Test Split

The dataset was divided into:

- **80% training data**
- **20% testing data**

A `random_state` of 42 was used to make the split reproducible.

## Model Evaluation

The model was evaluated using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

### Mean Squared Error (MSE)

MSE measures the average squared difference between the actual and predicted
values.

A lower MSE indicates smaller prediction errors.

### Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents the prediction error in the
same units as the target variable.

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between the actual and predicted
values.

In this project, the MAE indicates that the model's predictions are, on
average, approximately **0.765 score points away from the actual value**.

### R² Score

The model achieved an R² score of approximately **0.84** on the test set.

This means the model explains approximately **84% of the variation in the
students' final exam scores** within the test set, while approximately 16%
remains unexplained by the model.

## Feature Importance through Coefficients

The Linear Regression coefficients were analyzed to understand which
features have the strongest influence on the predicted final score.

The analysis showed that:

- `G2` is the dominant predictor of `G3`
- `G1` is the next strongest predictor
- The remaining analyzed features have substantially smaller positive or
  negative coefficients

The coefficients were sorted by their absolute magnitude and visualized
using a bar plot.

## Actual vs Predicted Analysis

An actual vs predicted plot was created to compare the model's predictions
with the true `G3` values.

Most predicted values are reasonably close to the ideal diagonal relationship,
indicating that the model performs relatively well on the test set.

However, some observations deviate substantially from the diagonal,
representing larger prediction errors.

## Residual Analysis

Residuals were calculated as:

`Residual = Actual Value - Predicted Value`

The residual plot shows that the residuals are generally distributed around
zero, indicating that the model captures much of the relationship between
the input features and `G3`.

However, a slight downward pattern and a significant negative outlier were
observed, suggesting that some systematic prediction error remains and that
the linear model does not explain all observations equally well.

## Key Learnings

Through this project, I learned and practiced:

- Data exploration and understanding
- Data cleaning
- Handling duplicate values
- Identifying potential outliers
- Exploratory Data Analysis
- Correlation analysis
- Feature-target separation
- Train-test splitting
- Numerical and categorical preprocessing
- Building Scikit-learn Pipelines
- Using `ColumnTransformer`
- Handling missing values
- Feature scaling
- One-hot encoding
- Linear Regression
- MSE, RMSE, MAE and R² evaluation
- Regression coefficient analysis
- Actual vs predicted analysis
- Residual analysis

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
├── linear_regression.ipynb
├── wine-quality/
│   ├── wine quality.ipynb
│   └── README.md
│
└── README.md
