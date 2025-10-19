# NYC Taxi Analytics Pipeline
As I'm learning how modern data pipelines work, I wanted to practice with a real-world dataset. I chose the NYC taxi trip data because it's the perfect training ground for a data engineer.

**Why This Dataset?**
- Scale and Complexity: With over 100M+ records, I learned to handle realistic data volumes and performance tuning in the cloud.
- Messy and Realistic: The data has duplicates, missing values, and type mismatches—exactly what you encounter in production environments.
- Business Relevance: The project provides insights for policymakers and businesses, answering questions like "Which neighborhoods generate the most revenue?" or "What's the average trip distance?"
- Free and Well-Documented: As a public dataset from NYC TLC, it's accessible and regularly updated, which is perfect for practicing end-to-end data engineering skills.

## Project Overview

This project demonstrates a fully orchestrated, cloud-based analytics engineering pipeline that processes millions of NYC taxi trip records:

* Ingests millions of NYC taxi trip records from public datasets (covering 2024 and 2025 data)
* Stores raw data efficiently in Google Cloud Storage
* Transfers raw data from GCS into BigQuery staging tables
* Transforms data using dbt Cloud (data build tool) with dimensional modeling, runs dbt data quality tests (e.g., uniqueness, non-null values) before publishing final models
* Loads clean, modeled data into BigQuery for analysis

## Technology Stack

| Category | Tool | Purpose |
| :--- | :--- | :--- |
| **Infrastructure (IaaC)** | **Terraform** | Provisioning and managing GCP resources (GCS buckets, BigQuery datasets). |
| **Data Ingestion** | **Python (requests), Docker** | Consistent environment for downloading data from the NYC TLC API and uploading to cloud storage. |
| **Cloud Storage** | **Google Cloud Storage (GCS)** | Efficient and reliable storage for raw, historical data. |
| **Data Warehouse** | **BigQuery** | Scalable, serverless warehouse for analytics and fast querying of modeled data. |
| **Transformation & Testing** | **dbt Cloud** | Applying dimensional modeling (Star Schema) and automated data quality testing before loading. |
