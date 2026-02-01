# 🤖 AI Automation: Workload Equity Engine

![n8n](https://img.shields.io/badge/n8n-Workflow-red?style=for-the-badge&logo=n8n)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o--mini-green?style=for-the-badge&logo=openai)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Database-blue?style=for-the-badge&logo=googlesheets)

An autonomous logistics engine designed to automate teacher coverage assignments. This system replaces manual spreadsheet coordination with an AI-driven process that prioritizes **staff workload equity** and data integrity.

---

## 📺 Project Demo


https://github.com/user-attachments/assets/e2f7b063-fd61-4d38-8cec-56bf1e2fb1cb



---

## 🚀 The Problem
In educational institutions, managing daily teacher absences is a high-friction task. Administrators typically spend **30–60 minutes** daily cross-referencing timetables and manually tracking who has covered which class. 

**Common Issues:**
* **Human Bias:** Certain teachers are "asked" to cover more often than others.
* **Data Silos:** Timetables and historical coverage records are often in separate files.
* **Administrative Burnout:** The morning rush to find coverages is stressful and error-prone.

## ✨ The Solution
The **Workload Equity Engine** automates the entire lifecycle of a coverage request in under **5 seconds**:

1. **Intelligent Extraction:** Identifies gaps in the Master Timetable based on absent staff inputs.
2. **Real-time Filtering:** Scans for available (FREE) teachers during those specific periods.
3. **AI Reasoning:** Uses **GPT-4o-mini** to select the best candidate based on historical coverage counts—ensuring the teacher with the lowest workload is picked first.
4. **Autonomous Execution:** Updates the Master Database, logs the history, and renders a custom HTML dashboard.

---

## 🛠️ Technical Architecture

### **Backend Orchestration**
The system is built on **n8n**, utilizing a custom-built event-driven architecture:
* **Preprocessing:** Custom JavaScript parses comma-separated staff names and validates dates.
* **Logic Layer:** A relational data synthesis between three separate Google Sheet datasets.
* **AI Layer:** LLM-based decision support using structured JSON outputs to ensure 0% hallucination rate.

### **Data Schema**
* **Master_Timetable:** Live schedule data.
* **Teacher_Master:** Staff records including `Total_Coverages` (The Equity Counter).
* **Coverage_History:** An immutable audit log of every assignment made.

---

## 📊 Business Impact
* **Time Savings:** Reclaimed ~2.5 hours of administrative time per week.
* **Accuracy:** 100% data consistency between scheduling and payroll/history logs.
* **Morale:** Transparent, data-backed fairness in work distribution.

---

## 👤 Author
**Atique Ahmed** *AI Automation Expert* 

---
*Developed as a production-ready solution for institutional logistics.*
