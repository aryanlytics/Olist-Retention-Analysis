# Olist_Retention_Analysis

## Project Overview
This project diagnoses the root cause of a critical business issue for the Olist Marketplace: $68\%$ of first-time customers fail to make a second purchase.
The analysis isolates the true drivers of churn to provide a strategic, constraint-aware recommendation that targets an estimated $3.6 Million Annual GMV opportunity.

## The Problem Statement
The Churn Crisis: 
Olist has a $68\%$ first-purchase churn rate, leading to unsustainably high customer acquisition costs.
The Core Question: 
Is this retention failure due to Operational issues (like late delivery, low seller quality) or Structural issues (like the mix of products sold)?
The Constraint: 
As a SaaS platform, Olist cannot control logistics or delivery carriers. The solution must focus on factors within Olist's control.

## Analytical Findings (The Proof)
The Logistic Regression model was used to prove the dominance of structural factors over operational factors.

Factor Type       	                     Key Metric	                Finding	                                                            Impact
Structural (Product Category)            Odds Ratio (OR)            Best categories (Computers) have an $\text{OR}$ of $0.248$.         Reduces the odds of churn by $75.2\%$.
Operational (Late Delivery)              Odds Ratio (OR)            A late delivery (is_late) has an $\text{OR}$ of $3.09$.             Increases the odds of churn by $209\%$.





