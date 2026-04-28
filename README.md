# 🚀 MonitoringForDevOps – Observability Stack

A production-inspired **observability stack** designed to monitor applications and infrastructure using industry-standard tools. This project demonstrates how to collect, store, and visualize **metrics and logs** in a containerized environment.

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
| Orchestration  | Docker Compose | Service orchestration                          |

---

## ⚙️ What This Project Does

* Collects **application and container logs**
* Scrapes **system and container metrics**
* Stores logs in **Loki** and metrics in **Prometheus**
* Visualizes everything in **Grafana dashboards**
* Provides a **single-pane observability view**

---

## 🔍 Architecture & Flow

```text
Application / Containers
        │
        ├── Logs → Promtail → Loki ─────────┐
        │                                   │
        ├── Container Metrics → cAdvisor ─┐  │
        │                                  ├→ Prometheus ──┐
        ├── Host Metrics → Node Exporter ─┘                │
                                                          ↓
                                                    Grafana
```

### Flow Breakdown

* **Logs Pipeline**

  * Applications write logs → Docker stores them → Promtail collects → Loki stores → Grafana visualizes

* **Metrics Pipeline**

  * cAdvisor → container metrics
  * Node Exporter → host metrics
  * Prometheus → scrapes & stores → Grafana visualizes

---

## 📊 Key Capabilities

* 📈 Real-time system and container monitoring
* 📜 Centralized log aggregation
* 🔍 Queryable logs and metrics
* 📉 Performance bottleneck identification
* 🧩 Modular architecture for scaling

---

## 🚀 Getting Started

### 1. Clone Repository

```bash
git clone https://github.com/kartikmaha/MonitoringForDevOps.git
cd MonitoringForDevOps
```

---

### 2. Start the Stack

```bash
docker compose up -d
```

---

### 3. Access Services

| Service    | URL                   |
| ---------- | --------------------- |
| Grafana    | http://localhost:3000 |
| Prometheus | http://localhost:9090 |
| cAdvisor   | http://localhost:8080 |

---

### 4. Grafana Login

```text
Username: admin
Password: admin
```

---

## 📁 Project Structure (High-Level)

```text
.
├── docker-compose.yml
├── prometheus/
│   └── prometheus.yml
├── promtail/
│   └── promtail.yml
├── grafana/
│   └── provisioning/
└── app/
```

---

## 🧠 Design Highlights

* **Separation of concerns** between logs and metrics
* **Pull-based metrics collection** (Prometheus)
* **Push-based log aggregation** (Promtail → Loki)
* **Container-native monitoring** using cAdvisor
* **Centralized visualization** via Grafana

---

## 🧹 Cleanup

To stop and remove all services:

```bash
docker compose down
```

To remove volumes (reset data):

```bash
docker compose down -v
```

---

## 💡 Future Enhancements

* Add **Alertmanager** for alerting
* Integrate **OpenTelemetry** for tracing
* Add **custom application metrics**
* Deploy on **Kubernetes (Helm-based setup)**

---

## 📣 Final Note

This project reflects a **real-world observability setup**, demonstrating the ability to design and deploy monitoring systems using modern DevOps tooling. It highlights practical knowledge of **metrics, logging, and system visibility**, essential for production-grade environments.

---
