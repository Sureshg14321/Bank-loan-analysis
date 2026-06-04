# 🏦 Bank Loan Analysis Dashboard

An interactive **Power BI Dashboard** developed to analyze loan portfolio performance, borrower behavior, repayment trends, and lending risk. This project provides actionable insights for financial institutions through dynamic visualizations, KPI tracking, and advanced business analytics.

---

## 📌 Project Overview

The **Bank Loan Analysis Dashboard** is a Business Intelligence solution built using **Power BI** to monitor and evaluate loan performance across multiple dimensions.

The dashboard helps stakeholders:

- Monitor loan applications and funding trends
- Analyze repayment performance
- Identify Good Loans and Bad Loans
- Understand borrower demographics
- Evaluate regional lending patterns
- Support data-driven lending decisions

---

## 🎯 Business Problem

Banks process thousands of loan applications and require a centralized reporting solution to:

- Track loan application trends
- Monitor funded and received amounts
- Identify high-risk loans
- Analyze borrower demographics
- Evaluate repayment performance
- Improve lending strategies

Traditional reporting methods are often static, time-consuming, and lack interactivity. This dashboard addresses these challenges through real-time analytics and intuitive visualizations.

---

## 🚀 Project Objectives

- Analyze overall loan portfolio performance
- Measure funding and repayment trends
- Identify Good Loans and Bad Loans
- Track loan applications across states
- Analyze loan purpose and borrower characteristics
- Provide executive-level insights
- Enable interactive filtering and drill-down analysis

---

## 🛠 Tools & Technologies Used

| Tool | Purpose |
|--------|---------|
| Power BI Desktop | Dashboard Development |
| Power Query | Data Cleaning & Transformation |
| DAX | KPI & Measure Creation |
| Excel / CSV Dataset | Source Data |
| Data Modeling | Relationship Management |

---

## 📊 Data Cleaning & Transformation

### Date Transformation
- Converted Issue Date into Date format
- Created Month and Quarter columns

### Data Type Corrections
- Interest Rate → Decimal Number
- DTI → Decimal Number
- Funded Amount → Currency
- Loan Amount → Currency

### Missing Value Handling
- Checked for null values
- Removed unnecessary blanks

### Feature Engineering
Created:
- Issue Month
- Quarter
- Good Loan Flag
- Bad Loan Flag

---

## 📈 DAX Measures

### Total Loan Applications

```DAX
Total Loan Applications =COUNT(LoanData[id])
```

### Total Funded Amount

```DAX
Total Funded Amount =SUM(LoanData[loan_amount])
```

### Total Amount Received

```DAX
Total Amount Received =SUM(LoanData[total_payment])
```

### Average Interest Rate

```DAX
Average Interest Rate =AVERAGE(LoanData[int_rate])
```

### Average DTI

```DAX
Average DTI =AVERAGE(LoanData[dti])
```

### Good Loan Applications

```DAX
Good Loan Applications =CALCULATE(COUT(LoanData[id]),LoanData[loan_status] IN {"Fully Paid","Current"})
```

### Good Loan Percentage

```DAX
Good Loan % =DIVIDE([Good Loan Applications],[Total Loan Applications])
```

### Bad Loan Applications

```DAX
Bad Loan Applications =CALCULATE(COUNT(LoanData[id]),LoanData[loan_status] = "Charged Off")
```

### Bad Loan Percentage

```DAX
Bad Loan % =DIVIDE([Bad Loan Applications],[Total Loan Applications])
```

---

# 📋 Dashboard Pages

## 1️⃣ Executive Summary

### KPIs
- Total Applications
- Total Funded Amount
- Total Amount Received
- Average Interest Rate
- Average DTI

### Visualizations
- Monthly Application Trend
- Loan Status Distribution
- State-wise Good Loan Analysis
- State-wise Bad Loan Analysis

### Purpose
Provides a high-level overview of the loan portfolio performance.

---

## 2️⃣ Good Loan Analysis

### KPIs
- Good Loan Applications
- Good Loan Funded Amount
- Good Loan Amount Received
- Good Loan Percentage

### Visualizations
- Grade Analysis
- Quarterly Trend Analysis
- State Analysis
- Purpose Analysis
- Home Ownership Analysis

### Purpose
Identifies characteristics of successfully performing loans.

---

## 3️⃣ Bad Loan Analysis

### KPIs
- Bad Loan Applications
- Bad Loan Funded Amount
- Bad Loan Amount Received
- Bad Loan Percentage

### Visualizations
- Grade Analysis
- Quarterly Trend Analysis
- State Analysis
- Purpose Analysis
- Home Ownership Analysis

### Purpose
Analyzes risky and defaulted loans to support risk mitigation strategies.

---

## 4️⃣ Business Analysis

### Visualizations
- Monthly Trend Analysis
- Regional Analysis
- Loan Term Analysis
- Employment Length Analysis
- Loan Purpose Analysis
- Home Ownership Analysis

### Purpose
Provides deep insights into borrower behavior and lending performance.

---

# 🔍 Key Findings

## Loan Portfolio Performance

| Metric | Value |
|----------|----------|
| Total Applications | 39K |
| Total Funded Amount | 436M |
| Total Amount Received | 473M |

### Good Loans
- Approximately **86%** of loans are classified as Good Loans.
- Majority belong to **Grades A and B**.

### Bad Loans
- Approximately **14%** of loans are classified as Bad Loans.
- Higher default risk observed in lower credit grades.

### Loan Purpose
- Debt Consolidation is the most common loan purpose.
- Credit Card and Home Improvement are major categories.

### Home Ownership
- Most borrowers belong to:
  - Mortgage
  - Rent

### Regional Trends
- Certain states contribute significantly higher loan application volumes.

---

# 💼 Business Impact

This dashboard enables stakeholders to:

- Monitor lending performance
- Reduce loan default risk
- Improve approval strategies
- Understand customer borrowing behavior
- Enhance portfolio management
- Support strategic business decisions

---

# 📌 Conclusion

The **Bank Loan Analysis Dashboard** transforms raw loan data into meaningful business insights through interactive visualizations, KPIs, and analytical reports.

The solution provides a comprehensive view of loan performance through:

- Executive Summary
- Good Loan Analysis
- Bad Loan Analysis
- Business Analysis

This dashboard serves as a valuable decision-support tool for banking and financial institutions seeking to optimize lending operations and minimize risk.

---


# 📷 Dashboard Screenshots

## Executive Summary
<img width="1366" height="768" alt="ex sum" src="https://github.com/user-attachments/assets/6d355e7d-25dd-4d6a-ad78-1a1a71433bc7" />

## Good Loan Analysis
<img width="1366" height="768" alt="Goodloan" src="https://github.com/user-attachments/assets/c6416426-1ebb-4332-bb34-a743c6445dff" />

## Bad Loan Analysis
<img width="1366" height="768" alt="badloan" src="https://github.com/user-attachments/assets/a378bd3f-2551-4756-b08f-dc0937df9705" />

## Business Analysis
<img width="1366" height="768" alt="bus analy" src="https://github.com/user-attachments/assets/986554b5-b00b-4500-82a7-e8364de3f8bb" />


---



⭐ If you found this project useful, consider giving it a star on GitHub.
