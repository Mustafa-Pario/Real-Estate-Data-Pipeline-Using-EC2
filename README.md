# Real Estate Data Pipeline with AWS, Airflow, Snowflake & Power BI

![redfin-diagram](https://github.com/user-attachments/assets/234cb3d2-f9ff-4930-864b-d363682586c4)

This repository contains an end-to-end, cloud-based automated ETL data pipeline designed to ingest, process, and analyze real estate data from Redfin. The pipeline leverages AWS services, Apache Airflow for orchestration, Snowflake for data warehousing, and Power BI for analytics and visualization.

The solution is built to be scalable, modular, and production-oriented, enabling reliable data ingestion and near real-time analytics on real estate market trends.

## Project Overview

The data pipeline consists of the following stages:

1. **Data Extraction**: 
   - Real estate data is programmatically extracted from Redfin using Python.
   - Raw source data is stored in an Amazon S3 bucket for durability and auditability.

2. **Transformation**:
   - Python-based transformation scripts clean, normalize, and structure the raw data.
   - Transformed datasets are written to a separate S3 bucket, following a multi-layer (raw → processed) data architecture.

3. **Automated Data Loading (Snowpipe)**:
   - Snowpipe is configured to automatically ingest transformed data from S3 into Snowflake.
   - This enables continuous, event-driven data loading with minimal latency.

4. **Data Warehousing**:
   - Snowflake serves as the central analytical data warehouse.
   - Data is optimized for querying, reporting, and downstream BI consumption.
     
5. **Orchestration & Scheduling**:
   - Apache Airflow, deployed on an AWS EC2 instance, orchestrates the entire ETL workflow.
   - DAGs handle task scheduling, dependencies, retries, and monitoring to ensure pipeline reliability.

6. **Data Visualization**:
   - Snowflake is connected to Power BI to build interactive dashboards.
   - Visualizations provide insights into key real estate metrics and trends.

## Architecture

The architecture includes the following components:
- **Amazon S3**: Stores raw and transformed data.
- **Python**: Handles data extraction and transformation.
- **Snowflake**: Stores the final processed data for analytics.
- **Apache Airflow**: Orchestrates the ETL pipeline.
- **Power BI**: Provides visualization for data insights.

## Technologies Used

- **Python**: For extraction and transformation scripts.
- **AWS S3**: For cloud storage of raw and transformed data.
- **Apache Airflow**: For orchestrating and automating the data pipeline.
- **Snowflake**: For cloud-based data warehousing.
- **Power BI**: For data visualization.
- **AWS EC2**: For running the Airflow instance.

## Key Features

- **Automated Data Ingestion**: Redfin data is automatically ingested and stored in S3 buckets.
- **ETL Orchestration**: Airflow schedules and monitors the ETL pipeline.
- **Real-Time Loading**: Data is continuously ingested into Snowflake using Snowpipe.
- **Visualization**: Power BI connects to Snowflake for advanced analytics and dashboards.
  
  ## Visualizations through Power BI
  ### Sum of Homes Sold
   ![sum-of-homes-sold](https://github.com/user-attachments/assets/c3e0efc4-690f-4aad-aa1d-0db25e7870f9)


  ### Sum of Inventory
   ![sum-of-inventory](https://github.com/user-attachments/assets/2bed1deb-48a0-4592-b724-753790d3041d)

