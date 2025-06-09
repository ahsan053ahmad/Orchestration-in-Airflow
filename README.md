# Orchestration-in-Airflow

This repository contains the submission for a Data Engineering lab focused on orchestrating ETL pipelines using **Apache Airflow**. The assignment illustrates how to construct and manage directed acyclic graphs (DAGs) for scheduling and automating multi-step workflows.

---

### Business Problem

Modern data engineering requires orchestrating multiple tasks such as extraction, transformation, loading, validation, and cleanup. Manual scheduling of these operations is error-prone and unscalable. This lab demonstrates how to use Apache Airflow to solve that challenge by managing interdependent operations using well-defined DAGs.

---

### Project Objectives

- Understand the structure and scheduling logic of DAGs in Apache Airflow
- Implement a sample DAG for loading, transforming, and verifying data
- Schedule tasks to run at defined intervals
- Use Airflow operators such as `PythonOperator` and `BashOperator`
- Simulate alerts and notifications upon DAG failures or completions

---

### Solution Approach

1. **DAG Construction**
   - Defined the DAG's configuration with scheduling (`@daily`), retries, start date, etc.
   - Established task dependencies using the Airflow `>>` operator for sequential execution

2. **Operators Used**
   - `PythonOperator`: For executing Python data processing functions
   - `BashOperator`: For running shell scripts, used to simulate data ingestion

3. **Functions Implemented**
   - Load function: Reads and ingests data from a local or simulated external source
   - Transform function: Performs cleansing or enrichment of the ingested data
   - Verify function: Ensures the integrity and completeness of data after transformation

4. **Testing and Debugging**
   - DAG was validated and tested locally using the Airflow UI and CLI
   - Dummy tasks and alert messages were added to simulate a production-like DAG environment

---

### Business Value

This project illustrates how Airflow can be effectively used to:

- Automate recurring data workflows reliably
- Track and manage task dependencies visually
- Ensure data pipeline observability and debugging through logs and alerts
- Serve as a core orchestration framework for scalable data engineering pipelines

---

### Challenges Encountered

- Understanding DAG scheduling quirks (e.g., `start_date` in the past)
- Managing retries and catching task failures
- Debugging PythonOperator errors from within Airflow's logs

---
