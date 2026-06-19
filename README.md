Simple-Linear-Regression-IBM-AI-Engineer

Simple Linear Regression: Predicting Vehicle CO2 Emissions

[[Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[[Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0-orange.svg)](https://scikit-learn.org/)
[[IBM AI Engineer](https://img.shields.io/badge/Course-IBM%20AI%20Engineer%20Certificate-green.svg)]
(https://www.coursera.org/professional-certificates/ibm-ai-engineer)

Project Overview
This project implements Simple Linear Regression using `scikit-learn` to predict the Carbon Dioxide (CO2) emissions of various vehicles. The primary objective is to understand the end-to-end machine learning workflow—from Exploratory Data Analysis (EDA) and train/test splitting to model training and evaluation. 

Additionally, the project compares two different independent variables (`ENGINESIZE` vs. `FUELCONSUMPTION_COMB`) to demonstrate how feature selection impacts model accuracy and error rates.

Dataset
The analysis utilizes the FuelConsumption.csv dataset, sourced from the Government of Canada. It contains model-specific fuel consumption ratings and estimated CO2 emissions for new light-duty vehicles.
Target Variable: `CO2EMISSIONS` (g/km)
Selected Features for Testing: 
  1. `ENGINESIZE` (Liters)
  2. `FUELCONSUMPTION_COMB` (Combined L/100 km)
Data Size: 1,067 vehicle records.

Methodology
The project follows a structured machine learning pipeline:
1. Data Exploration & Visualization: Analyzed feature distributions using histograms and mapped linear relationships via scatter plots to ensure the data was suitable for linear regression.
2. Train/Test Split: Divided the dataset into 80% training data and 20% testing data (`random_state=42`) to evaluate the model's ability to generalize to unseen data.
3. Model Training: Implemented `scikit-learn`'s `LinearRegression` to find the line of best fit (Ordinary Least Squares) for the training data.
4. Evaluation: Assessed model performance on the unseen test set using standard regression metrics: MAE, MSE, RMSE, and R².
5. Feature Comparison: Repeated the pipeline using a second feature to compare predictive power.

Results & Mathematical Interpretation

Experiment 1: Engine Size vs. CO2 Emissions
The algorithm determined the following line of best fit: 
CO2 Emissions = 126.29 + (38.99 × Engine Size)**

| Metric | Value | Interpretation |
| R-Squared (R²) | 0.76 | Engine size explains 76% of the variance in CO2 emissions. |
| RMSE | 31.40 | The average prediction error is ~31.4 g/km. |
| MAE | 24.10 | The average absolute error is ~24.1 g/km. |

Experiment 2: Combined Fuel Consumption vs. CO2 Emissions
The algorithm determined the following line of best fit:
CO2 Emissions = 69.10 + (16.18 × Fuel Consumption Combined)

| Metric | Observation | Interpretation |
| MSE | Lower than Exp 1 | The model's squared errors were smaller, indicating a tighter fit to the data. |

Key Insight: The Importance of Feature Selection
While both models yielded strong R² scores, the model utilizing `FUELCONSUMPTION_COMB` resulted in a lower Mean Squared Error (MSE). Because fuel consumption is a more direct physical proxy for carbon output than engine displacement, the linear relationship is tighter. This highlights a fundamental rule of machine learning: **The quality and relevance of your input features directly dictate the accuracy of your model.

Technologies Used
Python 3.14.5
Pandas: Data loading, statistical summarization (`df.describe()`), and feature extraction.
NumPy: Array reshaping (converting 1D arrays to 2D for scikit-learn compatibility).
Scikit-Learn: Model building (`LinearRegression`), train/test splitting, and evaluation metrics.
Matplotlib: Data visualization (scatter plots, histograms, and regression line overlays).

Skills Demonstrated
a. Implementation of Simple Linear Regression from scratch using scikit-learn.
b. Conducting Exploratory Data Analysis (EDA) to verify linear assumptions.
c. Proper data splitting techniques to prevent overfitting and test generalization.
d. Interpreting regression coefficients, intercepts, and evaluation metrics (R², RMSE, MAE).
e. Comparing multiple features to determine the strongest predictor for a target variable.

Course Participant/Code Executor: Obinna Nwosu C,; Author: Jeff Grossman,; Other Contributor(s): Abhishek Gagneja, © IBM Corporation. All rights reserved.
