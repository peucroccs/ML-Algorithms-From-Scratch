## Linear Regression (Ordinary Least Squares)

**File:** `OLS.py`

This module implements a **Linear Regression model estimated using the Ordinary Least Squares (OLS) method**.

---

### Model Overview

- **Model:** Linear Regression
- **Estimation Method:** Ordinary Least Squares (OLS)
- **Solution:** Closed-form (Normal Equation)
- **Intercept:** Must be added manually

---

### OLS Class

The `OLS` class provides a minimal and explicit interface for fitting and analyzing a linear regression model.

#### Public Methods
- `fit(X, y)`
- `predict(X)`
- `summary()`

---

### `fit(X, y)`

Fits the linear regression model using the OLS method.

#### Parameters

- **X** (`numpy.ndarray`)  
  Feature matrix of shape `(n_samples, n_features)`  
  OBS: The intercept term is **not** added automatically.

- **y** (`numpy.ndarray`)  
  Target vector of shape `(n_samples,)`

#### Computed Metrics

After fitting, the following statistics are available:

- Regression coefficients
- R-squared and Adjusted R-squared
- Degrees of freedom
- Residual variance estimate
- Standard errors of the coefficients
- t-statistics
- Two-sided p-values

---

### `predict(X)`

Generates predictions using the fitted model.

#### Parameters

- **X** (`numpy.ndarray`)  
  Feature matrix of shape `(n_samples, n_features)`

#### Returns

- **y_pred** (`numpy.ndarray`)  
  Predicted values

---

### `summary()`

Prints a formatted summary of the regression results, including:

- Coefficient estimates
- Standard errors
- t-statistics
- p-values

---

### Notes

- This implementation prioritizes **clarity and learning** over performance.
- Matrix inversion may fail if the design matrix is singular.
