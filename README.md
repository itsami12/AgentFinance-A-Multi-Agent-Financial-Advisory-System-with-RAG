# AgentFinance – A Multi-Agent Financial Advisory System with RAG

## 🌟 Overview
AgentFinance is an **AI-driven multi-agent financial advisory system** designed to deliver **cohesive, accurate, and high-speed financial guidance** across **taxation, investment analysis, and economic forecasting**.

The system leverages a **Coordinator-based multi-agent architecture** combined with **Retrieval-Augmented Generation (RAG)** to integrate structured financial data with authoritative unstructured documents. This design ensures **low latency, minimal hallucination, and explainable outputs**, making AgentFinance suitable for high-stakes financial decision support.

Unlike monolithic LLM systems, AgentFinance decomposes financial reasoning into **specialized autonomous agents**, each grounded in domain-specific data and tools.

---

## ✨ Features
- 🤖 **Multi-Agent Orchestration**
  - Central **Coordinator Agent** routes queries intelligently.
  - Supports both **single-domain and cross-domain financial queries**.

- 💰 **Tax Advisory Agent**
  - Accurate federal tax computation aligned with **IRS 2024 regulations**.
  - Achieves **$0.09 Mean Absolute Error (MAE)**.
  - Powered by **1,290 IRS document chunks** via RAG.

- 📈 **Investment Advisory Agent**
  - Market analysis using historical **stock and cryptocurrency data**.
  - Risk-based portfolio recommendations (Conservative, Moderate, Aggressive).
  - Enhanced with **280 market research documents**.

- 📊 **Data Analyst Agent**
  - Macroeconomic and consumer trend analysis.
  - Uses datasets from **World Bank, CEX, and national surveys**.
  - Enables forecasting and segmentation analysis.

- 🔎 **Retrieval-Augmented Generation (RAG)**
  - Reduces hallucinations through semantic document grounding.
  - Enables transparent and explainable responses.

- ⚡ **High Performance**
  - **94.3% routing accuracy**
  - **742 ms P95 latency**
  - **100% success rate** across evaluation queries

---

## 🧰 Tech Stack

| **Category** | **Tools & Frameworks** |
|-------------|------------------------|
| **LLM & Reasoning** | Tool-augmented LLM Agents |
| **Multi-Agent System** | Coordinator + Specialist Agents |
| **RAG Engine** | ChromaDB |
| **Embeddings** | all-MiniLM-L6-v2 (384-dim) |
| **Database** | SQLite |
| **Backend** | Python |
| **Data Sources** | IRS, Stock & Crypto Markets, World Bank |

---

## 🗂 System Architecture

![AgentFinance Architecture](assets/arciture.png)

**Flow Overview**

User Query  
↓  
Coordinator Agent  
↓  
Specialized Agents  
(Tax Agent | Investment Agent | Data Analyst Agent)  
↓  
RAG Subsystem  
↓  
Relational Database + Vector Store  
↓  
Integrated Financial Advice

---

## 🗄 Data Infrastructure
- **Relational Database**
  - 18 tables
  - 183,777 structured records

- **Vector Store**
  - Total documents: 1,794
    - Tax: 1,290 (72%)
    - Investment: 280 (15.5%)
    - Analyst: 224 (12.5%)

- **Chunking Strategy**
  - Chunk size: 1,000 characters
  - Overlap: 200 characters
  - Retrieval: Top-K = 5 (cosine similarity)

---

## 🚀 Setup Instructions

### **Prerequisites**
- Python 3.10+
- SQLite
- Virtual environment support
- Recommended: 8GB RAM

---
ame/AgentFinance-A-Multi-Agent-Financial-Advisory-System-with-RAG.git
cd AgentFinance-A-Multi-Agent-Financial-Advisory-System-with-RAG
