# Realtime Data Streaming Pipeline

## Overview

This project demonstrates the implementation of an end-to-end real-time data streaming pipeline using modern data engineering tools. The pipeline simulates real-time user data ingestion, processes it using Apache Spark, and stores the results in Cassandra, enabling efficient querying and analysis.

## Technologies Used

**Apache Airflow**: Workflow orchestration and task scheduling.
**Apache Kafka**: Real-time data streaming.
**Apache Zookeeper**: Cluster management for Kafka.
**Apache Spark**: Stream processing for data transformations and aggregations.
**Cassandra**: Scalable NoSQL database for processed data storage.
**Docker**: Containerization for consistent and portable deployment.

## Pipeline Workflow

Data Ingestion: Simulated real-time user data fetched from the randomuser.me API is streamed via Kafka.
Orchestration: Airflow DAGs schedule and manage the ingestion, processing, and storage tasks.
Stream Processing: Spark processes the streamed data in real time to clean, enrich, and transform it.
Data Storage: The processed data is stored in Cassandra for downstream analytics and querying.

## Features

End-to-end data engineering solution for real-time data.
Scalable and reliable architecture using Apache Kafka and Spark.
Efficient querying and analysis with Cassandra’s distributed storage.
Modular design with Docker for seamless deployment and scalability.

## How to Run

**Set Up Environment**:
Ensure Docker and Docker Compose are installed.
Clone the repository to your local machine.
**Install Dependencies**:
Navigate to the project directory and run docker-compose up to start all services (Airflow, Kafka, Zookeeper, Spark, Cassandra).
**Run the Pipeline**:
Use the Airflow UI to trigger the DAGs for data ingestion and processing.
Monitor data flow through Kafka, Spark, and into Cassandra.
**Verify Output**:
Query the Cassandra database to verify processed data.

## Directory Structure

bash
Copy code
/dags # Airflow DAGs for workflow orchestration
/logs # Log files for debugging and monitoring
/script # Custom scripts for data processing
/spark_stream.py # Spark Streaming application
docker-compose.yml # Docker Compose configuration
requirements.txt # Python dependencies
Data engineering architecture.png # Architecture diagram of the pipeline

## Future Improvements

Add support for real-time analytics dashboards using tools like Grafana.
Implement error handling and data quality checks within the pipeline.
Scale the architecture to support higher data throughput.
