## 🌍 Overview

The Global Climate Data Engineering Project is a production-grade encompassing batch processing, streaming, analytics, and observability. It monitors weather conditions for 50 cities across 6 continents utilizing 16 containerized services. 

The platform architecture fetches data from the free **Open-Meteo API** and processes it through an hourly batch layer and a 5-minute interval streaming layer. It features robust automated data quality checks, anomaly detection using standard and robust z-scores, and fully automated dashboard provisioning.

---

## 🛠️ Tech Stack

| Layer | Tool |
| :--- | :--- |
| **Orchestration** | **Apache Airflow 2.8** |
| **Streaming** | **Apache Kafka 3.5** |
| **Object Storage** | **MinIO** |
| **Warehouse** | **PostgreSQL 15** |
| **Transformation** | **dbt Core 1.7** |
| **Dashboards** | **Grafana** |
| **Monitoring** | **Prometheus & Pushgateway** |
| **Data Source** | **Open-Meteo API** |

---

## ⚡Architecture
<img width="688" height="1517" alt="Gemini_Generated_Image_tvyvi1tvyvi1tvyv" src="https://github.com/user-attachments/assets/6bee0dfe-9e7b-4ad1-98d7-5f683212a4da" />

