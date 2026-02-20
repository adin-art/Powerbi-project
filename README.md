# 📊 Program Performance Analytics Dashboard

## Overview

This repository contains a Power BI dashboard developed to analyze and monitor program performance across regions and time periods. The solution applies dimensional modeling, DAX calculations, and structured data transformation to generate interactive performance insights.

---

## Objectives

- Monitor achievement against targets
- Analyze budget variance and expenditure trends
- Compare regional performance
- Track performance over time
- Support data-driven decision-making

---

## Tools & Technologies

- Microsoft Power BI Desktop
- Power Query (ETL)
- DAX (Data Analysis Expressions)
- Star Schema Data Modeling

---

## Data Model

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

Relationships are structured as one-to-many from dimensions to the fact table using a star schema model.

---

## Data Transformation

Data preparation steps performed in Power Query:

- Data type standardization
- Null handling
- Duplicate removal
- Column renaming and normalization
- Derived column creation
- Unpivoting where necessary

---

## Key DAX Measures

```DAX
Achievement Rate =
DIVIDE(
    SUM(Fact_Performance[Actual]),
    SUM(Fact_Performance[Target])
)

Budget Variance % =
DIVIDE(
    SUM(Fact_Performance[Expenditure]) - SUM(Fact_Performance[Budget]),
    SUM(Fact_Performance[Budget])
)

Cost per Beneficiary =
DIVIDE(
    SUM(Fact_Performance[Expenditure]),
    SUM(Fact_Performance[Beneficiaries])
)


Cumulative Actual =
CALCULATE(
    SUM(Fact_Performance[Actual]),
    FILTER(
        ALL(Dim_Date),
        Dim_Date[Date] <= MAX(Dim_Date[Date])
    )
)
