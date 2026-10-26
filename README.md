# Credit Card Fraud Analysis
SQL + pandas analysis of credit card fraud data with visualizations

## Overview
Exploratory analysis of a credit card fraud dataset to identify which customer segments (gender, age, state, day of week, month) are most affected by fraud in terms of frequency and severity. The goal is to answer: **which segments should fraud detection prioritise?**

## Data
- **Source:** credit_card_fraud_detection_2026.csv
- **Size:** 1000 rows × 25 columns
- **Key columns:** `fraud_amount_lost`, `customer_age`, `customer_gender`, `customer_state`, `transaction_day_of_week`, `transaction_datetime`

## Setup
1. Clone this repo
2. Install dependencies:
   ```bash
   pip install pandas ipython-sql matplotlib
3.Download the CSV from the source above and place it in the project folder
4.Open credit_card_fraud.ipynb in Jupyter and run all cells top to bottom

Key Findings
Gender: Gender: Females are the most frequently targeted group by fraud events, while the "Other" category has the highest average loss per event.
State: Nebraska has the most fraud events (77 total), while Los Angeles has the highest average loss per event ($328).
Age: 75 suffers the largest average loss per fraud event ($474).
Day of week: Fraud events peak on Saturday, suggesting weekend transactions are less monitored.
Monthly pattern: Total losses peak in January, with $32358 in total fraud losses.
Distribution: The mean loss is $136 but the median is only $50 — the distribution is heavily right-skewed, meaning a small number of very large events drive the average upward.
Visualizations
Fraud Events by Day of Week

Top 10 States by Fraud Events

Distribution of Fraud Losses

Monthly Fraud Losses

Methodology
EDA — checked shape, missing values (only browser had 41,709 nulls, irrelevant to analysis), and summary statistics
Targeted SQL queries — GROUP BY / AVG / SUM / COUNT across gender, state, age, day of week, and month
Skewness check — compared mean vs median to identify outlier-driven averages
Visualization — matplotlib bar charts, histogram, and line chart
