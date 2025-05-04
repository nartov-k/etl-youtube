
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
![Architecture Diagram](https://github.com/nartov-k/etl-youtube/tree/main/architechture/low-level_architecture.png)
 

## Features

- Automated extraction and transformation of YouTube ad performance data
- Serverless ETL pipeline on AWS for scalability
- Interactive dashboard with key KPIs like impressions, engagement, and cost metrics
- Designed for marketing teams to identify high-ROI ad opportunities

## Impact

- Replaces manual spreadsheet tracking with automated data flows  
- Improves decision-making for ad spend and targeting  
- Serves as a real-world demonstration of cloud-based analytics at scale


