# 🐝 BeeHaven: End-to-End IoT Data Pipeline (Azure & Power BI)

## 📌 Executive Summary
**BeeHaven** is an industrial-grade data engineering ecosystem designed to monitor honeybee colony health. By orchestrating a pipeline that merges high-frequency IoT sensor data with external meteorological APIs, this project provides actionable insights into foraging patterns and honey production across multiple geographic sites.

## 🏗️ Data Architecture (Medallion Framework)
The pipeline leverages **Azure Synapse Analytics** to implement a scalable Medallion Architecture:

* **🥉 Bronze (Raw Layer):** Automated ingestion of heterogeneous JSON/CSV telemetry from Azure Data Lake Storage (ADLS) Gen2.
* **🥈 Silver (Curated Layer):** Real-time data cleaning using **PySpark**. Implemented advanced time-series interpolation to handle sensor gaps and schema normalization.
* **🥇 Gold (Analytical Layer):** * **Feature Engineering:** Executed complex temporal alignment to synchronize per-minute sensor data with hourly weather updates.
    * **Optimization:** Data modeling into aggregated **Parquet** files, reducing query latency for BI reporting.

## 💻 Technical Implementation
> [!IMPORTANT]  
> **Security First:** All credentials, connection strings, and API keys have been removed and managed via environment variables for security purposes.

### 📂 Repository Navigation
All technical assets have been organized into specific folders for review:
* **[Notebooks & Source Code](./notebooks)**: Contains all the Python and PySpark scripts used for data transformation and business logic.
* **[Architecture & Dashboards](./visuals)**: Includes high-resolution screenshots of the Azure Synapse pipelines and the final Power BI analytical reports.

## 📊 Visualizations & Insights
The final Power BI solution delivers high-impact analytical views (see the **visuals** folder for full graphs):
1.  **Environmental Correlation:** Quantifying the direct impact of external temperature on bee foraging activity.
2.  **Health Monitoring:** Analyzing weight fluctuations to detect honey production peaks or potential colony risks.

---

## 🛠️ Tech Stack & Tools
| Category | Technology |
| :--- | :--- |
| **Cloud Provider** | Microsoft Azure (ADLS Gen2, Synapse) |
| **Data Processing** | Python, PySpark, Pandas |
| **Orchestration** | Synapse Pipelines (ETL/ELT) |
| **Storage Format** | Apache Parquet (Columnar Storage) |
| **Visualization** | Power BI Desktop |

---

## 💡 Conclusion
This project demonstrates the complete lifecycle of a Data Engineering solution, from raw IoT ingestion to advanced cloud orchestration and business intelligence. By handling asynchronous time-series data and implementing a robust Medallion architecture on Azure, BeeHaven showcases a professional and scalable approach to environmental monitoring and industrial data processing.

---
*Developed by Tatiana Tchouakam
