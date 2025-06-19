# Power BI Financial Model

This project presents a dynamic, DAX-powered financial model built in Power BI, designed to analyze business performance through Actual, Budget, and Last Year comparisons. It includes interactive visualizations for P&L, contribution margin, net profit tracking, and detailed cash flow monitoring.

## 📌 Key Features

- **DAX Measures** for:
  - Dynamic Aggregation using SWITCH and SELECTEDVALUE
  - % Contribution Margin & Net Profit calculations
  - Budget vs. Actual vs. Last Year comparisons
  - Cash Flow Computation and Bank Balance Tracking
- **Interactive Slicers** for:
  - Period comparison selection (e.g., Budget vs. Last Year)
  - Dynamic P&L hierarchies
- **Custom Display Folders** and readable format strings for user-friendly insights

## 📊 Data Preparation (Power Query)

The raw financial data required extensive preprocessing before modeling. Using **Power Query**, I performed the following transformations:

- **Combined multiple header rows** into a single row to standardize column names.
- **Removed irrelevant rows** (e.g., metadata, empty or null rows).
- **Applied M language logic** to:
  - Rename and promote headers dynamically.
  - Fill down category fields.
  - Replace errors and standardize data types.
- **Merged datasets** using `Append Queries` and `Merge Queries` to bring in budget vs. actual.
- **Created a custom date table** from scratch using M code, covering:
  - `Date`
  - `Year`
  - `Month`, `MonthNo`
  - `Quarter`, `Day`
  - Relationships established to link transactions and budgets for time intelligence functions.

> These transformations were crucial for ensuring a clean and reliable data model for DAX calculations and accurate dashboard visuals.

## 🧠 Measures Logic Highlight

- `01 Actual`: Calculates running totals per P&L structure
- `02 Actual`: Includes % Contribution Margin and Net Profit
- `03 Actual`: Filters out row-level duplication using `ISINSCOPE`
- `06 Comparison Value`: Toggles between Budget and Last Year
- `07 %Actual Vs Comparison`: % variance using absolute comparison
- `001–004 CashFlow Measures`: Models inflow, outflow, net flow, and rolling bank balances

## 🧮 Tech Stack

- Power BI (Desktop)
- DAX
- Power Query (for ETL)
- Excel (for metadata/dictionary)

## 📸 Screenshots

### Profit & Loss Overview
![Profit & Loss](https://github.com/DennisMochoge/PowerBI-AccountingDashboard/blob/main/Screenshots/Profit%20%26%20Loss.png?raw=true)

### Cash Flow View
![Cash Flow](https://github.com/DennisMochoge/PowerBI-AccountingDashboard/blob/main/Screenshots/CAsh%20Flow.png?raw=true)

## 🔧 How to Use

1. Open the `.pbix` file in Power BI Desktop
2. Connect your data to `fact Transactions`, `fact Budget`, and `dim P&LMask` structure
3. Use the Comparison slicer to toggle periods
4. Explore calculated cash flows and performance metrics


## 👨‍💻 Author

Dennis Atogo Mochoge  
[LinkedIn](https://www.linkedin.com/in/dennismochoge/) | [GitHub](https://github.com/DennisMochoge)
