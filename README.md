# ETL project based on Kaggle Tokyo Olympic dataset

This repository contains the code and pipeline definitions for an ETL (Extract, Transform, Load) process designed to handle datasets related to the Tokyo Olympics. It demonstrates an end-to-end data engineering project using various Azure services.

## Overview

The project follows a systematic approach to ingest raw data from multiple sources, store it, transform it into a structured format, and finally load it for analytics and visualization purposes.



## Services Used

- Azure Data Lake Storage Gen2
- Azure Data Factory
- Azure Databricks
- Azure Synapse Analytics

## Steps

### 1. Setting up the Data Lake

- **Create a Storage Account**: Setup includes the creation of a container that hosts both raw and transformed data.
- **Raw Data**: `raw-data` folder in Azure Data Lake for initial data dump.
- **Transformed Data**: `transformed-data` folder for the processed data ready for analytics.

### 2. Building the Data Pipeline with Azure Data Factory

- **Create Data Factory**: Integrate with GitHub repository for project version control.
- **Pipeline Construction**: Develop data pipelines for entities such as medals, teams, coaches, and more. The pipelines extract data from the sources and load it into Data Lake Gen2.
- **Data Sources**: Configured HTTP sources for data ingestion. 

### 3. Data Processing with Azure Databricks

- **Create Azure Databricks Workspace**: Initialize a new compute and cluster.
- **App Registration**: Generate credentials required for Azure Databricks configuration.
- **Databricks Notebook**: Use provided client ID, tenant ID, and a secret key obtained from the app registration to establish a connection with Data Factory.

### 4. Analytics with Azure Synapse

- **Create Azure Synapse Analytics Workspace**: Define SQL pools and manage queries.
- **Database and Tables**: Setup and manage databases and tables within Azure Synapse.
- **SQL Queries**: Perform SQL queries to extract insights from the processed data.



