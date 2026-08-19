# Bank_Customer_Churn_Analysis
Overview

This project analyzes a bank's customer ('Bank_Churn_Messy.xlsx)  dataset  to understand who is churning and why. Two raw data sources (customer info and account info) were joined, cleaned, and explored to uncover the demographic and financial patterns behind customer churning, and prepared for future predictive modeling.

Business Need

Losing customers is costly, and it's far cheaper to retain an existing customer than acquire a new one. A bank needs a reliable, unified view of its customer and account data, along with clear insight into which customer segments are most likely to churn, so retention efforts can be targeted rather than applied blindly across the board.

Objectives

Join and QA the Data
Load the raw customer and account datasets
Left join account info to customer info on Customer ID
Check for and remove duplicate rows and columns

Data Cleaning

Check data types for each column and correct as needed
Replace missing values — "MISSING" for categorical fields, median for numeric fields
Profile numeric columns for extreme or non-sensical values and impute with the median
Standardize inconsistent category labels (e.g. combining country name variations under "Geography")

Exploratory Data Analysis (EDA)

Bar chart comparing churners vs. non-churners
Churn rate by Geography and Gender
Box plots for each numeric field, split by churn status
Histograms for each numeric field, split by churn status

Data Prep & Feature Engineering

Drop columns not suitable for modeling
Create dummy variables for categorical fields
Engineer a new "Balance vs. Income" feature (balance ÷ estimated salary) and visualize it against churn status

Key Findings

Germany has a higher churn rate compared to France and Spain
Inactive members (IsActiveMember = No) churn at a noticeably higher rate than active members, suggesting engagement is a strong retention signal.
Churn is not evenly distributed , certain geographies and older customers show meaningfully higher churn rates than others.
Customers with a high balance relative to their income tend to churn more, suggesting financial strain is a contributing factor.
Overall churn rate is about 20% — roughly 1 in 5 customers in the dataset exited the bank.

Tools & Libraries

Python
pandas
numpy
seaborn
matplotlib
