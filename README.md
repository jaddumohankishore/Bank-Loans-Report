# 💰 Bank Loans Report Analysis using Power BI

Welcome to the **Bank Loan Analysis Power BI** project repository!  
This project provides **insightful analysis and visualization** of bank loan data using **Power BI**, enabling financial institutions to make **data-driven decisions** and monitor loan portfolio performance effectively.

---

## 🧾 Overview

This Power BI project analyzes various aspects of **bank loans** to provide valuable insights for **decision-making and performance tracking**.  
It comprises **two main dashboards**:

- 📊 **Summary**
- 📈 **Overview**

---

## 🧩 Project Components

| Component | Description |
|------------|-------------|
| **Problem Statement** | Defines the objectives, scope, and expected outcomes of the Bank Loan Analysis. It highlights the need to analyze lending performance, customer repayment behavior, and key financial KPIs. |
| **Query Document (SQL)** | Contains SQL queries used for data cleaning, aggregation, and generating metrics such as total loan amount, repayment trends, and average interest rates. |
| **Financial_Loan Dataset** | The dataset containing loan-related data such as borrower details, loan amount, interest rate, status, DTI ratio, and more. Used as the foundation for SQL querying and Power BI visualization. |

---

## 🎯 Problem Statement

Financial institutions generate large volumes of loan data daily, but deriving actionable insights from this data can be challenging.  
This project aims to analyze and visualize loan-related metrics to answer key business questions such as:

- How many loan applications were received, approved, or charged off?  
- What is the total amount funded and received?  
- Which regions or borrower types contribute most to defaults or repayments?  
- How do factors like **loan purpose**, **home ownership**, and **income** affect loan approval and repayment?

The goal is to provide a **comprehensive Bank Loan Analysis Report** that helps stakeholders **evaluate performance, manage risks, and optimize lending strategies**.

---

## 📊 Dashboard 1: Summary

### **Key Performance Indicators (KPIs)**

1. **Total Loan Applications:**  
   Total number of loan applications received during a specific period, including **Month-to-Date (MTD)** and **Month-over-Month (MoM)** changes.
2. **Total Funded Amount:**  
   Total funds disbursed as loans, including **MTD Funded Amount** and **MoM** analysis.
3. **Total Amount Received:**  
   Total payments received from borrowers, including **MTD Amount Received** and **MoM** comparisons.
4. **Average Interest Rate:**  
   Average interest rate across all loans with **MTD** and **MoM** variation tracking.
5. **Average Debt-to-Income Ratio (DTI):**  
   Average borrower DTI to assess financial stability and risk levels.

### **Summary Visualization**

**Loan Status Grid View:**  
Provides an overview of lending operations categorized by **Loan Status**, displaying key metrics such as:

- Total Loan Applications  
- Total Funded Amount  
- Total Amount Received  
- MTD & MoM KPIs  
- Average Interest Rate  
- Average DTI

---

## 📈 Dashboard 2: Overview

1. **Monthly Trends by Issue Date (Line Chart):**  
   Identify seasonality and long-term lending activity trends.
2. **Regional Analysis by State (Filled Map):**  
   Analyze regions with the highest or lowest lending performance.
3. **Loan Term Analysis (Donut Chart):**  
   Visualize loan distributions across different term lengths (e.g., 36 or 60 months).
4. **Employee Length Analysis (Bar Chart):**  
   Observe how borrower employment stability impacts lending metrics.
5. **Loan Purpose Breakdown (Bar Chart):**  
   Display the distribution of loans based on their stated purpose (education, small business, etc.).
6. **Home Ownership Analysis (Tree Map):**  
   Analyze loan distribution based on home ownership status.

---

## ⚙️ SQL Query Document

The `Query_Document.sql` file contains SQL queries that perform:

- Data extraction and cleaning from the **Financial_Loan Dataset**
- Calculation of **key metrics (KPIs)** such as total loans, average interest rates, and DTI
- Grouping and aggregation by **Loan Status, Purpose, and Region**
- Generating **monthly trend data** for Power BI visuals

### Example SQL Query

```sql
SELECT 
    loan_status,
    COUNT(loan_id) AS Total_Loans,
    SUM(loan_amount) AS Total_Funded_Amount,
    AVG(int_rate) AS Average_Interest_Rate
FROM financial_loan
GROUP BY loan_status;
```
#### Dataset Used:

The bank loan analysis dataset comprises essential fields such as Loan ID, Address State, Purpose, Grade, Sub Grade, Annual Income, Loan Status, Last Payment Date, Verification Status, Debt-to-Income Ratio, and Interest Rates. These fields provide insights into borrower demographics, employment stability, loan characteristics, risk assessment, and payment behavior.

#### Conclusion:

The Details Dashboard streamlines access to critical loan data, facilitating informed decision-making, enhancing operational efficiency, optimizing lending strategies, mitigating risks, and maximizing overall performance.

### Getting Started

1. **Clone the Repository:** Clone this repository to your local machine using `git clone https:github.com/jaddumohankishore/Bank-Loans-Report.
2. **Open the Power BI Project:** Open the `.pbix` file using Power BI Desktop.
3. **Interact with Dashboards:** Explore the interactive dashboards and visualizations to gain insights into bank loan data.

### Adding Images

You can find images of the dashboards in the `Output` directory of this repository.

#### Summary Dashboard
![Summary Dashboard](/output/Summary.png)

#### Overview Dashboard
![Overview Dashboard](/output/Overview.png)

#### Details Dashboard
![Details Dashboard](/output/Details.png)

### Contributing

Contributions to enhance the analysis or add new features are welcome! If you have any suggestions, ideas, or bug fixes, feel free to open an issue or submit a pull request.
