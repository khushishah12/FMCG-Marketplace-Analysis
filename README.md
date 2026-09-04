🛒 FMCG Marketplace Analysis: End-to-End Data Engineering Pipeline


📌 Project Overview
Welcome to the FMCG Marketplace Analysis project! This repository contains a robust, end-to-end Data Engineering solution designed to process, transform, and analyze marketplace data for a Fast-Moving Consumer Goods (FMCG) company.

The core objective of this project is to build a scalable data pipeline that integrates parent and child company data, processes both full and incremental loads, and prepares the data for insightful dashboarding and business intelligence.

🚀 Key Objectives
Data Integration: Combine and harmonize datasets from various sources (Parent Company and Child Company).

Robust ETL Pipeline: Design and implement a reliable Extract, Transform, Load (ETL) process to handle both historical (full load) and daily (incremental) data.

Data Modeling: Structure the data into optimized dimension and fact tables for efficient querying.

Business Intelligence: Prepare denormalized views specifically tailored to power interactive dashboards.

🛠️ Tech Stack & Tools
Platform: Databricks

Processing Engine: Apache Spark

Languages: Python (PySpark), SQL

Concepts: Medallion Architecture (Bronze, Silver, Gold), Incremental Loading, Fact & Dimension Modeling

📂 Project Structure
Here is a breakdown of how the project is organized:

0_data/: The raw data repository.

1_parent_company/: Contains full and incremental data extracts (Customers, Gross Price, Products, Orders).

2_child_company/: Contains full load data and daily landing files for orders.

1_codes/: The core ETL logic (Jupyter/Databricks Notebooks).

1_setup/: Configuration notebooks (Catalog setup, Utilities, Date Dimension creation).

2_dimension_data_processing/: Logic for cleaning and structuring Customer, Product, and Pricing dimension tables.

3_fact_data_processing/: Complex logic for processing Full Load and Incremental Load Fact data.

2_dashboarding/: The final presentation layer.

SQL queries for denormalizing data.

The final fmcg_dashboard.pdf showcasing business insights.

resources/: Architecture diagrams and visual assets.

⚙️ Architecture & Workflow

This project follows a structured approach to data engineering:

Ingestion: Raw CSV files are read from the landing zones.

Transformation (Silver Layer): Data is cleaned, standardized, and joined using PySpark. Dimension tables (Customers, Products, Pricing) are populated.

Loading (Gold Layer): Fact tables are created. The pipeline handles daily incremental updates seamlessly, ensuring the data warehouse is always current.

Serving: Data is denormalized using SQL for optimal dashboard performance.

📊 Dashboard & Insights
The final output is a comprehensive dashboard that provides actionable insights into the FMCG marketplace performance. It tracks key metrics such as:

Sales trends over time

Product category performance

Customer behavior and regional distribution

💡 How to Run the Project

Set up a Databricks workspace.

Upload the files from the 0_data folder to your Databricks File System (DBFS) or cloud storage.

Run the notebooks in the 1_codes/1_setup folder first.

Execute the Dimension processing notebooks, followed by the Fact processing notebooks.

🤝 Let's Connect!
If you have any questions, suggestions, or just want to chat about Data Engineering, feel free to reach out!
