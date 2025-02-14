![image](https://github.com/user-attachments/assets/de19a803-b0c2-4bba-9436-b04b0466317f)

# TaxiTripProject
Dataset link - https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
Azure Data Engineering Pipeline with Medallion Architecture and Delta Lake

In this project, I developed an end-to-end data engineering pipeline on Azure Databricks to process and transform NYC Taxi trip data. Leveraging the Medallion Architecture (Bronze, Silver, Gold layers) and Delta Lake, the pipeline efficiently ingests, cleans, and aggregates large datasets, ensuring high-quality, structured data ready for advanced analytics.

Pipeline Overview

Raw Data Ingestion (Bronze Layer)

Utilized Azure Data Factory to dynamically load raw data (CSV/Parquet) into Azure Data Lake Storage Gen2 (ADLS Gen2).

Configured a dynamic pipeline to handle varying data conditions, ensuring efficient ingestion based on file size and activity.

Data Transformation (Silver Layer)

In Azure Databricks, data was processed using PySpark to clean, transform, and enrich raw datasets.

Key transformations included adding derived columns such as trip_date and trip_year, and applying data quality checks.

Transformed data was then written back to ADLS Gen2 in Parquet format, ready for further aggregation.

Data Aggregation & Final Processing (Gold Layer)

The Gold Layer stored aggregated and optimized data in Delta Lake format, ensuring transactional consistency and enabling time travel for historical analysis.

Created Delta tables for key datasets (e.g., trip_zone, trip_type, tripdata2023) and used SQL in Databricks for efficient querying.

Enabled schema evolution to seamlessly handle changes in the incoming data structure.

Technologies Used

✅ Azure Data Lake Storage Gen2 (ADLS Gen2)

✅ Azure Databricks

✅ Delta Lake

✅ PySpark

✅ Azure Data Factory (Dynamic Pipeline)

✅ Microsoft Entra ID

Project Highlights

🚀 Scalability: Built a flexible pipeline that adapts to varying data sizes and complexities, ensuring smooth data processing.

✅ Data Quality: Implemented robust data transformations and validations to guarantee clean and structured data.

⚡ Efficient Storage & Performance: Utilized Delta Lake to optimize query performance, enable time travel, and handle large-scale data efficiently.

📜 Versioning: Leveraged Delta Lake’s versioning capabilities to track changes and maintain historical data.
