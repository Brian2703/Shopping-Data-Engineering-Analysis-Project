# Customer Shopping Analysis (Databrick & AWS)

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
- Store data in DeltaLake.
  
Silver (Processed Data)
- Handle missing values.
- Standardize formats and perform transformations.
- Validate and prepare data for analytics.

Gold (Analytical Data)
- Aggregate and compute revenue insights.
- Generate key customer behavior metrics.
- Provide structured data for dashboards.

  
## Dashboard & Visualization:
SQL queries are used to create visualizations and business intelligence reports in Databricks Analytics.


## Technology Stack:
- Cloud Storage: AWS S3
- Data Processing: Databricks (Apache Spark, Delta Lake)
- Analytics & Dashboarding: Databricks SQL
- This project follows a structured ETL approach to process and refine raw shopping data into meaningful insights, optimizing data quality, monitoring, and pipeline reusability.

## Project Workflow
1. <b>Create S3 bucket and upload dataset</b>
- Log in to AWS and create a new S3 bucket to store raw shopping data.
- Upload the dataset files into the S3 bucket under a designated folder for structured storage.

2. <b> Create an IAM User in AWS</b>
- Set up an IAM user to manage access control for Databricks.
- Assign the AmazonS3FullAccess permission to ensure seamless data access.
- Obtain the Access Key ID and Secret Access Key.

3. <b>Create Databricks Workspace and Link it with S3</b>
- Set up a Databricks workspace on AWS for data processing and analytics.
- Configure Databricks to connect directly to the S3 bucket using IAM authentication.

4. <b>Create Bronze Notebook, Silver Notebook and Gold Notebook</b>

5. <b>SQL queries for plotting charts</b>
- All queries is store in folder

5. <b>Dashboard building</b>


