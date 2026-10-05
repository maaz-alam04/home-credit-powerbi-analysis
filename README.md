# Home Credit — Loan Portfolio & Credit Risk Analytics

A Power BI analytics project focused on understanding loan applications, customer profiles, credit exposure, repayment behavior, and payment difficulty using the Home Credit Default Risk dataset.

---

## 📊 Project Overview

This project analyzes a large-scale loan portfolio to identify patterns associated with payment difficulties and understand customer credit behavior.

The dashboard combines loan application data with previous applications, external credit records, installment payments, POS/Cash transactions, and credit-card history.

The analysis was designed as a portfolio project to demonstrate practical skills in:

- Data cleaning and transformation
- Data modeling
- Power Query
- DAX
- KPI development
- Interactive dashboard design
- Credit risk analysis
- Business-oriented insight generation

---

## 🎯 Business Objective

The primary objective is to analyze customer and loan characteristics and identify patterns associated with payment difficulties.

Key questions explored include:

- What percentage of applications experienced payment difficulties?
- How does payment difficulty vary across age and income groups?
- How does credit burden relate to payment difficulty?
- How successful were customers' previous applications?
- What does external credit exposure look like?
- How do customers behave when making installment payments?
- What patterns exist in POS/Cash and credit-card delinquency?
- How do repayment behaviors differ between customer groups?

---

## 🗂️ Dataset

The project uses the **Home Credit Default Risk** dataset from Kaggle.

The dataset contains multiple related tables covering:

- Current loan applications
- Previous loan applications
- External credit bureau records
- Bureau balance history
- Installment payments
- POS/Cash balance
- Credit-card balance

Due to the large size of the original dataset, the raw CSV files are **not included in this repository**.

The Power BI `.pbix` file is available separately through Google Drive.

---

## 🛠️ Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX**
- **Microsoft Excel / CSV**
- **GitHub**

---

## 🧹 Data Preparation

Data preparation was performed using Power Query.

Major transformation steps included:

- Data type validation
- Handling missing and null values
- Replacing selected categorical nulls with `Unknown`
- Preserving meaningful numeric nulls
- Removing unnecessary columns
- Creating analytical columns
- Creating categorical groups
- Preparing fields for visualization
- Creating sorting columns for ordered categories
- Structuring the data for Power BI relationships

### Derived Fields

Examples of analytical fields created include:

- `AGE_YEARS`
- `AGE_GROUP`
- `EMPLOYMENT_STATUS`
- `YEARS_EMPLOYED`
- `INCOME_GROUP`
- `CREDIT_TO_INCOME`
- `CREDIT_BURDEN_GROUP`
- `PAYMENT_DIFFICULTY_STATUS`
- `PAYMENT_TIMING`
- `PAYMENT_DELAY_GROUP`
- `PAYMENT_AMOUNT_STATUS`
- `DPD_STATUS`
- `CC_DPD_STATUS`

---

## 🔗 Data Model

The Power BI model uses a relational structure connecting the current application table with historical credit and repayment tables.

### Main relationships

```text
application_train_clean
        │
        ├── previous_application_clean
        │          │
        │          ├── installments_payments_clean
        │          ├── POS_CASH_balance_clean
        │          └── credit_card_balance_clean
        │
        └── bureau_clean
                   │
                   └── bureau_balance_clean

The model uses appropriate one-to-many relationships based on customer and previous-application identifiers.
📐 DAX & KPIs
Key measures were created using DAX, including:
- Total Applications
- Payment Difficulties
- Payment Difficulty Rate
- Total Credit
- Average Credit
- Average Income
- Total Previous Applications
- Approved Previous Applications
- Previous Approval Rate
- Active External Credits
- Total Outstanding Debt
- Total Overdue Amount
- Average Payment Delay
- Total Amount Paid
Additional measures were created to analyze payment difficulty across payment behavior and delinquency categories.
📊 Dashboard
The final dashboard contains four analytical pages.
1. Executive Overview
Focus: Customer profile, credit exposure, and overall payment difficulty.
KPIs
- 308K Total Applications
- 25K Payment Difficulties
- 8.07% Payment Difficulty Rate
- 184.21B Total Credit
- 599.03K Average Credit
- 168.80K Average Income
Analysis
- Payment difficulty by age group
- Payment difficulty by income group
- Payment difficulty by credit burden
2. Customer & Credit Risk Profile
Focus: Previous applications and external credit exposure.
KPIs
- 199.97B Total Outstanding Debt
- 65M Total Overdue Amount
Analysis
- Previous applications by approval status
- Previous approval rate by payment difficulty
- External credit records by status
3. Loan & Repayment Performance
Focus: Installment payment behavior and repayment accuracy.
Analysis
- Installment payment delay severity
- Payment difficulty by payment amount status
- Installment payment timing distribution
- Installment payment amount distribution
- Average payment timing
Key repayment observations include:
- A large majority of installment records were paid early.
- Most payment records matched the installment amount exactly.
- A smaller proportion of records were underpaid or paid late.
4. Delinquency & Credit Behavior
Focus: Delinquency patterns across POS/Cash and credit-card portfolios.
Analysis
- Payment difficulty by credit-card delinquency
- Credit-card delinquency distribution
- Credit-card records by contract status
- Payment difficulty by POS/Cash delinquency
- POS/Cash delinquency distribution
The analysis focuses on identifying patterns rather than assuming that delinquency categories directly cause payment difficulties.
🔍 Key Insights
Customer Risk
- Overall payment difficulty rate was approximately 8.07%.
- Younger applicants showed higher payment difficulty rates than older applicants.
- The 18–25 age group had the highest observed rate at approximately 11.74%, while the 56+ group had approximately 5.17%.
Income & Credit Burden
- Lower-income groups generally showed higher payment difficulty rates.
- The 500K+ income group had an observed rate of approximately 5.40%.
- Credit burden showed variation across categories, with the 3x–4x group showing the highest observed rate at approximately 8.85%.
Previous Applications
- Approximately 62% of previous applications were approved.
- Customers without current payment difficulties had a higher previous approval rate (~63%) compared with customers experiencing payment difficulties (~55%).
Repayment Behavior
- Approximately 68% of installment records were paid early.
- Approximately 23% were paid on time.
- Approximately 8% were paid late.
- Around 89% of payment records matched the expected installment amount exactly.
Credit Exposure
- External credit records were dominated by closed accounts, followed by active accounts.
- Total outstanding debt across bureau records was approximately 199.97B.
⚠️ Analytical Notes
Some metrics in this project represent records rather than unique customers.
For example, installment, POS/Cash, credit-card, and bureau tables can contain multiple records for the same customer.
Therefore:
Observed relationships should be interpreted as associations in the dataset, not as proof of causation.

Payment difficulty rates calculated across payment or delinquency categories are based on customers associated with those categories, and customers may appear in multiple categories.
📷 Dashboard Preview
Screenshots of all four dashboard pages are available in the screenshots folder.
Dashboard Pages
1. Executive Overview
2. Customer & Credit Risk Profile
3. Loan & Repayment Performance
4. Delinquency & Credit Behavior
📥 Power BI File
The complete .pbix file is available through Google Drive:
Download / Access Power BI Dashboard
The PBIX file is hosted externally because of its large file size.

🚀 How to Use
1. Download the .pbix file from the link above.
2. Open it using Microsoft Power BI Desktop.
3. Explore the four dashboard pages.
4. Use the interactive visuals and filters to investigate customer and credit-risk patterns.
📚 Skills Demonstrated
Data Analytics
- Data Cleaning
- Exploratory Data Analysis
- Credit Risk Analysis
- KPI Analysis
- Business Intelligence
- Data Visualization
Power BI
- Power Query
- Data Modeling
- DAX
- Calculated Columns
- Measures
- Interactive Dashboards
- Slicers & Filters
- Data Relationships
👨‍💻 Author
Maaz Alam
B.Tech — Computer Science & Engineering
Interested in Data Analytics, Business Intelligence, and Data Science.
