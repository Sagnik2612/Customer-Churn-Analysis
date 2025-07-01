#  Bank Customer Churn Analysis

##  Introduction

In a highly competitive banking industry, customer retention is critical. Losing high-value clients to competitors not only impacts revenue but also affects brand loyalty. This project addresses a core question: **Which customers are likely to churn, and why?**

Using real-world bank data from Kaggle, we perform a deep exploratory analysis and build a predictive model to identify churned customers, understand driving factors, and offer strategic recommendations for stakeholder action.

---

##  Problem Statement

A retail bank observed increasing customer churn and seeks to:
- Identify **which customers are likely to exit** (churn).
- Understand **why they’re leaving** based on demographics and financial behavior.
- Enable data-driven **retention strategies** that lower attrition risk.

---

##  Stakeholder Expectations

Business stakeholders:Product, Marketing, and CX (Customer Experience)teams

expect:

- Clear, visual breakdown of **churn patterns** by geography, age, account activity, and balance.
- A reliable **ML model to predict future churners**.
- Actionable insights that are **quantifiable and segment-specific**.
- A strategic report to help allocate **retention resources effectively**.

---

##  Dataset Overview

-  **Size:** 10,000 customers
-  **Features:** Credit Score, Geography, Gender, Age, Tenure, Balance, Products, Card Holding, Activity, Salary
-  **Target:** `Exited` (1 = churned, 0 = retained)
-  **Source:** [Kaggle - Churn Modelling CSV](https://www.kaggle.com/datasets/aakash50897/churn-modellingcsv)

---

##  Exploratory Data Analysis (EDA)

###  Geography vs Churn

- **Germany** has the highest churn rate (~46%).
- **France** has the largest customer base but lowest churn.
- Stakeholders should **prioritize Germany** for intervention.

###  Gender Distribution

- Slightly more **female customers churned** than males (by ~5–7%).
- Indicates gender-based communication or product gaps.

###  Age vs Churn

- Churned customers are generally **older (avg ~45)**.
- Younger customers (30–40) show lower churn → age is a key risk marker.

###  Balance vs Churn

- Customers with **balance = 0** rarely churned.
- High churn seen in customers with **balance > ₹100,000**, often high-value clients.

###  Customer Activity

- Inactive users (`IsActiveMember = 0`) are **twice as likely to churn**.
- Customer engagement is a strong negative correlate with churn.

###  Number of Products

- Customers with **2 products churned most** (unexpected pattern).
- Likely due to aggressive cross-selling without value addition.

###  Correlation Heatmap

- **Age, Balance, and Inactivity** are positively correlated with churn.
- **Engagement and number of products** show negative or complex relationships.

---

##  Machine Learning Model Summary

###  Model: Logistic Regression

- **Accuracy:** ~80%
- **Churn Recall (Sensitivity):** ~35–40%
- **Interpretability:** High

The model gives a decent baseline. While accuracy is strong, **low recall suggests potential for better models** (e.g., XGBoost or Random Forest) in future iterations.

---

##  Business Impact & Recommendations

 Target churn reduction in:
-  Germany
-  Age group 45+
-  High-balance clients

 Suggested Retention Strategies:
- Personalized loyalty offers for high-value clients
- Age-specific support concierge services
- Re-engagement emails or app nudges for inactive customers

 Resource Allocation:
- Focus on **high-risk, high-LTV** segments (older, high-balance, Germany)
- Improve CX touchpoints for **female churners** based on feedback analysis

---

##  Repository Navigation

| Folder/File                | Purpose                                      |
|---------------------------|----------------------------------------------|
| `Customer_Churn_Analysis.ipynb` | Full annotated notebook with EDA + ML      |
| `README.md`                | Project summary & business insights         |

---

##  Conclusion

This project demonstrates how **data-driven churn analysis** can uncover hidden trends and enable **targeted retention strategies** in the banking sector. With clear visuals, percent-driven inferences, and actionable insights, stakeholders can confidently reduce attrition by addressing churn causes where they matter most.

The project balances **technical accuracy and business relevance**, making it a strong portfolio piece and a practical blueprint for solving real-world churn problems.

---

