# Syriatel Customer Churn 

## Project Overview

Customer churn is one of the most pressing challenges in the telecommunications industry. Syriatel, like other telecom providers, faces significant revenue losses when customers discontinue their services.

This project builds a **classification model** to predict customer churn and identify the key drivers behind it. By understanding these patterns, Syriatel can take proactive steps to improve customer retention, reduce churn, and increase satisfaction.

---

## Objectives

1. Identify the key factors contributing to customer churn.
2. Build predictive models to classify whether a customer is likely to churn.
3. Evaluate models using appropriate classification metrics.
4. Provide business recommendations to help Syriatel reduce churn and retain customers.

---

## Dataset

The dataset contains **3,333 customer records** with features such as:

* **Customer Information:** state, area code, phone number.
* **Service Usage:** day, evening, and night call minutes, charges, and number of calls.
* **Plans:** international plan, voice mail plan.
* **Customer Service Interaction:** number of customer service calls.
* **Target Variable:** churn (1 = churned, 0 = not churned).

---

##  Analysis

* **Data Cleaning:**

To prepare the dataset for modeling, the following cleaning steps were performed:
* Missing values: Checked for null or missing entries; none were found.
* Irrelevant identifiers: Removed non-informative fields such as phone numbers that do not contribute to prediction.
* Categorical encoding: Converted categorical variables into numerical form using dummy encoding.
* Column consistency: Standardized column names for uniformity and easier reference.
* Class balance: Verified the target variable distribution and applied class_weight="balanced" during modeling to account for any imbalance

* **Exploratory Data Analysis (EDA):**

  * Distribution of churn across features.
  * Bivariate analysis to compare churn with categorical and numerical variables.
  * Identification of redundant features (e.g., charges derived from minutes).

* **Feature Engineering:**

  * Dropped irrelevant features (`phone number`, charges).
  * Created dummy variables for categorical features.
  * Addressed class imbalance using **SMOTE (Synthetic Minority Oversampling Technique)**.

* **Modeling:**

  * Baseline: Logistic Regression.
  * Decision Tree Classifier.
  * Random Forest Classifier (best performing model).
  * Hyperparameter Tuning on Random Forest.

---

##  Results

* **Best Model:** Random Forest Classifier.
* **Accuracy:** \~94% after hyperparameter tuning.
* **Key Predictors of Churn:**

  * International plan.
  * Number of customer service calls.
  * Total day minutes.

---

##  Business Insights

* Customers with **international plans** have a significantly higher churn rate.
* Churn spikes when **customer service calls exceed 3**, suggesting dissatisfaction with support.
* Heavy **daytime users** are more likely to churn, highlighting potential unmet needs in call packages.

---

##  Recommendations

1. **Enhance Customer Service:** Resolve issues more efficiently to prevent churn after repeated calls.
2. **Review International Plans:** Offer competitive pricing or incentives for international users.
3. **Targeted Retention Campaigns:** Use the churn prediction model to flag high-risk customers and intervene early.
4. **Customer-Centric Packages:** Design flexible plans for heavy daytime users.

---
Feel free to connect on [LinkedIn](https://www.linkedin.com/in/peris-kigo-098170302)


