# 🍴 Food Inspection Data Warehousing  
### Dimensional Model - Star Schema  

---

## Overview  
This repository focuses on building a **Data Warehouse** for food inspection data sourced from **Dallas** and **Chicago**. Using a **Star Schema Dimensional Model**, the project enables efficient querying and analysis of food inspection details to derive actionable insights. The model supports use cases like risk analysis, violation trends, and inspection performance.

---

## Objectives  
- Organize and integrate food inspection data into a centralized **Data Warehouse**.  
- Enable insightful analysis by employing a **Star Schema Dimensional Model**.  
- Provide a platform for answering key business questions related to inspection scores, violations, and risk management.  

---

## Data Sources  
The data for this project comes from the following sources:  
1. **Food_Inspection_Dallas**: Details of food inspections conducted in Dallas.  
2. **Food_Inspection_Chicago**: Food inspection records from Chicago.  

These datasets include fields such as inspection types, inspection scores, violation details, business information, and risk categorization.  

---

## Dimensional Model  

The model follows a **Star Schema** design and includes the following components:  

### Fact Tables  
1. **Fact_Food_Inspection**:  
   - Central fact table capturing key metrics like inspection score, risk type, and inspection details.  
   - Linked to multiple dimensions (Business, Date, Inspection Type, Risk, Result).  

2. **Fact_FI_Violation**:  
   - Fact table for violations observed during inspections.  
   - Includes details such as violation codes, descriptions, points, and comments.  

### Dimension Tables  
1. **Dim_Business**:  
   - Captures details about food businesses such as license number, address, and facility type.  

2. **Dim_Inspection_Type**:  
   - Contains types of inspections (e.g., routine, follow-up).  

3. **Dim_Result**:  
   - Stores inspection outcomes (e.g., pass, fail).  

4. **Dim_Risk**:  
   - Classifies inspections into risk levels (e.g., high risk, low risk).  

5. **Dim_Date**:  
   - Standard date dimension to support temporal analysis.  

6. **Dim_Violations**:  
   - Contains violation codes, descriptions, and assigned points for severity.  

---

## Key Features  

- **Risk Analysis**: Identify businesses with high-risk inspections.  
- **Violation Trends**: Analyze common violations and their impact on inspection outcomes.  
- **Temporal Analysis**: Observe patterns over time (e.g., seasonal trends in violations).  
- **City Comparison**: Compare inspection trends and results between Dallas and Chicago.  

---

## Insights and Use Cases  

1. **Inspection Performance**:  
   - Average scores of food establishments over time.  

2. **Violation Frequency**:  
   - Most common violations by category and city.  

3. **Risk Management**:  
   - Distribution of inspections across risk levels.  

4. **Business Analysis**:  
   - Locations with the most violations or lowest scores.  

5. **Temporal Insights**:  
   - Weekly, monthly, and seasonal patterns in inspections and violations.  

---

## Tools and Technologies  

- **ETL**: Talend for data extraction, transformation, and loading.  
- **Database**: Star Schema implemented in **SQL Server/PostgreSQL**.  
- **Visualization**: Tableau or Power BI for dashboards and insights.  
- **Data Profiling**: Alteryx for profiling raw data from source systems.  

---

## Dimensional Model Diagram  

The following diagram represents the **Star Schema Dimensional Model** used for this project:

![Dimensional Model](./image.png)

---

## Deliverables  

1. **ETL Pipelines**: Scripts and workflows for loading data into the warehouse.  
2. **Dimensional Model**: SQL scripts to create and populate fact and dimension tables.  
3. **Dashboards**: Interactive visualizations for food inspection trends and insights.  
4. **Reports**: Business insights based on risk analysis, violations, and scores.  

---
