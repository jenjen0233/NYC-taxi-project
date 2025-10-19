# NYC Taxi Analytics Pipeline
As I am learning how modern data pipelines work, I wanted to practice with a real-world dataset. I chose NYC taxi trip data, and here's why it's perfect for learning:
- Scale and complexity: With 100M+ records, you learn to handle real data volumes.
- Messy and realistic: The data has duplicates, missing values, and type mismatches — exactly what you'll encounter in production environments.
- Interesting business questions: I can answer questions like "Which neighborhoods generate the most revenue?" or "What's the average trip distance?" These insights matter to policymakers and businesses making decisions.
- Free and well-documented: As a public dataset from NYC TLC, it's accessible to anyone and regularly updated — perfect for practicing data engineering skills like ingestion, transformation, and orchestration.
Most importantly, if you can build a pipeline for taxi data, you can apply the same patterns to e-commerce, logistics, or any time-series business data.

## Project Overview

This project demonstrates an analytics engineering pipeline that:
* Ingests millions of NYC taxi trip records from public datasets (2024 and 2025)
* Stores raw data efficiently in Google Cloud Storage
* Transforms data using dbt (data build tool) with dimensional modeling
* Loads clean, modeled data into BigQuery for analysis
* Provides automated data quality testing and validation
