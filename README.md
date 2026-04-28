# 🚀 MonitoringForDevOps – Observability Stack

A production-inspired **observability stack** designed to monitor applications and infrastructure using industry-standard tools. This project demonstrates how to collect, store, and visualize **metrics and logs** in a containerized environment.

---

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-0A1F44?style=for-the-badge&logo=grafana&logoColor=white)
![Promtail](https://img.shields.io/badge/Promtail-F2A900?style=for-the-badge&logo=grafana&logoColor=black)
![cAdvisor](https://img.shields.io/badge/cAdvisor-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-6929C4?style=for-the-badge&logo=opentelemetry&logoColor=white)

---

## 📌 Overview

This project sets up a **centralized monitoring system** using Docker, enabling visibility into:

* Application behavior
* Container performance
* Host-level system metrics
* Log aggregation and analysis

It follows a modular and scalable architecture aligned with real-world DevOps practices.

---

## 🧰 Tech Stack

| Category       | Tool           | Purpose                                        |
| -------------- | -------------- | ---------------------------------------------- |
| Metrics        | Prometheus     | Time-series metrics collection & storage       |
| Logs           | Loki           | Log aggregation and indexing                   |
| Log Collection | Promtail       | Ships logs from containers to Loki             |
| Containers     | cAdvisor       | Container-level metrics (CPU, memory, network) |
| Host Metrics   | Node Exporter  | System-level metrics (CPU, RAM, disk)          |
| Visualization  | Grafana        | Unified dashboards for logs & metrics          |
| Orchestration  | Docker Compose | App orchestration                          |

---

## ⚙️ What This Project Does

* Collects **application and container logs**
* Scrapes **system and container metrics**
* Stores logs in **Loki** and metrics in **Prometheus**
* Visualizes everything in **Grafana dashboards**
* Provides a **single-pane observability view**

---

### 🔍 Architecture & Project Flow

![Architecture & Project Flow](Assets/ThreeTierChatApp.png)

---

## 📚 Project Snapshots

### 📊 Monitoring & Alerts

- 📈 **Monitoring Dashboard (Prometheus + Grafana)**  

  ![Monitoring](Assets/monitoring.png)

---

## 📊 Key Capabilities

* 📈 Real-time system and container monitoring
* 📜 Centralized log aggregation
* 🔍 Queryable logs and metrics
* 📉 Performance bottleneck identification
* 🧩 Modular architecture for scaling

---


---
