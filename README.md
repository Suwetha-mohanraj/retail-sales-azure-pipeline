# Retail Sales Analytics Pipeline — Azure Cloud

Azure | ADF | SQL| PowerBI | DP-900

## Project Overview

This project demonstrates an end-to-end retail sales analytics pipeline built on Microsoft Azure. 
The pipeline automates data ingestion, transformation, storage, and visualization for business reporting and decision-making.

## Problem statement
A retail chain's daily sales data was scattered across monthly CSV files
with no central analytics view. Finance had no visibility into revenue
trends, top-selling products, or regional performance. Reports were
built manually every week in Excel.

## Solution
Built a fully automated end-to-end data pipeline on Microsoft Azure that
ingests raw CSV files daily, loads them into a structured SQL database,
and visualises business insights in a live Power BI dashboard — with
zero manual intervention.

## Architecture
CSV files (3 months of sales data)
    ↓
Azure Blob Storage (raw-sales-data container)
    ↓
Azure Data Factory (ForEach pipeline — runs daily at 7 AM IST)
    ↓
Azure SQL Database (star schema — fact_sales, dim_products, dim_regions)
    ↓
Power BI Dashboard (KPI cards, charts, DAX measures, slicers)  

## Tech stack
- Azure Blob Storage — raw file landing zone for CSV ingestion
- Azure Data Factory — ETL orchestration with Get Metadata + ForEach
- Azure SQL Database — star schema with computed columns and views
- T-SQL — table design, views, stored procedures
- Power BI Desktop — dashboard with KPI cards, charts, DAX measures
- Microsoft Azure Portal — resource management and firewall config
  
## Dashboard Screenshot
![Dashboard screenshot](screenshots/Retail%20Dashboard.png)

### Product Analysis

![Product Analysis](screenshots/Retail%20Dashboard%20product%20analysis%20.png)


## Key findings
- Electronics = 85% of total revenue 
- South region leads at 36% market share
- 22 transactions across Jan–Mar 2024
- Avg transaction value: ₹34,580

  ## Features

- Automated CSV ingestion
- ETL pipeline using Azure Data Factory
- Data storage in Azure SQL Database
- Interactive Power BI dashboard
- Retail sales performance analysis
- Scalable cloud-based architecture

## What I built
- ADF pipeline with Get Metadata + ForEach loop
- Schedule trigger running daily at 7 AM IST
- Star schema: fact_sales + dim_products + dim_regions
- Computed column for total_amount (SQL calculated field)
- Summary view vw_daily_sales_summary for Power BI
- 4 KPI cards + charts + slicers + DAX measures
  
## Future Enhancements

- Real-time streaming analytics
- Azure Synapse integration
- Machine learning-based sales prediction
- Automated alerts and monitoring

## Certification
Microsoft Certified: Azure Data Fundamentals (DP-900)
