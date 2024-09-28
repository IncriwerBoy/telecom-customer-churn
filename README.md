# Telecom Customer Churn Analysis

## Project Overview

This project focuses on analyzing customer churn data for a telecom company. The goal is to explore the patterns of churn behavior and identify key factors contributing to customer attrition. Through the use of Exploratory Data Analysis (EDA) and handling missing values, insights are derived to better understand customer churn, guiding strategies to improve retention.

## Dataset

The dataset includes customer-level information such as demographics, services subscribed, payment methods, and churn status. The key columns are:
- **Customer ID**: Unique customer identifier.
- **Demographics**: Gender, Age, Marital Status.
- **Services**: Internet Type, Phone Service, Streaming Services, etc.
- **Monthly Charges**: Total monthly charge paid by the customer.
- **Churn Status**: Whether the customer has churned or is still active.

### Key Features with Missing Data:
- **Offer**: 3,877 missing values
- **Avg Monthly Long Distance Charges**: 682 missing values
- **Multiple Lines**: 682 missing values
- **Internet Type**: 1,526 missing values
- **Churn Category**: 5,174 missing values
- **Churn Reason**: 5,174 missing values

## Project Steps

### 1. **Handling Missing Values**
   - **Offer**: Since offers are specific to certain campaigns, missing values are imputed as "No Offer."
   - **Avg Monthly Long Distance Charges** & **Multiple Lines**: Missing values are likely customers without long-distance services. Imputed as 0 or "No Multiple Lines."
   - **Internet Service Columns**: Missing values in columns like `Internet Type`, `Online Security`, `Device Protection Plan`, etc., are filled as "No Internet."
   - **Churn Category** & **Churn Reason**: Missing values correspond to customers who haven't churned and are filled as "Not Applicable."

### 2. **Exploratory Data Analysis (EDA)**

#### Key Visualizations:

- **Churn Rates by Gender**: 
   - A **stacked bar plot** shows churn rates for males vs. females. This highlights how gender impacts churn behavior.

- **Density of Monthly Charges by Churn Status**:
   - A **KDE plot** shows the distribution of monthly charges across churned and active customers. This gives insights into the pricing patterns that could influence churn.

- **Churn vs. Tenure**:
   - Analyzed the relationship between how long a customer stays with the company and their likelihood to churn, using scatter plots and bar charts.

- **Internet Services and Churn**:
   - Investigated how internet-related services (e.g., Internet Type, Streaming Services) influence churn rates through heatmaps and bar plots.

### 3. **Insights from EDA**

- **Churn by Monthly Charges**: Customers with higher monthly charges tend to churn more frequently, as indicated by a higher density of churned customers in the KDE plot for `Monthly Charge`.
  
- **Gender and Churn**: The stacked bar plot shows that churn rates are slightly higher among female customers than male customers, though the overall difference isn't drastic.

- **Impact of Tenure**: Customers with shorter tenures (i.e., those who have been with the company for a shorter period) tend to churn more, showing that retention efforts should be focused on newer customers.

### 4. **Next Steps**

- Further analysis to identify key churn predictors using machine learning algorithms.
- Develop models for predicting churn probability and providing business recommendations based on the findings.

---

## Tools & Libraries

- **Python**: Used for data analysis and visualization.
- **Pandas**: Data manipulation and cleaning.
- **Matplotlib & Seaborn**: For creating visualizations (bar plots, KDE plots, etc.).
- **Jupyter Notebook**: For running and documenting the analysis.

---

This project showcases key EDA techniques and strategies for handling missing data, helping telecom companies improve customer retention by understanding churn drivers.
