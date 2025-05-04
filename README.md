
# YouTube Ad Analytics ETL Dashboard

This project is an end-to-end data pipeline and analytics dashboard that helps companies analyze YouTube ad performance and optimize their ad placement strategy.

## Project Overview

- **Goal:** Provide actionable insights on YouTube ad trends using automated data collection, ETL, and visualization.
- **Outcome:** Supports ad strategy decisions with interactive visuals and centralized metrics.

## Project Objectives

1. **Data Management**: Extract raw data from csv file and YouTube API and store it in AWS S3.
2. **ETL Automation**: Streamline data transformation using AWS Glue and Lambda.
3. **Dashboard Development**: Design an interactive dashboard with AWS QuickSight to visualize trends and inform ad placement strategies for end users.

## System Design & Technologies Used

- **Data Ingestion**
    - ***YouTube API*** - For fetching YouTube data
    - ***AWS S3*** – Raw and processed data storage 
- **Data Transformation** 
    - ***AWS Lambda*** – Data transformation from JSON to Parquet  
- **ETL Automation**
    - ***AWS Glue*** – Automates data catalog creation and ETL processing (data joining)  
- **Data Analysis**
    - ***AWS Athena*** – Querying processed data
- **Visualization** 
    - ***Amazon QuickSight*** – Interactive dashboard for end users  
- **General**
    - ***AWS CLI*** - Command-line interface for managing AWS resources
    - ***Python 3.8*** - For Lambda functions, ETL scripts, API integration

### Architecture Diagram
![High-level Architecture Diagram](https://github.com/nartov-k/etl-youtube/tree/main/architecture/high-level_architecture.png)
![High-level Architecture Diagram](https://raw.githubusercontent.com/nartov-k/etl-youtube/main/architecture/high-level_architecture.png)
![Low-level Architecture Diagram](https://github.com/nartov-k/etl-youtube/tree/main/architecture/low-level_architecture.jpg)
![Low-level Architecture Diagram](https://raw.githubusercontent.com/nartov-k/etl-youtube/main/architecture/low-level_architecture.jpg)

## Implementation Steps

1. **Data Collection**:
   - Fetch data from the YouTube API (JSON/CSV formats).
   - Store raw data in an S3 bucket.
   
2. **Data Transformation**:
   - Convert JSON/CSV files to Parquet format using Lambda functions.
   - Update data types for compatibility and optimize data storage.

3. **ETL Pipeline**:
   - Create a data catalog in AWS Glue.
   - Join datasets and partition data for efficient querying.

4. **Querying**:
   - Use AWS Athena to run SQL queries on the transformed data.
   
5. **Visualization**:
   - Connect Athena to QuickSight for dashboard development.
   - Visualize trends, engagement metrics, and ad placement insights.

## Features

- Automated extraction and transformation of YouTube ad performance data
- Serverless ETL pipeline on AWS for scalability
- Interactive dashboard with key KPIs like Top viewed categories (e.g., "Entertainment," "Music"), Engagement rates, Best-performing ad placement categories and Cost metrics
- Designed for marketing teams to identify high-ROI ad opportunities

## Impact

- Improves decision-making for ad spend and targeting  
- Serves as a real-world demonstration of cloud-based analytics at scale

### Dashboard
![Dashboard 1](https://github.com/nartov-k/etl-youtube/tree/main/dashboard/frontend1.png)
![Dashboard 1](https://raw.githubusercontent.com/nartov-k/etl-youtube/main/dashboard/frontend1.png)
![Dashboard 2](https://github.com/nartov-k/etl-youtube/tree/main/dashboard/frontend2.png)
![Dashboard 2](https://raw.githubusercontent.com/nartov-k/etl-youtube/main/dashboard/frontend2.png)

## Challenges

- API Rate: limited ability to update large datasets efficiently.
- Lambda Configuration:
    - Created manual Lambda layers for Python 3.8 compatibility.
    - Resolved issues related to data type mismatches.
- Query Optimization: Managed data partitioning for efficient querying.
- Dataset Updates**: Limited updates to top 500 rows due to time and cost constraints.

---

## Links and References

- [AWS Doc](https://aws.amazon.com/documentation/)
- [YT API Doc](https://developers.google.com/youtube/v3/getting-started)
- [Dashboard (Requires Account)](https://us-east-1.quicksight.aws.amazon.com/sn/dashboards/4e5f0d59-4fa3-430e-9c9b-9e1da61a0ea1)


