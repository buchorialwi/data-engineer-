# 🚖 NYC Taxi Data Pipeline: Medallion Architecture

## 📌 Project Overview
This project demonstrates an end-to-end Data Engineering ETL pipeline using Databricks, Apache Spark, and Delta Lake. The pipeline processes raw New York City Taxi data to analyze peak hours and calculate average fares, providing actionable insights for driver scheduling.

## 🏗️ Architecture (Medallion Pattern)
The pipeline is designed using the Medallion Architecture to progressively clean and aggregate data:
* **Bronze Layer:** Ingests raw taxi trip data (`.parquet` format) directly from cloud storage.
* **Silver Layer:** Cleanses and transforms the data (filters for valid passenger counts, distances, and specific timeframes) using Spark SQL.
* **Gold Layer:** Aggregates the data to calculate total rides and average fare amounts grouped by the hour of the day.

## 🛠️ Technologies & Skills Demonstrated
* **Environment:** Databricks
* **Languages:** PySpark, Spark SQL
* **Storage:** Delta Lake
* **Key Concepts:** 
  * Lazy Evaluation & Parallel Processing
  * Delta Table Maintenance (`OPTIMIZE`, `ZORDER`, `VACUUM`)
  * Time Travel & Transaction Logs

## 🚀 How to Run
This pipeline was developed in Databricks. To replicate:
1. Import the `.ipynb` notebook into a Databricks Workspace.
2. Attach to a running compute cluster.
3. Run the cells sequentially to build the Bronze, Silver, and Gold tables.
