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

### Dashboard Overview
![Dashboard Overview](Screenshots/dashboard-overview.png)

### Cash Flow View
![Cash Flow](Screenshots/CAsh-Flow.png)

## 🔧 How to Use

1. Open the `.pbix` file in Power BI Desktop
2. Connect your data to `fact Transactions`, `fact Budget`, and `dim P&LMask` structure
3. Use the Comparison slicer to toggle periods
4. Explore calculated cash flows and performance metrics

## 📜 License

MIT License. See `LICENSE` for more information.

## 👨‍💻 Author

Dennis Atogo Mochoge  
[LinkedIn](https://www.linkedin.com/in/dennismochoge/) | [GitHub](https://github.com/DennisMochoge)
