# Airflow Docker Application

This application uses Apache Airflow to schedule and monitor workflows. It is containerized using Docker for easy deployment and scaling.

## Application Structure

The application consists of a single Airflow DAG (Directed Acyclic Graph) that performs the following tasks:

1. Print a welcome message.
2. Print the current date.
3. Fetch and print a random quote from the Quotable API.

The tasks are executed in the order specified above.

## Docker Configuration

The Dockerfile uses the `apache/airflow:latest` image as a base. It updates the package lists for upgrades and new package installations. Then, it installs git and cleans up the package lists.

The Docker Compose file sets up a service named `airflowwindowsdocker` that uses the `airflowwindowsdocker:aksh2` image. It mounts the `./airflow` directory to `/opt/airflow` in the container. The webserver is exposed on port 8080.

## How to Run

1. Build the Docker image: `docker build -t airflowwindowsdocker:aksh2 .`
2. Start the service: `docker-compose up`

After starting the service, you can access the Airflow webserver at `http://localhost:8080`.

