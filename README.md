# Customer Retention Decision System
Predicting Customer Churn and Translating ML Predictions into Business Impact

## Project Overview

Customer churn directly affects recurring revenue in subscription-based businesses. While a traditional churn model answers "Which customers are likely to churn?", this project goes one step further:

> "Which customers represent the greatest financial risk, and where should the business focus its retention efforts?"

This project builds a machine learning-based decision-support system that predicts customer churn, estimates 'Expected Revenue at Risk', prioritizes customers based on financial impact, and evaluates potential retention strategies through ROI simulation.

The goal is to demonstrate how machine learning can move beyond prediction and support **real business decisions and revenue protection**.



## Business Problem

A company cannot realistically provide expensive retention interventions to every customer.

A customer with a high probability of churn is not necessarily the highest-value customer to prioritize.

For example:

* Customer A → 90% churn probability × $20 monthly charges
* Customer B → 75% churn probability × $100 monthly charges

Although Customer A has a higher churn probability, Customer B represents a greater potential financial risk.

Therefore, this project combines 'churn probability with customer revenue' to prioritize retention efforts.



## Project Objectives

The project aims to:

1. Predict the probability of customer churn.
2. Evaluate multiple machine learning models.
3. Estimate Expected Revenue at Risk for each customer.
4. Prioritize customers based on potential financial impact.
5. Simulate different retention strategies.
6. Estimate campaign cost, revenue saved, net profit, and ROI.
7. Translate ML predictions into actionable business recommendations.



## Dataset

The project uses the 'Telco Customer Churn' dataset.

The dataset contains customer-level information including:

* Customer demographics
* Tenure
* Contract type
* Internet service
* Payment method
* Monthly charges
* Total charges
* Churn status

The target variable is:
**Churn**

* Yes → Customer churned
* No → Customer remained



## Project Workflow


Business Problem
       ↓
Data Understanding
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Feature Engineering
       ↓
Model Development
       ↓
Model Evaluation
       ↓
Churn Probability
       ↓
Expected Revenue at Risk
       ↓
Customer Prioritization
       ↓
Retention Strategy Simulation
       ↓
ROI Analysis
       ↓
Business Recommendations



##  Machine Learning Approach

Three classification models were evaluated:

* Logistic Regression
* Random Forest
* XGBoost

The models were evaluated using metrics including:

* ROC-AUC
* Precision
* Recall
* F1-Score
* Accuracy

Model comparison was performed to select the model that provided the most suitable predictive performance for the business problem.



## From Churn Prediction to Revenue Impact

A key part of this project is connecting machine learning predictions to financial impact.

Instead of ranking customers only by their probability of churn, the project calculates:


Expected Revenue at Risk=
Churn Probability × Monthly Charges


This creates a customer-level financial risk score.

A customer with a lower churn probability can still become a higher priority if their monthly revenue contribution is significantly larger.

This shifts the project from:

"Who is likely to churn?"
to:
"Where should the business invest its retention resources?"



## Customer Prioritization

Customers are segmented into:

* High Priority
* Medium Priority
* Low Priority

based on their Expected Revenue at Risk.

This allows customer-success teams to allocate limited retention resources according to potential financial impact rather than treating every customer equally.



## Retention Strategy & ROI Simulation

The project also simulates three hypothetical retention strategies:

| Strategy       |   Cost | Expected Success Rate |
| -------------- | -----: | --------------------: |
| Email Campaign |    Low |                   Low |
| Phone Call     | Medium |                Medium |
| Discount Offer |   High |                  High |

For each strategy, the project estimates:

* Campaign Cost
* Expected Revenue Saved
* Net Profit
* ROI

> Note: Campaign costs and success rates are simulated assumptions for demonstration. In a real business environment, these values should be estimated from historical campaign data.



## Business Impact

The project demonstrates how an organization could use ML predictions to:

* Identify customers at high risk of churn.
* Quantify potential revenue exposure.
* Prioritize high-impact customers.
* Allocate retention resources more efficiently.
* Compare retention strategies based on expected ROI.
* Connect machine learning performance with business outcomes.

The key idea is that model accuracy alone is not the final objective. The model should ultimately help the business make better decisions.



## Key Insights

1. Churn probability is not the same as financial risk

    A customer with a high probability of churn may not represent the highest monetary risk.

2. Customer value should influence prioritization

    Combining churn probability with MonthlyCharges provides a more business-oriented prioritization framework.

3. Retention resources should be allocated selectively

    Expensive interventions should be focused on customers where the potential financial benefit justifies the cost.

4. ML metrics and business metrics should work together

    ROC-AUC, precision, recall and F1-score evaluate model performance, while Revenue at Risk and ROI connect the model to business decisions.



##  Limitations

* Retention campaign costs and success rates are simulated.
* Expected Revenue at Risk is an estimate, not guaranteed future revenue loss.
* The model is evaluated using historical/offline data.
* The analysis does not establish that a retention intervention actually causes a customer to stay.
* Real-world deployment would require monitoring and periodic retraining.



## Future Improvements

Potential future improvements include:

* Using historical retention campaign outcomes.
* Measuring actual customer response to interventions.
* Developing uplift/causal models to identify customers who are most likely to respond to retention actions.
* Adding model monitoring and periodic retraining.
* Optimizing retention decisions directly for financial outcomes.
* Integrating predictions into existing CRM workflows.



##  Technologies Used

1* Python
2* Pandas
3* NumPy
4* Scikit-learn
5* XGBoost
6* Matplotlib
7* Seaborn
8* Jupyter Notebook



## Repository Structure


Customer-Retention-Decision-System/
│
├── Customer_Retention_Decision_System.ipynb
├── README.md
├── requirements.txt
└── data/
    └── WA_Fn-UseC_-Telco-Customer-Churn.csv



##  How to Run

Clone the repository and install the required libraries:

>pip install -r requirements.txt
>Open the notebook:
>Customer_Retention_Decision_System.ipynb
>Run the notebook from beginning to end to reproduce the analysis.



##  Final Takeaway

This project was designed around a simple principle:

> **Machine learning should not stop at predicting an outcome; it should help a business decide what to do next.**

By connecting churn prediction with revenue-at-risk analysis, customer prioritization, and retention ROI, this project demonstrates an approach to ML that considers both **technical performance and business impact**.
