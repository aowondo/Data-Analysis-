# 💧 Water Billing System

## 📌 Overview
The **Water Billing System** is designed to automate utility billing by generating invoices and providing an operations dashboard for consumption monitoring.  
It supports **multi-house management**, tracks usage, and integrates billing calculations in **Excel** with support from **Python for sample data generation**.

---

## ⚡ Key Features
- **Automated Invoice Generation** – Create one-click invoices in PDF format directly from the dashboard.  
- **Operations Dashboard** – Monitor water consumption across houses, analyze trends, and flag spikes.  
- **Consumption Spike Simulation** – Includes a **Python data generator** that introduces realistic usage patterns to mimic real-world data.  
- **Multi-House Management** – Each house has a dedicated worksheet with its own billing table.  
- **Flexible Data Entry** – Input form automatically appends records to the correct house worksheet.  

---

## 🏗️ Project Structure
| File | Description |
|---------------|-------------|
| `sample data generator.ipynb` | Generates sample data, including **spikes** in consumption for realistic testing. |
| `water_management.xlsm` | Core Excel workbook with operations dashboard and invoice generator. |
| `water_meter_sample_data` | Contains generated data for each house (billing tables). |
| `README.md` | Documentation file (this file). |

---

## 🖥️ Workflow
1. **Generate Data** using the Python script to populate realistic consumption records.  
2. **Update House Sheets** with new readings via the input form.  
3. **Monitor Dashboard** for spikes, anomalies, and summaries.  
4. **Generate Invoice** from the dashboard with a single click.  

---

## 🛠️ Tech Stack
- **Excel (VBA Macros)** – Core billing logic and dashboard functionality.  
- **Python (Pandas, ReportLab)** – Data generator + PDF automation.  
- **Markdown** – Project documentation.  

---

## 📊 Sample Data Simulation
The Python script adds **randomized consumption values** with built-in **spikes** to test anomaly detection and billing accuracy.  

```python
# Example snippet from data generator
import random

def generate_consumption(days=30):
    return [random.randint(5, 15) if i % 10 != 0 else random.randint(30, 50) for i in range(days)]

print(generate_consumption())
