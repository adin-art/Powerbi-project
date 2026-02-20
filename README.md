# 📊 Program Performance Analytics Dashboard

## 📌 Project Overview

This repository contains a Power BI dashboard developed to monitor and evaluate program performance across regions and time periods.  

The solution applies dimensional modeling principles, DAX-based KPI calculations, and structured ETL processes to generate interactive and decision-support analytics.

---

## 🎯 Objectives

- Track achievement against planned targets  
- Monitor budget utilization and variance  
- Compare regional performance  
- Analyze time-based trends  
- Support evidence-based reporting  

---

## 🛠 Tools & Technologies

- Microsoft Power BI Desktop  
- Power Query (ETL)  
- DAX (Data Analysis Expressions)  
- Star Schema Data Modeling  

---

## 🏗 Data Model

### Fact Table
**Fact_Performance**
- Target  
- Actual  
- Budget  
- Expenditure  
- Beneficiaries  
- Region_ID  
- Activity_ID  
- Date_ID  

### Dimension Tables
- Dim_Region  
- Dim_Date  
- Dim_Activity  

Model structure follows a **Star Schema** with one-to-many relationships from dimensions to the fact table.

---

## 🔄 Data Transformation (Power Query)

Data preparation included:

- Data type standardization  
- Null value handling  
- Duplicate removal  
- Column normalization  
- Unpivoting structured performance metrics  
- Creation of derived columns  

---

## 📐 Key DAX Measures

```DAX
Achievement Rate =
DIVIDE(
    SUM(Fact_Performance[Actual]),
    SUM(Fact_Performance[Target])
)


