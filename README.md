# ML-Algorithms-From-Scratch

## Description
This project focuses on implementing Machine Learning algorithms without using external libraries. The main goal is to study the mathematics, logic, and internal mechanics behind the most well-known ML models.

## Algorithms Implemented

### OLS (Ordinary Least Squares)

## Linear Regression (OLS)

This module contains an implementation of a **Linear Regression model estimated using the Ordinary Least Squares (OLS) method**, built from scratch for educational purposes.

For implementation details, see `OLS.py`.

---

## OLS Class

The `OLS` class provides a simple interface to fit, predict, and inspect a linear regression model using OLS.

### Available Methods
- `fit(X, y)`
- `predict(X)`
- `summary()`

---

## `fit(X, y)`

Fits a linear regression model using the **Ordinary Least Squares** method.

### Parameters

- **X** (`numpy.ndarray`)  
  Feature matrix of shape `(n_samples, n_features)`  
  ⚠️ This implementation does **not** add an intercept automatically — it must be included manually (e.g., a column of ones).

- **y** (`numpy.ndarray`)  
  Target vector of shape `(n_samples,)`

### Computed Statistics

This method computes and stores:

- Regression coefficients  
- R-squared and Adjusted R-squared  
- Degrees of freedom  
- Residual variance estimate  
- Standard errors for each coefficient  
- t-statistics  
- Two-sided p-values (Student’s t-distribution)

---

## `predict(X)`

Generates predictions using the fitted model.

### Parameters

- **X** (`numpy.ndarray`)  
  Feature matrix of shape `(n_samples, n_features)`

### Returns

- **y_pred** (`numpy.ndarray`)  
  Predicted values for the given input matrix `X`

---

## `summary()`

Prints a formatted summary of the regression results, including:

- Coefficient estimates  
- Standard errors  
- t-statistics  
- p-values  

The output is inspired by classical statistical packages such as `statsmodels`.

---

## Notes

- This implementation is intended for **learning and experimentation**.
- No regularization or numerical stability enhancements are included.
- Matrix inversion may fail if the design matrix is singular.


