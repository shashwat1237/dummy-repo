# 🛡️ Project Aegis
### AI Data Resilience & Schema Drift Defense Platform

![Status](https://img.shields.io/badge/Status-Active-success)
![Platform](https://img.shields.io/badge/Google_Cloud-Run-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Focus](https://img.shields.io/badge/Focus-AI_Data_Observability-purple)

---

## 📌 Overview
**Project Aegis** is a next-generation **data resilience and AI assurance platform** designed to defend modern data pipelines against **silent schema drift** — one of the most common and costly causes of AI model and analytics failures.

Aegis continuously monitors data lineage, simulates schema failures, calculates downstream blast radius, and auto-heals pipelines using AI-generated SQL virtual patches — all without downtime.

---

## ❗ The Problem
Modern AI systems rely on complex data pipelines across databases, APIs, warehouses, and models. Small schema changes often result in:

* **Silent AI model corruption**
* **Broken dashboards and reports**
* **Incorrect business decisions**
* **Hours to days of debugging**

> **Static pipelines = Fragile pipelines.**

---

## 🚀 Core Innovation: Data Lineage–Driven Risk Engine
Aegis treats data pipelines as a **connected graph**, not isolated tables. By modeling sources, transformations, warehouses, and AI consumers as a dependency graph, Aegis can:

1.  **Predict impact** before failure occurs.
2.  **Measure blast radius** in milliseconds.
3.  **Translate technical failure** into business risk (Data VIX).

---

## ⭐ Key Features
* 🧠 **End-to-End Data Lineage Visualization**
* 💥 **Schema Drift Simulation (Chaos Injection)**
* 📉 **Real-Time Blast Radius Analysis**
* 📊 **Data VIX Risk Scoring (0–100)**
* 🤖 **AI-Generated SQL Remediation (Virtual Patching)**
* 🩺 **One-Click Global Heal**
* ☁ **Cloud-Native, Scale-to-Zero Architecture**

---

## 🧰 Technology Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.10, TypeScript |
| **Backend** | FastAPI |
| **Frontend** | React 18 (Vite) |
| **Visualization** | React Flow |
| **State Management** | Zustand |
| **Containerization** | Docker |
| **Cloud Platform** | Google Cloud Run |
| **Registry** | Google Container Registry |

---

## 🏗 Architecture

```mermaid
graph TD
    A[Aegis Frontend<br/>Lineage Graph + Risk UI] -->|HTTP/REST| B[Aegis Backend<br/>Risk Engine + AI Copilot]
    
    subgraph Data Layer
    C[(Data Sources<br/>Postgres, APIs)]
    D[AI / Dashboards<br/>ML Models, BI]
    end
    
    B -->|Monitors| C
    B -->|Protects| D
    C -->|Flows to| D
