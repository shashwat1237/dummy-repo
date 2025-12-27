# 🛡️ Project Aegis
### AI Data Resilience & Schema Drift Defense Platform

![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.10+-blue)
![React](https://img.shields.io/badge/react-18-61DAFB)
![Google Cloud](https://img.shields.io/badge/GCP-Cloud%20Run-4285F4)

---

## 📌 Overview
**Project Aegis** is a next-generation data resilience and AI assurance platform designed to defend modern data pipelines against **silent schema drift** — one of the most common and costly causes of AI model and analytics failures.

Aegis continuously monitors data lineage, simulates schema failures, calculates downstream blast radius, and auto-heals pipelines using AI-generated SQL virtual patches — all without downtime.

## ❗ Why This Exists — The Problem
Modern AI systems rely on complex data pipelines across databases, APIs, warehouses, and models. Static pipelines are fragile pipelines. Small schema changes often cause:
*   **Silent AI model corruption** (feeding bad data into training/inference).
*   **Broken dashboards** and inaccurate business reports.
*   **Incorrect business decisions** based on stale or malformed data.
*   **Hours to days of manual debugging** to find the root cause.

## 🚀 Core Innovation: Data Lineage–Driven Risk Engine
Aegis treats data pipelines as a **connected graph**, not isolated tables. By modeling sources, transformations, warehouses, and AI consumers as a dependency graph, Aegis can:

1.  **Predict impact** before a failure occurs.
2.  **Measure blast radius** in milliseconds.
3.  **Translate technical failure into business risk** via the **Data VIX** (Volatility Index).

---

## ⭐ Key Features
*   🧠 **End-to-End Data Lineage Visualization:** Interactive graph representing your entire data ecosystem.
*   💥 **Schema Drift Simulation (Chaos Injection):** Test your pipeline's resilience by simulating column drops or type changes.
*   📉 **Real-Time Blast Radius Analysis:** Instantly see which models and dashboards are affected by a specific change.
*   📊 **Data VIX Risk Scoring:** A 0–100 volatility index representing the health of your data environment.
*   🤖 **AI-Generated SQL Remediation:** "Virtual Patching" that generates SQL logic to bypass or fix broken schemas.
*   🩺 **One-Click Global Heal:** Deploy fixes across the entire graph instantly.
*   ☁ **Cloud-Native Architecture:** Built to scale-to-zero on Google Cloud Run.

---

## 🏗 Architecture
```text
┌────────────────────────────────┐
│        Aegis Frontend          │
│   (React + Lineage Graph UI)   │
└───────────────┬────────────────┘
                │
                v
┌────────────────────────────────┐
│        Aegis Backend           │
│   (FastAPI + AI Risk Engine)   │
└───────────────┬────────────────┘
                │
    ┌───────────┴───────────┐
    │                       │
┌───▼──────────┐      ┌─────▼──────────┐
│ Data Sources │      │ AI/Dashboards  │
│ (Postgres)   │      │ (ML Models)    │
└──────────────┘      └────────────────┘

## 🧰 Technology Stack

| Component | Tech | Language/Framework |
| :--- | :--- | :--- |
| **Backend** | FastAPI | Python 3.10 |
| **Frontend** | React 18 (Vite) | TypeScript |
| **Visualization** | React Flow | Dependency Graphing |
| **State Management** | Zustand | Lightweight State |
| **Infrastructure** | Docker | Containerization |
| **Cloud Platform** | Google Cloud Run | Serverless Hosting |

---

## 📁 Project Structure

```text
Aegis-platform/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── LineageGraph.tsx   # Data lineage visualization
│   │   │   ├── SchemaInspector.tsx # Column-level inspection
│   │   │   ├── RiskPanel.tsx       # Data VIX display
│   │   │   └── CopilotDrawer.tsx   # AI remediation UI
│   │   └── data/                  # Mock / demo datasets
├── backend/
│   ├── api/
│   │   ├── lineage.py             # Lineage APIs
│   │   ├── chaos.py               # Schema drift simulation
│   │   ├── risk.py                # Blast radius & VIX logic
│   │   └── heal.py                # AI remediation endpoints
│   ├── services/
│   │   ├── blast_radius.py        # Graph traversal logic
│   │   ├── data_vix.py            # Risk scoring engine
│   │   └── remediation.py         # AI SQL patch generation
├── Screenshots/                   # Demo visuals
├── docker/                        # Deployment configurations
├── README.md
└── LICENSE

⚙️ Installation & Setup
Clone the Repository
code
Bash
git clone https://github.com/<your-username>/Aegis-platform.git
cd Aegis-platform
Run Backend
code
Bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
Run Frontend
code
Bash
cd frontend
npm install
npm run dev
☁️ Deployment
Aegis is optimized for Google Cloud Run using a scale-to-zero strategy to minimize costs.
🔗 Live Demo: View Project Aegis Online
🧭 Future Roadmap
Real-time Connectors: Direct integration with Snowflake, BigQuery, and Databricks.
Automated CI/CD: Prevent "bad" schema migrations during the PR process.
Multi-tenant Support: Enterprise-grade workspace isolation.
Root Cause Explanation: Natural language explanations for why a pipeline failed using LLMs.
📜 License
Distributed under the MIT License. See LICENSE for more information.
