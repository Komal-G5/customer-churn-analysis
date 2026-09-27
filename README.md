# Customer Churn Analysis

> **End-to-end customer churn analytics project** focused on identifying churn patterns, customer risk segments, retention trends, and revenue exposure using Python, SQL, SQLite, Pandas, Matplotlib, and Seaborn.

### 📌 Project Snapshot

| Metric                  |       Result |
| ----------------------- | -----------: |
| Customers Analyzed      |      **507** |
| Overall Churn Rate      |   **30.77%** |
| Monthly Revenue at Risk | **2,026.44** |
| High-Risk Customers     |      **116** |

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

## 📊 Visual Analysis

The analysis includes business-focused visualizations covering **churn trends, customer risk, revenue exposure, subscription behavior, satisfaction, and customer support patterns**.

### Churn & Retention

| Analysis                        | Visualization                                        |
| ------------------------------- | ---------------------------------------------------- |
| Monthly Customer Churn Trend    | Time-series analysis of monthly churn                |
| Churn Rate by Plan Type         | Comparison across Basic, Standard, and Premium plans |
| Churn Rate by Contract Type     | Comparison of Monthly vs Annual contracts            |
| Churn Rate by Subscription Type | Comparison across acquisition/subscription types     |

### Customer Risk & Revenue

| Analysis                               | Visualization                                        |
| -------------------------------------- | ---------------------------------------------------- |
| Churn Risk Distribution                | Distribution of Low, Medium, and High-risk customers |
| Monthly Revenue Exposure by Churn Risk | Revenue associated with different risk segments      |
| Monthly Charges by Plan & Churn Risk   | Relationship between plan charges and customer risk  |

### Customer Experience

| Analysis                               | Visualization                                              |
| -------------------------------------- | ---------------------------------------------------------- |
| Churn Rate by CSAT Group               | Churn patterns across satisfaction groups                  |
| Churn Rate vs CSAT Score               | Relationship between satisfaction score and observed churn |
| Complaint Distribution by Churn Status | Complaint patterns across churn status                     |

### Additional Analysis

* Churn Rate by State
* Churn Rate by Gender
* Correlation Heatmap

All visualizations are available in the [`visuals/`](./visuals/) directory.


---

## 📈 Executive Visuals

### Monthly Churn Trend

![Monthly Customer Churn Trend](./visuals/4.1%20Monthly_Customer_Churn_Trend_%28Time_Series_KPI%29.png)

### Churn Rate by Contract Type

![Churn Rate by Contract Type](./visuals/4.4%20Churn_Rate_by_Contract_Type.png)

### Churn Risk Distribution

![Customer Churn Risk Distribution](./visuals/4.7%20Customer_Churn_Risk_Distribution.png)

### Monthly Revenue Exposure by Churn Risk

![Monthly Revenue Exposure by Churn Risk](./visuals/4.8%20Monthly_Revenue_Exposure_by_Churn_Risk.png)

---

## 💡 Key Business Insights

### 1. Contract Type & Churn

Monthly-contract customers showed a higher observed churn rate (**39.77%**) compared with annual-contract customers (**20.99%**).

**Business implication:** Short-term contracts may represent a higher-retention-risk segment and could be useful for targeted retention and contract-conversion analysis.

### 2. Plan-Level Churn

The Basic plan recorded the highest observed churn rate (**37.22%**), followed by Standard (**28.97%**) and Premium (**23.89%**).

**Business implication:** Plan-level churn patterns can help identify segments that require deeper investigation into pricing, benefits, usage, or customer experience.

### 3. Customer Risk & Revenue Exposure

The dataset contains **116 high-risk customers**, associated with approximately **1,477.84 in monthly charges**.

**Business implication:** Customer risk segmentation can be combined with revenue exposure to prioritize retention analysis based on both customer risk and financial impact.

### 4. Churn & Revenue Impact

The overall observed churn rate was **30.77%**, while monthly revenue associated with churned customers was approximately **2,026.44**.

**Business implication:** Churn analysis should consider both customer volume and financial exposure rather than relying only on churn percentage.

### 5. Customer Satisfaction

Customers in the lower CSAT groups showed substantially higher observed churn than customers in the high-CSAT group.

**Business implication:** Customer satisfaction can be monitored alongside churn metrics to identify potential customer-experience risk areas.

### 6. CLTV & Churn

Average CLTV among churned customers (**433.63**) was lower than the overall average CLTV (**794.82**).

**Business implication:** CLTV and churn should be analyzed together to understand whether customer attrition is concentrated among lower-value or strategically important customer segments.

> **Note:** These findings describe observed relationships in the dataset and should not be interpreted as proof of causation.


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

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Komal-G5/customer-churn-analysis.git
cd customer-churn-analysis
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it:

**macOS / Linux**

```bash
source .venv/bin/activate
```

**Windows**

```bash
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/churn_analysis_.ipynb
```

### 5. Run the Analysis

Run the notebook cells sequentially.

The notebook performs:

**Data Extraction → Data Cleaning → Data Integration → Feature Engineering → Exploratory Analysis → KPI Analysis → Visualization → Business Insights**

The project uses relative project paths, so the analysis does not depend on the original local computer location.

### 6. Project Outputs

Generated analysis outputs and visualizations are available in:

```text
visuals/
```

The repository also includes the processed analysis notebook and supporting datasets required for the project.

---

## 🧠 Skills Demonstrated

### Data & SQL

* SQL-based data extraction and querying
* Multi-table data integration using relational keys
* SQLite database analysis
* Data validation and consistency checks

### Python & Data Analysis

* Pandas-based data manipulation and transformation
* NumPy-based numerical analysis
* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Feature engineering
* Date/time-based analysis

### Statistical & Analytical Techniques

* KPI calculation and metric design
* Churn and retention analysis
* Customer segmentation
* Correlation analysis
* Distribution analysis
* Trend analysis
* Risk segmentation
* Revenue exposure analysis

### Data Visualization

* Matplotlib
* Seaborn
* Time-series visualization
* Categorical comparison
* Risk and revenue visualization
* Correlation heatmaps

### Business Analytics

* Translating business questions into analytical metrics
* Identifying high-risk customer segments
* Connecting customer churn with revenue exposure
* Comparing customer, subscription, contract, and satisfaction patterns
* Converting analytical findings into business-focused insights

### Analytics Workflow

**Raw Data → SQL Extraction → Data Cleaning → Data Integration → Feature Engineering → EDA → KPI Analysis → Visualization → Business Insights**

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
