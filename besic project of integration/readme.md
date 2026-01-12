# 🚀 Automated Multi-Source Sales Analytics Pipeline

A modern data engineering project demonstrating a hybrid-cloud ETL pipeline. This project orchestrates data movement from a **Local PostgreSQL** instance to **Databricks Community Edition** using **Apache Airflow**, with a mirrored CI/CD workflow between **GitLab** and **GitHub**.

## 🏗️ Architecture
1.  **Source:** Local PostgreSQL (Operational DB).
2.  **Orchestrator:** Apache Airflow (DAG management).
3.  **Compute/Transform:** Databricks (PySpark / Spark SQL).
4.  **Storage:** Delta Lake (Gold Layer summary tables).
5.  **DevOps:** GitLab (Primary Dev) mirrored to GitHub (Public Portfolio).

## 🛠️ Tech Stack
* **Orchestration:** Apache Airflow
* **Data Processing:** PySpark / Databricks
* **Database:** PostgreSQL
* **Version Control:** GitLab & GitHub
* **Language:** Python 3.x

## 📁 Project Structure
├── dags/
│   ├── sales_main_dag.py          # The Airflow orchestration file
│   └── utils/
│       └── helpers.py             # Reusable Python functions (e.g., logging)
├── notebooks/
│   └── silver_to_gold_sales.py    # Databricks PySpark transformation code
├── sql/
│   ├── postgres_init.sql          # Script to set up local DB
│   └── analytical_queries.sql     # Sample queries for the final Delta Table
├── config/
│   ├── airflow_connections.yaml   # (Reference only) Documentation for connections
│   └── databricks_job_config.json # JSON spec for the Databricks job
├── .gitignore                     # To hide .env, __pycache__, and DS_Store
├── README.md                      # Project documentation
└── requirements.txt               # List of python libraries needed