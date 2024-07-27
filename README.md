# YouTube Data Analytics Project

## Overview

This project aims to securely manage, streamline, and perform analysis on the structured and semi-structured YouTube video data based on the video categories and trending metrics.

## Project Goals

1. **Data Ingestion**: Build a mechanism to ingest data from different sources.
2. **ETL System**: Transform raw data into a proper format.
3. **Data Lake**: Use a centralized repository to store data from multiple sources.
4. **Scalability**: Ensure the system scales as data size increases.
5. **Cloud**: Use AWS to process vast amounts of data.
6. **Reporting**: Build a dashboard to answer key questions.

## AWS Services Used

- **Amazon S3**: Object storage service for scalability, data availability, security, and performance.
- **AWS IAM**: Identity and Access Management to securely manage access to AWS services and resources.
- **Amazon QuickSight**: Scalable, serverless BI service for building interactive dashboards.
- **AWS Glue**: Serverless data integration service for discovering, preparing, and combining data.
- **AWS Lambda**: Computing service to run code without managing servers.
- **AWS Athena**: Interactive query service for data stored in S3.

## Dataset

We are using a Kaggle dataset containing statistics (CSV files) on daily popular YouTube videos over many months. The dataset includes up to 200 trending videos published daily for many locations. Each region's data is in its own file and includes:
- Video title
- Channel title
- Publication time
- Tags
- Views
- Likes and dislikes
- Description
- Comment count
- Category ID (included in a JSON file linked to the region)

- ## Steps to Run the Project

1. **Data Ingestion**: 
   - Use `data_ingestion.py` to ingest data from Kaggle and upload it to Amazon S3.

2. **ETL Process**:
   - Use AWS Glue jobs (`glue_jobs.py`) to transform raw data into a structured format.

3. **Data Storage**:
   - Store transformed data in Amazon S3.

4. **Data Processing and Querying**:
   - Use AWS Athena to run SQL queries on the data stored in S3 (`queries.athena.sql`).

5. **Dashboard Creation**:
   - Use Amazon QuickSight to create interactive dashboards for reporting and visualization.

6. **Lambda Functions**:
   - Use `lambda_functions.py` for automating data workflows and integrating various AWS services.
