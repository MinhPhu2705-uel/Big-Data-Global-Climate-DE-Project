## 🌍 Overview

The Global Weather Analytics Platform is a production-grade data engineering project encompassing batch processing, streaming, analytics, and observability. It monitors weather conditions for 50 cities across 6 continents utilizing 16 containerized services with $0 in cloud spend. 

The platform architecture fetches data from the free Open-Meteo API and processes it through an hourly batch layer and a 5-minute interval streaming layer. It features robust automated data quality checks, anomaly detection using standard and robust z-scores, and fully automated dashboard provisioning.

---

## 🛠️ Tech Stack

| Layer | Tool | Key Characteristics |
| :--- | :--- | :--- |
| **Orchestration** | **Apache Airflow 2.8** | Utilizes CeleryExecutor to closely mirror real production environments. |
| **Streaming** | **Apache Kafka 3.5** | Provides durable, partitioned, and replayable message queues. |
| **Object Storage** | **MinIO** | Offers an S3-compatible API for easy future migration to AWS. |
| **Warehouse** | **PostgreSQL 15** | Supports composite primary keys, partial indexes, and window functions without extra infrastructure. |
| **Transformation** | **dbt Core 1.7** | Enables lineage graphs, column-level testing, and ephemeral intermediates. |
| **Dashboards** | **Grafana** | Uses provisioned-as-code JSON for instant, reproducible setups requiring zero clicks. |
| **Monitoring** | **Prometheus & Pushgateway** | Collects pull-based metrics to track pipeline health and Data Quality SLOs. |
| **Data Source** | **Open-Meteo API** | A completely free service offering 80 years of history with no API key or rate limits. |

---

## ⚡ Quick Start

### 1. Infrastructure Setup
Clone the repository and set up your environment variables:

```bash
git clone [https://github.com/YOUR_USERNAME/weather-analytics-platform](https://github.com/YOUR_USERNAME/weather-analytics-platform)
cd weather-analytics-platform
cp .env.example .env
