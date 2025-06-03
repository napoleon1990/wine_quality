# Wine Quality Prediction using Linear Regression

 ## Overview
This project analyzes a wine quality dataset from Kaggle, focusing on predicting wine quality based on physicochemical properties. The analysis includes:

Data loading & exploration

Feature scaling

Simple Linear Regression (single feature: alcohol content)

Multiple Linear Regression (all features)

Model evaluation & visualization

The goal is to determine how well chemical properties (e.g., acidity, alcohol content, pH) can predict wine quality (rated on a scale from 0 to 10).

## Dataset
The dataset consists of two CSV files:

winequality-red.csv (red wine samples)

winequality-white.csv (white wine samples)

Each dataset includes the following features:

Fixed acidity

Volatile acidity

Citric acid

Residual sugar

Chlorides

Free sulfur dioxide

Total sulfur dioxide

Density

pH

Sulphates

Alcohol

Quality (target variable, score between 0-10)

##  Data Preprocessing
Loading & Merging Data

Red and white wine datasets are loaded and merged into a single DataFrame (df).

pd.read_csv() is used with sep=';' since the data is semicolon-separated.

Exploratory Data Analysis (EDA)

Checked data structure with df.head(), df.columns, and df.dtypes.

Examined unique quality ratings with df["quality"].unique().

Feature Scaling

Applied StandardScaler() to normalize features (except quality) for better model performance.

## Linear Regression Models
1. Simple Linear Regression (Alcohol vs. Quality)
Goal: Predict wine quality based solely on alcohol content.

Model: LinearRegression() from sklearn.

Train-Test Split: 70% training, 30% testing (test_size=0.3).

Evaluation Metrics:

Mean Squared Error (MSE): Measures average squared difference between predicted and actual values.

R² Score (Coefficient of Determination): Indicates how well the model explains variance in the target variable (0 = worst, 1 = best).

# Results:

MSE: [Value from your output]

R² Score: [Value from your output]

# Visualization:

A scatter plot shows actual quality scores (blue dots) vs. the predicted regression line (red).

Helps visualize how well alcohol content alone predicts quality.

2. Multiple Linear Regression (All Features vs. Quality)
Goal: Improve prediction accuracy by using all available features.

Train-Test Split: 67% training, 33% testing (test_size=0.33).

# Evaluation Metrics:

MSE: [Value from your output]

R² Score: [Value from your output]
