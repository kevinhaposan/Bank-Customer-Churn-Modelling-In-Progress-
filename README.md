# **Bank-Customer-Churn-Modelling**
Note: This content is in progress

## **A. Introduction**
## A1. Background
Technological developments and increasingly fierce competition are pushing companies not only to focus on acquiring new customers but also on retaining existing ones. Raka Bank is one startup company that focuses on this problem. Based on the data the company has, **RakaBank has a churn rate of 20.37%**. Generally, startup banks believe that an **annual churn rate of less than 15% is acceptable**. 

Raka Bank wants to identify which aspects encourage customers to churn so that they can provide the right solution to prevent customers from churning. Raka Bank has asked Data Lovelace for help to predict and identify factors that encourage customers to churn.

## A2. Goals
Decrease churn rate from 20.37% to at least under 15% in order to reduce cost.

## A3. Objective
Create a model machine learning to predict potential customer churn and identity the factors of customer churn.

## A4. Business Metric
Churn Rate (%)

## **B. Exploratory Data Analysis**
## B1. Descriptive Statistics

About dataset:<br>
This dataset was taken from [Kaggle](https://www.kaggle.com/code/mathchi/churn-problem-for-bank-customer/input?select=churn.csv)
- The dataset consist of 10,000 rows and 14 columns.
- The dataset consist of 10,000 rows and 14 columns.
- Target variabel is the Exited columns.

## B2. Univariate Analysis
### B2.1 Numerical Univariate Statistics
![image](https://github.com/kevinhaposan/Bank-Customer-Churn-Modelling-In-Progress-/assets/156397084/5622e061-8ef3-4ac5-8fe5-29222d650599)
<br>
![image](https://github.com/kevinhaposan/Bank-Customer-Churn-Modelling-In-Progress-/assets/156397084/f8565491-dacd-46fd-b72c-ff885157999f)
<br>
Based on the analysis using Numerical - Univariate Statistics, it was found that:
- Credit Score shows a Normal distribution (No Skew), Age shows a Positively Skewed distribution, and Balance shows a Bimodal distribution.
- The dominant values for Credit Score fall within the range of 600-700, while for Balance, the frequencies are observed around 0 and within the range of 100,000-150,000.
- Age and Credit Score are considered not to have outliers because their values do not differ significantly within the data.

### B2.2 Categorical Statistics
![image](https://github.com/kevinhaposan/Bank-Customer-Churn-Modelling-In-Progress-/assets/156397084/c590e0f0-5233-4470-a517-055ce03b11e0)
<br>
Based on the analysis using Categorical - Univariate Statistics, the following findings were obtained:
Dominant Values:
- Geography: France
- Gender: Male
- InActiveMember & HasCrCard: Those who possess (1)
- Exited: Non-churning customers (0)

Follow-up steps during data processing are:
- Filtering outlier data
- Performing feature transformation such as normalization or standardization
- Creating feature encoding for model development
- Addressing class imbalance.

## B3. Multivariate Analysis
### B3.1 Heatmap
![image](https://github.com/kevinhaposan/Bank-Customer-Churn-Modelling-In-Progress-/assets/156397084/d3e8d99d-4d72-4f29-a62d-7a49b2f17942)

### B3.2 Pairplot
![image](https://github.com/kevinhaposan/Bank-Customer-Churn-Modelling-In-Progress-/assets/156397084/fe543522-e0f3-4c0d-a90d-7c5ced9cf217)
<br>

Correlation of each feature:
Age and Balance show the highest positive correlation value, indicating that as the age and balance increase, the churn rate will also increase.
IsActiveMember shows a correlation value of -0.16 and a negative correlation, suggesting that if the customer is not active, the likelihood of churn will increase.
As for Credit Score, Tenure, NumofProducts, Has Credit Card, and Estimated Salary, they show very small values < 0.1.

No interesting patterns: in the pairplot, there are no clusters of straight points.
