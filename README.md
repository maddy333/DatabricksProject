# ✈️ Databricks Data Engineering Project – Flights Booking Use Case

## 🚀 Project Overview

This project simulates a **production-grade data engineering pipeline** built on the **Databricks Lakehouse Platform**, following the **Medallion Architecture** (Bronze, Silver, Gold). It demonstrates how raw flight booking data can be ingested, cleaned, transformed, and modeled into **business-ready analytics** using:

- **Incremental ingestion**
- **Schema evolution**
- **Declarative pipelines (DLT)**
- **Dimensional modeling**
- **dbt Cloud transformations**

The pipeline is fully **modular and automated**, showcasing **data quality enforcement**, **governance with Unity Catalog**, and modern **analytics engineering** workflows.

---

## 🧱 Architecture

![Architecture](architecture.png)

The project follows the **Medallion Architecture**, a layered approach that promotes scalable, governed, and high-quality data processing:

- 🔹 **Bronze Layer**: Raw data landing zone; ingested incrementally using **Databricks Autoloader**
- 🔸 **Silver Layer**: Cleaned and transformed data built with **Lakeflow Declarative Pipelines (DLT)**
- 🏅 **Gold Layer**: Highly refined, analytics-ready tables built using **star schema modeling**, including **dynamic SCDs and fact tables**

---

## ⚙️ Delta Live Tables (Silver Layer)

![DLT Pipeline](dlt_pipeline.png)  
![DLT Pipeline](dlt_pipeline01.png)

Silver layer logic is handled using **Databricks Lakeflow (formerly Delta Live Tables)**. These declarative pipelines enable:

- Automatic schema handling  
- Incremental updates  
- Built-in data quality enforcement  

---

## 💡 Key Features & Technologies

This project provides hands-on experience with modern, in-demand data engineering tools:

- 📥 **Incremental Ingestion**: File-based ingestion via **Spark Structured Streaming** and **Databricks Autoloader**
- 📂 **Dynamic Notebook Orchestration**: Parameterized notebooks for modular bronze ingestion
- 🧬 **Lakeflow / DLT Pipelines**: Schema evolution, upserts, and **Auto CDC API**
- 📊 **Dimensional Modeling (Star Schema)**:
  - **Dynamic SCD Type 1 Builder**: Converts any source into a slowly changing dimension using parameters
  - **Dynamic Fact Builder**: Builds fact tables with incremental loads and upserts
- 🖥️ **Databricks Free Edition + Serverless Compute**: Used for cost-effective, cloud-native execution
- 🔐 **Unity Catalog + Volumes**: Data governance and file management replacing traditional DBFS
- ✅ **Data Quality Rules**: Enforced using DLT `expect()` expectations (e.g., `expect all`, `drop`)
- 🔀 **Dynamic Joins & Filters**: SQL join conditions built dynamically using parameters
- 🔁 **Multi-threading**: Notebook execution in parallel for efficient ingestion workflows
- ⚙️ **dbt Cloud Integration**:
  - SQL-first transformations on top of the Gold layer
  - dbt Cloud IDE setup, model development, and project execution

---

## 📁 Project Dataset

The pipeline is built on a **realistic Flights Booking dataset**, structured to simulate enterprise-grade challenges like **incremental loads** and **SCDs**.

- 🧾 **Fact Table**:
  - `fact_bookings.csv` – booking transaction data  

- 🧩 **Dimension Tables**:
  - `dim_passengers.csv`  
  - `dim_flights.csv`  
  - `dim_airports.csv`

These datasets are used to demonstrate concepts such as **schema evolution**, **complex joins**, and **data modeling** in the context of the airline industry.

---
