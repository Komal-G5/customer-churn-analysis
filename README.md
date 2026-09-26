# Customer Churn Analysis

## Project Overview

An end-to-end customer churn analysis project designed to identify customer segments with higher observed churn, understand factors associated with customer attrition, and quantify potential revenue exposure.

The project combines customer, subscription, revenue, support, satisfaction, and churn-risk data using **Python, SQL, SQLite, Pandas, Matplotlib, and Seaborn**.

The analysis follows a practical analytics workflow:

**Data Extraction → Data Cleaning → Data Integration → Feature Engineering → Exploratory Analysis → KPI Analysis → Visualization → Business Insights**

---

## Business Problem

Customer churn can directly affect recurring revenue and customer lifetime value.

The objective of this analysis is to understand:

* How frequently customers are churning
* Which customer segments show higher observed churn
* How contract and plan types relate to churn
* How customer satisfaction is associated with churn
* How much monthly revenue is associated with churned customers
* How many customers are currently classified as high churn risk

These findings can help inform further customer-retention analysis and prioritization.

---

## Project Objectives

* Calculate overall customer churn and retention KPIs
* Identify churn patterns across customer segments
* Analyze churn by plan, contract, subscription type, and state
* Examine the relationship between customer satisfaction and churn
* Analyze customer tenure and age
* Quantify monthly revenue exposure associated with churn
* Evaluate customer churn-risk distribution
* Analyze customer value using CLTV
* Create business-focused visualizations for decision support

---

## Dataset

The project uses a SQLite database containing three related tables:

* `db_customer`
* `db_subscription`
* `db_support`

An additional CSV dataset was integrated into the analysis.

After data integration and duplicate resolution, the final analysis contains:

**507 unique customers**

### Key Data Areas

**Customer Data**

* Customer ID
* Name
* Country
* State
* Gender
* Date of Birth

**Subscription Data**

* Subscription Start Date
* Subscription Type
* Plan Type
* Contract Type
* Renewal Date
* Cancellation Date
* Monthly Charges
* CLTV
* Churn Score
* Cancellation Reason

**Support Data**

* Complaint Date
* Escalations
* CSAT Score
* Customer Comments

---

## Tools & Technologies

| Category        | Tools               |
| --------------- | ------------------- |
| Programming     | Python              |
| Database        | SQLite              |
| Query Language  | SQL                 |
| Data Analysis   | Pandas, NumPy       |
| Visualization   | Matplotlib, Seaborn |
| Development     | Jupyter Notebook    |
| Version Control | Git, GitHub         |

---

## Data Preparation & Feature Engineering

The analysis included:

* Multi-table data integration using SQL/Pandas
* Data cleaning and standardization
* Missing-value handling
* Duplicate customer resolution
* Date conversion and validation
* Customer age calculation
* Customer tenure calculation
* Churn flag creation
* Churn-risk categorization
* CSAT grouping
* Monthly churn-period extraction
* Revenue exposure calculations

These transformations converted the raw customer data into an analysis-ready dataset.

---

## Key KPIs

| KPI                                    |     Result |
| -------------------------------------- | ---------: |
| Unique Customers                       |        507 |
| Overall Churn Rate                     |     30.77% |
| Average Customer Age                   | 42.2 years |
| Average Tenure                         | 1,454 days |
| Monthly Revenue                        |   7,117.93 |
| Monthly Revenue at Risk                |   2,026.44 |
| Revenue Churn Rate                     |     28.47% |
| Average CLTV                           |     794.82 |
| High-Risk Customers                    |        116 |
| Monthly Charges of High-Risk Customers |   1,477.84 |

---

## Churn Analysis

### Churn by Contract Type

Observed churn rate:

* Monthly: **39.77%**
* Annual: **20.99%**

Monthly-contract customers showed a higher observed churn rate than annual-contract customers in this dataset.

### Churn by Plan Type

* Basic: **37.22%**
* Standard: **28.97%**
* Premium: **23.89%**

### Churn by Subscription Type

* Paid: **35.87%**
* Refferal: **29.37%**
* Organic: **26.90%**

### Customer Satisfaction

The analysis grouped customers into Low, Medium, and High CSAT categories.

Observed churn rates were substantially different across these groups, with the Low-CSAT group showing the highest observed churn.

---

## Revenue & Customer Risk Analysis

The analysis goes beyond calculating churn percentages by examining potential financial exposure.

Key findings include:

* Approximately **2,026.44** in monthly charges are associated with churned customers.
* **116 customers** are classified as high churn risk.
* These high-risk customers represent approximately **1,477.84** in monthly charges.
* Average CLTV across customers is **794.82**.
* Average CLTV among churned customers is **433.63**.

This provides a financial perspective on customer churn rather than treating churn only as a percentage metric.

---

## Visual Analysis

The project includes visualizations covering:

* Monthly Customer Churn Trend
* Churn Rate by Plan Type
* Churn Rate by State
* Churn Rate by Contract Type
* Churn Rate by Subscription Type
* Customer Churn Risk Distribution
* Monthly Revenue Exposure by Churn Risk
* Complaint Distribution by Churn Status
* Churn Rate by CSAT Group
* Correlation Heatmap
* Monthly Charges by Plan and Churn Risk

All visualizations are available in the `visuals/` directory.

---

## Key Business Insights

* The overall observed customer churn rate is **30.77%** across 507 unique customers.
* Monthly-contract customers have a substantially higher observed churn rate than annual-contract customers.
* Basic-plan customers have the highest observed churn rate among the analyzed plans.
* Paid subscribers show the highest observed churn rate among the analyzed subscription types.
* Customer satisfaction shows a strong association with observed churn in this dataset.
* **2,026.44** in monthly charges are associated with churned customers.
* **116 customers** are classified as high churn risk, representing approximately **1,477.84** in monthly charges.

> **Note:** These are observed relationships within this dataset and should not automatically be interpreted as causal relationships.

---

## Project Structure

```text
customer-churn-analysis/
│
├── data/
│   ├── customer_churn.db
│   └── customer_churn_merged_500_rows.csv
│
├── notebooks/
│   ├── churn_analysis_.ipynb
│   └── exported_churn_data_.csv
│
├── visuals/
│   ├── 4.1 Monthly_Customer_Churn_Trend_(Time_Series_KPI).png
│   ├── 4.2 Churn_Rate_by_Plan_Type.png
│   ├── 4.3 Churn_Rate_by_State.png
│   ├── 4.4 Churn_Rate_by_Contract_Type.png
│   ├── 4.5 Churn_Rate_by_Gender.png
│   ├── 4.6 Churn_Rate_by_Subscription_Type.png
│   ├── 4.7 Customer_Churn_Risk_Distribution.png
│   ├── 4.8 Monthly_Revenue_Exposure_by_Churn_Risk.png
│   ├── 4.9 Churn_Rate_vs_CSAT_Score.png
│   ├── 4.10 Churn_Rate_by_CSAT_Group.png
│   ├── 4.11 Complaint_Distribution_by_Churn_Status.png
│   ├── 4.12 Correlation_Heatmap.png
│   └── 4.13 Monthly_Charges_by_Plan and Churn_Risk.png
│
├── .gitignore
├── requirements.txt
└── README.md
```

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Komal-G5/customer-churn-analysis.git
cd customer-churn-analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/churn_analysis_.ipynb
```

### 4. Run the notebook

Run the notebook from top to bottom to reproduce the analysis.

The project uses relative paths so that the notebook can be executed from the project structure without relying on machine-specific absolute file paths.

---

## Skills Demonstrated

This project demonstrates practical experience with:

* Python for data analysis
* SQL-based data extraction and transformation
* SQLite database handling
* Pandas data manipulation
* Data cleaning and preprocessing
* Multi-table joins
* Duplicate resolution
* Feature engineering
* Exploratory Data Analysis
* KPI development
* Customer segmentation
* Revenue analysis
* Churn-risk analysis
* Data visualization
* Business insight generation
* Git and GitHub workflow

---

## Future Improvements

Potential extensions include:

* Building an interactive Power BI dashboard
* Developing a predictive churn model using machine learning
* Performing cohort-based retention analysis
* Creating automated KPI reporting
* Adding customer-level retention recommendations
* Evaluating model performance using appropriate classification metrics

---

## Conclusion

This project demonstrates an end-to-end approach to customer churn analysis, from integrating raw customer data and preparing analysis-ready datasets to calculating business KPIs and communicating actionable patterns through visualizations.

The analysis provides a combined view of **customer behavior, subscription characteristics, revenue exposure, customer satisfaction, support activity, and churn risk**, creating a foundation for deeper retention and predictive analytics.
