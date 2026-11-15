# Azure Synapse Analytics – Hands-on Project

## Project Overview

This project demonstrates hands-on learning and implementation of Azure Synapse Analytics, integrating Azure Data Lake Storage Gen2 with Dedicated SQL Pool and Serverless SQL Pool.

The objective is to understand SQL-based data querying, external data access, data loading, and data transformation using Azure Synapse Analytics.

## Technologies Used

- Azure Synapse Analytics
- Azure Data Lake Storage Gen2 (ADLS Gen2)
- Dedicated SQL Pool
- Serverless SQL Pool
- PolyBase
- External Tables
- CETAS (CREATE EXTERNAL TABLE AS SELECT)
- COPY INTO
- Managed Identity
- Parquet

## Project Architecture

```text
          Azure Data Lake Storage Gen2
                     |
              Raw Data (CSV)
                     |
          Azure Synapse Analytics
                     |
          +----------+----------+
          |                     |
     Serverless SQL        Dedicated SQL
          Pool                 Pool
          |                     |
    External Tables       PolyBase
          |                     |
         CETAS             COPY INTO
          |                     |
     Parquet Files        Internal Tables
          |                     |
          +----------+----------+
                     |
                Data Analysis
```

## Implementation Details

### 1. Serverless SQL Pool
- Created database scoped credentials.
- Configured external data sources.
- Created external file formats.
- Created external tables to query ADLS Gen2 files.
- Used CETAS to export query results into Parquet files.

### 2. Dedicated SQL Pool
- Created internal tables.
- Practised ROUND_ROBIN distribution.
- Created external data sources using ABFSS.
- Configured PolyBase external tables.
- Practised loading data using COPY INTO.

### 3. ADLS Gen2 Integration
- Connected Azure Synapse with ADLS Gen2.
- Accessed raw CSV and Parquet files.
- Practised Managed Identity authentication.

## Key Learning Outcomes

- Understanding Dedicated SQL Pool vs Serverless SQL Pool.
- Understanding MPP architecture and table distributions.
- Working with external data sources and file formats.
- Querying data directly from ADLS Gen2.
- Understanding PolyBase and external tables.
- Loading data into Dedicated SQL Pool.
- Working with CSV and Parquet file formats.

## Repository Structure

```text
Azure-Synapse-Analytics/
|
|-- README.md
|-- Dedicated-SQL-Pool/
|-- Serverless-SQL-Pool/
|-- Validation/
```

## Note

This repository is part of my hands-on Azure Data Engineering learning journey. SQL scripts and implementation details are added as practical exercises are completed.
