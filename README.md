# Real-Time Order Processing System

## Executive Summary

This project implements a scalable real-time backend system for processing customer orders using Golang, Kafka, and containerized microservices. It is designed for high-concurrency environments and fault-tolerant communication across distributed services.

## Tech Stack

- Golang, Apache Kafka, Docker, Kubernetes, AWS

## Quick Start

1. Run Kafka server by Docker:

   ```sh
   sudo docker pull apache/kafka:3.7.0
   ```

2. Run the image on the required port 9292:

   ```sh
   sudo docker run -p 9092:9092 apache/kafka:3.7.0
   ```

3. Run the producer HTTP server:

   ```sh
   cd producer
   go run main.go
   ```

4. Run the worker (consumer) HTTP server:
   ```sh
   cd worker
   go run main.go
   ```
