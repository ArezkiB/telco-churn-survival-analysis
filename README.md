# telco-churn-survival-analysis
Survival analysis of customer churn using R and Cox Proportional Hazards models.
# Survival Analysis of Telco Customer Churn

##  Project Overview
Customer retention is a critical metric for subscription-based businesses. Traditional predictive models often treat "churn" as a simple binary event (will they leave?), ignoring the dimension of **time** (when will they leave?).

This project applies **Survival Analysis** techniques to the Kaggle Telco Customer Churn dataset to:
1.  Estimate customer retention curves.
2.  Identify significant risk factors using Cox Proportional Hazards models.
3.  Provide actionable business recommendations to maximize **Long-Term Customer Worth**.

## Key Results

### 1. Retention by Contract Type
Contract duration is the strongest predictor of retention.
* **Month-to-month:** High immediate churn risk.
* **1 & 2 Year Contracts:** Protective effect reduces churn hazard by **82%** and **97%** respectively.


### 2. The "Fiber Optic" Problem
Despite being a premium service, **Fiber Optic** internet is associated with a **4x higher risk of churn** compared to DSL. This suggests a disconnect between price and service quality.

### 3. Model Performance
The model is highly effective at distinguishing between low-risk and high-risk customers over time.
* **C-Statistic:** 0.847
* **12-Month AUC:** 0.860
* **36-Month AUC:** 0.879

## 4.Business Recommendations
Based on the survival model, the following actions are recommended:
* **Incentivize Long-Term Contracts:** Aggressively migrate month-to-month users to yearly plans using rate-locks or "first month free" offers.
* **Investigate Fiber Optic:** Urgent satisfaction auditing is needed for fiber users to address the high churn rate.
* **Promote Auto-Pay:** Users on "Electronic Check" are 2x more likely to churn. Incentivize a switch to automatic credit card/bank payments.

## Technologies Used
* **R** (Tidyverse, Survival, Survminer, SurvivalROC)
* **Techniques:** Kaplan-Meier Estimators, Cox Proportional Hazards, Stepwise AIC Selection, Time-Dependent ROC.

## How to Run
1.  Clone the repo.
2.  Ensure you have the required R packages installed:
    ```r
    install.packages(c("tidyverse", "survival", "survminer", "survivalROC"))
    ```
3.  Run the `survival_analysis.R` script.
