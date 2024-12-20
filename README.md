# Logistic Regression with Robust Estimators in R
This project demonstrates robust logistic regression using different estimators to handle multicollinearity and outliers. The estimators include ridge regression, Liu estimator, and robust variants such as Bianco-Yohai and conditionally unbiased bounded influence estimators.

## Overview of the Code
The code estimates logistic regression coefficients under conditions of multicollinearity and outliers using iterative and robust methods. Key steps include:

1. **Data Preparation**
-Standardizing the regressors using scale()
-Creating the response (y) and predictor (X) matrices

2. **Initial Estimation**
- Obtaining the first beta estimates using glm with a logit link

3. **Iterative Estimation**
- Iteratively solving for the beta coefficients using weighted least squares (glm.fit)
- A stopping condition based on tolerance (tol) ensures convergence

4. **Shrinkage Methods**
- Ridge Regression
- Liu Estimator
- Robust Kibria-Lukman estimator

5. **Robust Methods**
-Bianco-Yohai (BY) Estimator
-Conditionally unbiased bounded influence (CE) estimator

6. **Performance Metrics**
- Mean Squared Error (MSE)
- Variance and condition index calculations

7. **Comparison of Results**
-Comparing estimates from MLE, Ridge, Liu, and robust methods
- Outputs a summary table of coefficients and MSE values

## Dependencies
The code uses the following R libraries:

RobStatTM: Provides robust statistics tools
robcbi: Supports conditionally unbiased estimators
**To install them, run:**

R
Copy code
install.packages("RobStatTM")  
install.packages("robcbi")  

## Data Used
The Finney dataset is used in this analysis:

Response Variable (Resp)
Predictor Variables:
Vol (Volume of air inspired)
Rate (Inspiration rate)
The predictors are log-transformed to improve model stability.

## Key Outputs
The script generates:

1. Beta Coefficients: Coefficients for MLE, ridge, Liu, and robust methods.
2. Mean Squared Error (MSE): Performance metric for each method.
3. Shrinkage Results: Ridge and Liu estimators compared to robust solutions.
4. Robustness Analysis: Influence of outliers and multicollinearity.


## How to Run the Code
1. Load the required libraries.
2. Ensure the Finney dataset is loaded from the RobStatTM package.
3. Copy and paste the code into an R script file.
4. Run the script in RStudio or any R environment.
