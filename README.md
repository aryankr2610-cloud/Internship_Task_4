# Executive Sales Performance Dashboard (Power BI)

# Project Overview
This project focuses on professional Business Intelligence (BI) development, moving beyond simple visualization to robust data modeling and advanced analytical calculations. The objective was to transform raw sales data into a dynamic, executive-ready dashboard that provides strategic business insights

# Key Features
 . Star Schema Modeling: Implementation of a structured data model involving Fact and Dimension tables for optimized performance.  Advanced DAX Calculations: Creation of core business metrics and complex measures using Data Analysis Expressions.  
 . Time Intelligence: Analysis of month-over-month growth and historical performance trends.  
 . Interactive Storytelling: A dynamic dashboard designed for executive-level decision-making with multi-layered filtering. 

# Data Architecture
The project follows a Star Schema design:  Fact Table: Orders (Contains transactional data like Sales, Profit, and Quantity).  Dimension Tables: * Customers: Contains Customer IDs, Names, Segments, and Regions.  
Products: Contains Product IDs, Categories, and Sub-Categories.  
Calendar: A custom DAX-generated table for advanced time-based filtering.  

# DAX Measures Implemented
The following core measures were developed to drive the analytical engine of the dashboard:

Measure,                                  Logic / DAX Function

Total Sales,                              SUM(Orders[Sales]) 
Total Profit,                             SUM(Orders[Profit]) 
Profit Margin,                            "DIVIDE([Total Profit], [Total Sales]) "
Previous Month Sales,                     "CALCULATE([Total Sales], PREVIOUSMONTH(Calendar[Date])) "
Growth %,                                 "DIVIDE([Total Sales] - [Previous Month Sales], [Previous Month Sales]) "
Category Contribution %,                  "DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Products[Category]))) "

# Dashboard Layout
The dashboard is organized into three strategic sections: 

Top Section (KPIs): High-level summary of Total Sales, Profit, Margin, and Growth %.  
Middle Section (Trends): Monthly Sales trends (Line Chart) and Regional performance (Column Chart).  
Bottom Section (Deep Dive): Segment distribution and a breakdown of the Top 10 Customers.  

# Business Insights Derived
Regional Dominance: Identified the primary regions driving the majority of revenue.  
Product Profitability: Discovered which categories yield the highest margins versus those with the highest sales volume.  Seasonality: Identified consistent sales peaks and seasonal trends across the fiscal year.  

# Technologies Used
Power BI Desktop: For data modeling and visualization.  
Power Query: For ETL (Extract, Transform, Load) and data cleaning.
DAX: For complex statistical and time-intelligence measures.  

