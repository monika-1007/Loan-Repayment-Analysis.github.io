# 🚗 NBFI Vehicle Loan Repayment Analysis

## 📊 Project Overview

This project investigates vehicle loan repayment behaviors for a Non-Banking Financial Institution (NBFI), which is experiencing profitability issues due to increased default rates. Our aim was to explore and visualize customer data to identify key indicators of loan default and guide feature selection for future predictive modeling.

Dataset Source: [Kaggle - NBFI Vehicle Loan Repayment Dataset](https://www.kaggle.com/datasets/meastanmay/nbfi-vehicle-loan-repayment-dataset)

---

## 🎯 Objective

Use **data visualization** to:

* Identify key variables that distinguish defaulters from non-defaulters.
* Select and justify features for future predictive modeling by analyzing patterns.
* Eliminate noise by discarding less informative variables.

---

## 📁 Contents

* **Data Cleaning**

  * Handled missing values through mean, mode, and proportional imputation.
  * Created derived features like `Loan_Duration`, `Age`, `Employed_Years`, and `Registration_Years`.

* **Exploratory Data Analysis (EDA)**

  * Histograms, bar charts, scatter plots, line plots, pie charts, heatmaps, and box plots.
  * Key focus areas: income, credit score, employment, education, registration duration, and application behavior.

---

## 🔍 Key Findings

### 🔐 Retained Features

* `Client_Income` & `Client_Income_Type`
* `Credit_Amount` & `Loan_Annuity` (→ used to derive `Loan_Duration`)
* `Client_Education`
* `Age` (derived from `Age_Days`)
* `Employed_Days` → `Employed_Years`
* `Registration_Days` → `Registration_Years`
* Credit scores: `Score_Source_1`, `Score_Source_2`, `Score_Source_3` → `Avg_Score`

### 🚫 Removed Features

* `Application_Process_Day` & `Hour`: No useful pattern observed.
* `Car_Owned`: Only a 1.3% difference in default rate between owners and non-owners.

---

## 📈 Visualizations

* **Histograms**: Income distribution, skewness, and outlier handling.
* **Scatter Plots**: Credit Amount vs. Income patterns.
* **Bar Charts**: Employed years vs. default percentage.
* **Pie Charts**: Default distribution across education levels and car ownership.
* **Line Plots**: Registration duration and age correlations.
* **Box Plots**: Credit scores and default likelihood.
* **Heatmaps**: Application timing patterns.

---

## 🛠 Technologies Used

* Python (Pandas, NumPy)
* Seaborn & Matplotlib
* Jupyter Notebook

---

## 📌 Recommendations

* Add a more detailed **data dictionary** for better feature understanding (e.g., clarify if income is annual or monthly).
* Include **APR (Annual Percentage Rate)** for deeper financial analysis.
* Incorporate **vehicle specs** to assess their influence on loan terms and defaults.
