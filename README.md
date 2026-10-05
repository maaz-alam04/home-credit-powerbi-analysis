# Home Credit — Loan Portfolio & Credit Risk Analytics

A Power BI analytics project focused on understanding loan applications, customer profiles, credit exposure, repayment behavior, and payment difficulties using the Home Credit Default Risk dataset.

---

## 📊 Project Overview

This project analyzes a large-scale loan portfolio to identify patterns associated with payment difficulties and understand customer credit behavior.

The analysis combines current loan applications with previous applications, external credit records, installment payments, POS/Cash transactions, and credit-card history.

The project demonstrates practical skills in:

- Data cleaning and transformation
- Power Query
- Data modeling
- DAX
- KPI development
- Interactive dashboard design
- Credit risk analysis
- Business-oriented insight generation

---

## 🎯 Business Objective

The primary objective is to identify patterns associated with payment difficulties and understand customer and loan characteristics.

Key questions explored include:

- What percentage of applications experienced payment difficulties?
- How does payment difficulty vary across age and income groups?
- How does credit burden relate to payment difficulty?
- How successful were customers' previous applications?
- What does external credit exposure look like?
- How do customers behave when making installment payments?
- What patterns exist in POS/Cash and credit-card delinquency?

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

The original dataset is several gigabytes in size, so the raw CSV files are **not included in this repository**.

The completed Power BI `.pbix` file is hosted separately through Google Drive.

### 📥 Power BI Dashboard

[Download / Access the Power BI Dashboard](https://drive.google.com/drive/folders/1_UpKUxvFhtk_w1krZRAdYEt_q9fUw4tE?usp=sharing)

> The `.pbix` file is hosted externally because of its large file size.

---

## 🛠️ Tools & Technologies

- **Microsoft Power BI**
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
- Creating sorting columns
- Preparing data for visualization
- Structuring tables for Power BI relationships

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

```text
application_train_clean
│
├── previous_application_clean
│   ├── installments_payments_clean
│   ├── POS_CASH_balance_clean
│   └── credit_card_balance_clean
│
└── bureau_clean
    └── bureau_balance_clean
