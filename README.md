# Multiple Linear Regression Analysis of Jet Turbine Engine Thrust

This repository hosts an end-to-end multiple linear regression (MLR) analysis applied to a jet turbine engine performance dataset (`turbine_thrust.XLS`). The project evaluates how six operational and engineering predictor variables ($x_1$ to $x_6$) simultaneously influence the core engine response variable: **Turbine Thrust ($y$)**.

The primary objective is to construct a parsimonious predictive model, diagnose regression assumptions, identify influential anomalies, and deliver data-backed engineering recommendations for system control.

---

## 📊 Project Scope & Statistical Framework

The analysis steps through a comprehensive data-science and econometrics workflow:
1. **Data Ingestion & Integrity Checks**: Loading matrix inputs via `readxl` and identifying basic structure layouts.
2. **Exploratory Data Analysis (EDA)**: Mapping bivariate distributions and generating scatter charts to scan for structural trends.
3. **Model Fitting**: Building a full ordinary least squares (OLS) multiple linear regression model matching the framework:
   $$y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \beta_3 x_3 + \beta_4 x_4 + \beta_5 x_5 + \beta_6 x_6 + \epsilon$$
4. **Assumption Diagnostics**: Evaluating model fit using key regression diagnostics:
   * **Residual Analysis**: Residuals vs. Fitted plots to test homoscedasticity.
   * **Normality Testing**: Q-Q plots to confirm normally distributed errors.
   * **Multicollinearity Checks**: Calculating Variance Inflation Factors (VIF) to detect highly correlated predictors.
5. **Influence & Outlier Diagnostics**: Computing **Cook's Distance** and **DFFITS** thresholds to flag highly leverageable operational anomalies.

---

## 🛠️ Tech Stack & Dependencies

The analytics pipeline is developed inside an **R Markdown** environment using standard statistical packages:
* **`readxl`**: Programmatic Excel spreadsheet importing.
* **`car`**: Applied regression checks, diagnostic plots, and VIF calculation engines.
* **`ggplot2`**: Presentation-ready diagnostic and trend plotting matrices.

---

## 🏆 Key Engineering Insights & Findings

Based on the statistical evaluations computed in the script, the following operational trends were established:
* **Primary Driver**: Primary Speed (PSR) acts as the most statistically significant positive predictor driving turbine thrust values upward.
* **Thermal Drag**: Exhaust Temperature (ET) demonstrates a distinct, statistically significant negative relationship with system performance outputs.
* **Control Recommendations**: Operators should focus heavily on optimizing primary speed parameters while actively monitoring exhaust temperature safety thresholds to maintain peak engine thrust profiles.

---

## 🏃‍♂️ How To Run

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/turbine-thrust-regression.git](https://github.com/YOUR_USERNAME/turbine-thrust-regression.git)
   cd turbine-thrust-regression
