# Global Superstore Power BI Dashboard

> End-to-end Power BI dashboard analyzing **$3.57M profit**, **51K+ orders** across 13 regions - identifying **95% late delivery risk** and sales trends.

### 📸 Dashboard Preview

#### Page 1 - Executive Summary
![Executive Summary](executive%20summary.png)

#### Page 2 - Deep Dive Analysis
![Deep Dive](deep%20view%202.png)

### 🎯 Business Objectives
- Track Sales, Profit & Profit Margin (2015-2018)
- Identify sales trends & seasonality
- Breakdown profit by Category & Region
- Quantify Late Delivery Risk by Region
- Analyze Sales by Segment & Region

### 📐 DAX Measures Used
```DAX
Total Sales = SUM(FactOrders[Sales])
Total Profit = SUM(FactOrders[Profit])
Total Orders = COUNTROWS(FactOrders)
Profit Margin % = DIVIDE([Total Profit], [Total Sales])
Late Delivery % = DIVIDE(CALCULATE(COUNTROWS(FactOrders), FactOrders[Delivery Status]="Late"), [Total Orders])
