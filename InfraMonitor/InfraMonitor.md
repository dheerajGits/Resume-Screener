# STGI Hackathon: Build Your Own Observability Platform

## Background

In modern cloud environments, monitoring and observability are crucial for keeping applications running smoothly. In this hackathon, your challenge is to create a basic cloud monitoring tool. It will collect, process, and display logs and metrics from a Kubernetes cluster (control plane as well as pods).

## Challenge

You will set up a Kubernetes cluster (using MiniKube) with two applications, a PostgreSQL and a MySQL database, running on your local machine. Your task is to build a monitoring solution that collects logs from the applications running in the Minikube cluster, authenticates them, stores them in a time series database, and visualizes them in a custom dashboard.

---

## Requirements

### Initial Setup (Instructions provided)
- Use the given setup to create a Minikube cluster.
- The cluster will host two apps and databases.
- Follow the instructions to get your environment ready before building the monitoring tool.

### Log Collection
- Use any log/metrics collection tool like Fluent Bit, FluentD, or Logstash to gather logs from the application pods and database pods running in the Minikube cluster.
- Ensure these logs are sent to a backend service for further processing.

### Backend Service
- Develop a backend service to receive logs from the log collector.
- Implement basic authentication to ensure logs come from trusted sources like Fluent Bit.
- Process and store the logs in a time series database or a suitable storage solution.

### Time Series Database
- Set up a time series database to store the logs.
- Ensure logs are organized and easy to query.

### Custom Visualization Dashboard
- Build a web-based dashboard to display the logs stored in the database via different widgets.
- Include features like search and filtering to explore the data.
- Visualize important metrics like error rates, traffic, and performance.

> **Note:** You must build the dashboard from scratch. Using pre-built tools like Grafana is not preferred.

### Database Metrics Monitoring
- Collect metrics from the PostgreSQL database (e.g., query performance or resource usage).
- Use tools like Fluent Bit to collect these metrics and display them alongside your logs.

### AWS Integration
- You will be provided access to some AWS resources via AWS access keys.
- Collect logs or metrics from the AWS resources and integrate them into your backend.
- Show how AWS data combined with Kubernetes pod logs improves your monitoring platform.

### Efficient Searching Capabilities (Bonus)
- Add powerful features like keyword-based search, filters, and tags to streamline the search process.
- Include customizations like date-time filtering, allowing users to precisely track and analyze events or issues.

---

## Suggested Tools

- **Web Development for Visualization:** Use any stack (React, Django, Go, Node, etc.) to build your custom dashboard.

---

## Evaluation Criteria

- **Functionality:** Does your solution effectively collect, process, and visualize logs?
- **Usability:** Is the dashboard easy to use?
- **Completeness:** Does the tool provide useful insights and is it well-structured?

**Bonus Point:**
- Efficient search and filtering capabilities.

---
## Initial Setup

1. **Install Docker**
   - Ensure Docker is installed and running on your system. If not already installed, download and install Docker from the [official Docker website](https://www.docker.com/get-started).

2. **Install and Start Minikube**
   - Install Kubectl
   - Install Minikube on your local machine by following the instructions on the [Minikube installation page](https://minikube.sigs.k8s.io/docs/start/).
   - Start a Minikube cluster:
     ```bash
     minikube start
     ```
   - Set up the Kubernetes cluster using Minikube.

4. **Clone Sample Applications**
   - Clone the following two sample application codes and use the respective databases (MySQL and PostgreSQL) for these applications:
     - [app-1](https://github.com/tanishsummit/PyEditorial)
     - [app-2](https://github.com/manjillama/docker-node-crud-mysql)

5. **Create Kubernetes Deployments and Services**
   - Create Kubernetes deployments and services for both applications and the MySQL/PostgreSQL databases.
   - Ensure the applications are running on different ports.

6. **Sanity Check**
   - Once the apps and databases are deployed, verify they are running correctly by accessing their endpoints.
   - Take a basic functionality check for both applications to ensure everything is set up properly.
