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
│   └── sales_orchestrator.py      # Airflow DAG defining the workflow
├── notebooks/
│   └── transform_sales.py         # PySpark transformation logic
├── scripts/
│   └── init_db.sql                # Postgres schema setup
├── .gitignore                     # Prevents secrets/env leakage
└── README.md
