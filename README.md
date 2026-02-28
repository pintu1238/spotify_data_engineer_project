# Spotify Real-Time Data Engineering Pipeline | Azure Lakehouse Project

## Overview

This project demonstrates a production-grade end-to-end Azure data engineering pipeline built using modern Lakehouse architecture.

The solution covers batch and streaming ingestion, incremental processing, metadata-driven transformations, dimensional modeling, and CI/CD deployment practices.

The architecture follows the Medallion pattern (Bronze → Silver → Gold) to ensure scalable, reliable, and maintainable data processing.

---

## Architecture

Azure SQL Database (Source)  
→ Azure Data Factory (Ingestion & Orchestration)  
→ ADLS Gen2 (Bronze Layer - Raw Data)  
→ Azure Databricks (Silver & Gold Transformations)  
→ Delta Lake (Curated Tables)  

---

## Tech Stack

### Azure Services
- Azure Data Factory
- Azure SQL Database
- Azure Data Lake Storage Gen2
- Azure Databricks
- Unity Catalog

### Data Processing
- PySpark
- Spark Structured Streaming
- Databricks Autoloader
- Delta Lake (MERGE, Delta Live Tables)

### DevOps
- Git & GitHub
- Databricks Asset Bundles
- CI/CD Deployment

---

## Key Features

### Incremental Ingestion
- Implemented watermark-based incremental pipelines in Azure Data Factory
- Enabled backfilling capability for historical data loads
- Designed dynamic looping pipelines for scalable ingestion

### Real-Time Processing
- Built streaming pipelines using Spark Structured Streaming
- Used Databricks Autoloader for scalable file ingestion
- Supported incremental updates in Delta tables

### Metadata-Driven Architecture
- Developed dynamic transformation pipelines using PySpark and Jinja2
- Designed reusable, configurable pipeline logic
- Reduced hardcoding and improved maintainability

### Data Modeling
- Implemented Star Schema dimensional modeling
- Designed dimension tables with SCD Type 1 and Type 2 logic
- Built centralized fact tables for analytics
- Generated surrogate keys for referential integrity

### Delta Lake Implementation
- Used Delta Lake MERGE for upsert operations
- Ensured ACID-compliant transactions
- Managed schema evolution and incremental loads
- Implemented Delta Live Tables for declarative pipelines

### DevOps & Governance
- Integrated Unity Catalog for centralized governance
- Implemented Git-based version control
- Deployed pipelines using Databricks Asset Bundles
- Enabled CI/CD workflow for production-ready deployments

---

## Medallion Architecture

### Bronze Layer
- Raw data ingestion from Azure SQL
- Stored in ADLS Gen2 without transformations

### Silver Layer
- Cleaned and enriched data
- Applied deduplication and transformation logic
- Standardized schema

### Gold Layer
- Dimensional modeling (Star Schema)
- Aggregated and analytics-ready datasets
- Optimized for reporting and BI consumption

---

## Outcomes

- Built scalable batch and streaming data pipelines
- Implemented metadata-driven, reusable transformation framework
- Applied industry-standard dimensional modeling practices
- Delivered production-ready Lakehouse architecture on Azure
