Apache airflow on Windows docker using python

# Welcome DAG

This is an Apache Airflow Directed Acyclic Graph (DAG) named `welcome_dag`. It consists of three tasks that print a welcome message, the current date, and a random quote.

## Dependencies

- Apache Airflow
- Python
- requests

## Tasks

1. `print_welcome`: This task prints a welcome message to the console.
2. `print_date`: This task prints the current date to the console.
3. `print_random_quote`: This task fetches a random quote from the Quotable API and prints it to the console.

## Execution

The tasks are executed in the following order: `print_welcome` -> `print_date` -> `print_random_quote`.

## Schedule

The DAG is scheduled to run daily at 23:00.

## How to Run

To run this DAG, you need to have Apache Airflow installed and configured on your machine. Once you have Airflow set up, you can place this Python script in the `dags` directory of your Airflow installation. Airflow will automatically pick up the DAG and you can trigger it manually or wait for the next scheduled run at 23:00.

## Note

This DAG uses the `requests` library to fetch a random quote from an API. Make sure you have the `requests` library installed in your Python environment where Airflow is running.
