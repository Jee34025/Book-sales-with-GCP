# Book sales Pipeline
This project demonstrates a full data pipeline built using Apache Airflow to extract, transform, and load data into Google BigQuery, along with a separate Exploratory Data Analysis (EDA) process conducted using Google Colab.

---

## Project Overview

- EDA: Conducted in Google Colab to gain insights into sales trends and customer behavior.
- Data Source: MySQL database containing book sales information.

- ETL Pipeline:

    - Extract: Retrieve data from MySQL using Airflow's MySqlHook.

    - Transform: Process and merge data using Pandas.

    - Load: Store the transformed data as Parquet files in Google Cloud Storage (GCS) and load into BigQuery using GCSToBigQueryOperator.

---

## Setup Instructions
1. Clone the Repository
    ```
    git clone https://github.com/Jee34025/Book-sales-with-GCP.git

    cd Book-sales-with-GCP
    ```
2. Configure Environment Variables

- Copy the example environment file
    ```
    cp .env.example .env
    ```
- Edit .env to include your specific configurations

    ```
    MYSQL_CONNECTION=mysql_default
    CONVERSION_RATE_URL=https://your-api-url.com/
    ```


3. Set Up Airflow
    - Ensure Airflow is installed and configured.

    - Place main.py into your Airflow dags/ directory.

    - Start the Airflow scheduler and webserver.

## DAG Overview

![Airflow DAG Flow](https://github.com/Jee34025/Book-sales-with-GCP/images/dag_flow.png)

    





