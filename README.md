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
* **Language:** Python 3.12

🎯 Strategic Goals
1. Unified Orchestration
Goal: Move away from "crontabs" and manual scripts.

Vision: Use Airflow to provide a single pane of glass to monitor the health of the entire data journey, from a local Postgres row to a Cloud Delta Table.

2. Scalable Compute Separation
Goal: Keep the "Extract" light and the "Transform" heavy.

Vision: Use local resources only for data retrieval, offloading the expensive and complex aggregation logic to Spark on Databricks, allowing the system to handle millions of rows without crashing the local source.

3. DevOps Excellence (The Git Bridge)
Goal: Eliminate "Code Silos."

Vision: Use GitLab for internal development and CI/CD, while automatically mirroring to GitHub for public visibility and redundancy. This demonstrates a "Production-First" mindset where code is never stuck on a single machine.

4. Data Governance & Security
Goal: Zero-Trust Credential Management.

Vision: Demonstrate that passwords never enter the codebase. By using Secret Scopes and Environment Variables, the project envisions a world where a developer can lose their laptop, but the company's data remains secure.

🚀 The Future Roadmap (Scalability)
If this project were to grow, the vision includes:

Real-time Streaming: Moving from Batch (Airflow) to Streaming (Spark Structured Streaming).

Data Quality Checks: Integrating Great Expectations to stop the pipeline if the Postgres data is corrupted.

Infrastructure as Code: Using Terraform to deploy the Databricks clusters automatically.
