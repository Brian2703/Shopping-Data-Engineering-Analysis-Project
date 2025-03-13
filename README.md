# Customer Shopping Analysis (Databrick & AWS

## Overview

This project focuses on analyzing customer shopping habits based on dummy dataset. Using a structured medallion architecture (Bronze, Silver, Gold) within Databricks. 

The goal is to extract insights into customer demographics, purchased items, and revenue while ensuring high data quality through a robust data pipeline.

## Data Pipeline Architecture:

Bronze Layer: Raw data ingestion from AWS S3 into Databricks for storage in Delta Lake in its original form.

Silver Layer: Data cleaning, transformation, and structuring for analysis.

Gold Layer: Aggregations, calculations, and business intelligence insights.

1. Key Processes in Each Layer:

Bronze (Raw Data):
- Load raw shopping data from AWS S3.
- Store data in its original form for traceability.
  
Silver (Processed Data)
- Handle missing values and fix inconsistencies.
- Standardize formats and perform transformations.
- Validate and prepare data for analytics.

Gold (Analytical Data)
- Aggregate and compute revenue insights.
- Generate key customer behavior metrics.
- Provide structured data for dashboards.

  
## Dashboard & Visualization:
SQL queries are used to create visualizations and business intelligence reports in Databricks Analytics.


## Technology Stack:
Cloud Storage: AWS S3
Data Processing: Databricks (Apache Spark, Delta Lake)
Analytics & Dashboarding: Databricks SQL
This project follows a structured ETL approach to process and refine raw shopping data into meaningful insights, optimizing data quality, monitoring, and pipeline reusability.

## Project Workflow
1. <b>Create S3 bucket and upload dataset</b>

2. <b>Create an IAM User in AWS</b>

Set permissions to this user:

- AmazonS3FullAccess

2. <b>Create Databrick worspace and link it with S2</b>

3. <b>Create Bronze Notebook</b>


1. <b>Data is loaded into songplays fact table</b>

<img src="images/songplays_table.png" width="70%">

2. <b>The DAG is success for all tasks</b>

<img src="images/sparkify_DAG_success.png" width="70%">
