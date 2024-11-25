
# Realtime Data Streaming | End-to-End Data Engineering Project

## Table of Contents
- [Introduction](#introduction)
- [System Architecture](#system-architecture)
- [What You'll Learn](#what-youll-learn)
- [Technologies](#technologies)
- [Getting Started](#getting-started)
- [Watch the Video Tutorial](#watch-the-video-tutorial)

## Introduction

This project serves as a comprehensive guide to building an end-to-end data engineering pipeline. It covers each stage from data ingestion to processing and finally to storage, utilizing a robust tech stack that includes Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra. Everything is containerized using Docker for ease of deployment and scalability.



The project is designed with the following components:

- **Data Source**: We use `randomuser.me` API to generate random user data for our pipeline.
- **Apache Airflow**: Responsible for orchestrating the pipeline and storing fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper**: Used for streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of our Kafka streams.
- **Apache Spark**: For data processing with its master and worker nodes.
- **Cassandra**: Where the processed data will be stored.

## What You'll Learn

- Setting up a data pipeline with Apache Airflow
- Real-time data streaming with Apache Kafka
- Distributed synchronization with Apache Zookeeper
- Data processing techniques with Apache Spark
- Data storage solutions with Cassandra and PostgreSQL
- Containerizing your entire data engineering setup with Docker

## Technologies

- Apache Airflow
- Python
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker

## Getting Started

1. Clone the repository:
    ```bash
    https://github.com/Saumyasundaram23/Real-time-Data-Streamimg.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Real-time-Data-Streamimg
    ```

3. Install the Python libraries:
    ```bash
    pip install pyspark cassandra-driver
    ```
4. Run the Cassandra database:
    ```bash
    cassandra
    ```
This project demonstrates a real-time data streaming pipeline using Apache Spark, Apache Kafka, and Cassandra. Here's a brief explanation of the workflow:

Kafka Integration: The pipeline listens to a Kafka topic (users_created) for incoming JSON messages.
Spark Streaming: Spark processes the Kafka data stream in real time, extracting and transforming the data using a predefined schema.
Cassandra Storage: The transformed data is written to a Cassandra table (created_users) for storage and future analysis.
Fault Tolerance: Checkpointing ensures data reliability and consistency during streaming.
This system is ideal for scalable, distributed real-time data processing in use cases such as logging, event tracking, and user registration pipelines.
