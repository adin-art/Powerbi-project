# 📊 Sales Performance Dashboard | Power BI Project

## 🔎 Project Summary

This project is an interactive **Sales Performance Dashboard** built using Power BI to analyze revenue, profitability, order volume, and regional performance.

The goal of this project was to simulate a real-world business scenario where stakeholders need quick access to KPIs and performance insights to support strategic decision-making.

---

## 🖼 Dashboard Preview

![Sales Dashboard Overview](overview.png)

> Make sure `overview.png` is uploaded in the same repository folder as this README file.

---

## 🎯 Business Objectives

- Track overall company sales and profitability
- Compare performance across regions and countries
- Monitor monthly trends and sales targets
- Identify category-level contribution to revenue
- Analyze profit margin consistency

---

## 📌 Key Performance Indicators (KPIs)

| Metric | Value |
|--------|-------|
| Total Sales | 70.64M |
| Total Profit | 25.12M |
| Total Orders | 100K |
| Sales Variance | 378.33K |
| Profit Margin | 36% |

---

## 📊 Dashboard Features

### 1️⃣ Sales by Category
- Revenue breakdown across product categories
- Helps identify high-performing product lines

### 2️⃣ Profit vs Quantity Analysis
- Scatter plot visualization
- Regional comparison of profitability and volume
- Detects performance clusters and outliers

### 3️⃣ Regional Sales Distribution
- Donut chart representation
- Balanced contribution (~20% per region)

### 4️⃣ Country-Level Quantity Analysis
- Geographic distribution of order quantities
- Enables international performance tracking

### 5️⃣ Monthly Trend Analysis
- Sales trends over time
- Target vs actual comparison
- Sales variance monitoring
- Profit margin stability tracking

---

## 🛠 Technical Skills Demonstrated

- **Power BI Dashboard Design**
- **Data Modeling**
- **DAX Measures & Calculations**
- KPI Development
- Interactive Filtering (Region slicer)
- Data Visualization Best Practices
- Business Insight Extraction

---

## 🧮 Sample DAX Calculations

```DAX
Total Sales = SUM(Sales[SalesAmount])

Total Profit = SUM(Sales[Profit])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Sales Variance = [Total Sales] - [Sales Target]
