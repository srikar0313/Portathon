# 🌊 Maritime RAG Pipeline — Portathon 2024

## 🧩 Overview
This project was developed during **Portathon 2024**, an innovation hackathon focused on improving port operations and maritime logistics using data-driven AI systems.  
Our team built a **Maritime Retrieval-Augmented Generation (RAG) pipeline** that integrates domain-specific data, embeddings, and a Large Language Model (LLM) to provide intelligent, context-aware maritime insights.

---

## ⚙️ Problem Statement
Ports and maritime agencies handle massive amounts of **AIS (Automatic Identification System)** and cargo data, which is complex, unstructured, and hard to interpret in real time.  
The challenge was to build an **AI system capable of reasoning over this data** to assist in:
- Predicting **arrival times**  
- Assessing **port congestion risk**  
- Estimating **CO₂ emissions**  
- Performing **scenario-based analysis**

---

## 🚀 Our Solution
We designed an **Agentic AI pipeline** powered by **Retrieval-Augmented Generation (RAG)** that combines:
1. **AIS cargo data preprocessing** for structure and normalization  
2. **Vector-based retrieval** using **FAISS (Facebook AI Similarity Search)**  
3. **Domain adaptation** of a **LLaMA model** for maritime context understanding  
4. **LLM-based response generation** for forecasting and decision support  

The system can answer maritime-related queries and perform analytical reasoning on structured and semi-structured datasets.

---

## 🏗️ Architecture
Below is the high-level architecture of our pipeline:
AIS Cargo Data
↓
Data Preprocessing
	•	Cleaning / Filtering
	•	Normalization
	•	Feature Engineering
	•	Chunk Generation
↓
+—————––+                +–––––––––––+
| Q&A Generation    |                | Text Chunk Embedding |
| - Synthetic pairs |                | - Embedding Model    |
| - JSON data       |                | - Vector Conversion  |
+—————––+                +–––––––––––+
↓                                  ↓
LLaMA Fine-Tuning                     FAISS Vector Index
	•	Train Domain Adapter                - Metadata Store (pkl)
	•	Create Domain LLM                         ↓
__________________________________/
↓
RAG Pipeline
- Query → Embedding
- FAISS top-K Retrieval
- Domain-tuned LLM Inference
↓
Final Response
- Arrival Forecast
- Congestion Risk
- CO₂ Estimation
- Scenario Analysis
---

## 🧠 Key Components

| Component | Description |
|------------|-------------|
| **AIS Cargo Data** | Real or simulated maritime AIS datasets used for analysis |
| **Data Preprocessing** | Cleaning, normalization, and feature engineering of structured & unstructured data |
| **Embedding Generation** | Sentence-transformer embeddings for semantic search |
| **FAISS Vector Index** | Efficient retrieval of relevant text chunks |
| **Q&A Generation** | Synthetic data creation for domain adaptation |
| **LLaMA Fine-Tuning** | Lightweight fine-tuning to specialize the model for maritime terminology |
| **RAG Pipeline** | Combines retrieved chunks with LLM reasoning for grounded responses |

---

## 🧰 Tech Stack
- **Python 3.10+**
- **FAISS** – Vector similarity search  
- **Transformers / Sentence-Transformers** – Embedding generation  
- **LLaMA** – Large Language Model for domain reasoning  
- **Pandas / NumPy** – Data preprocessing and feature extraction  
- **Matplotlib / Seaborn** – Data visualization  
- **JSON / CSV** – Data storage formats  

---

## 📊 Example Use Cases
| Query | Example Response |
|--------|------------------|
| *“Forecast cargo arrivals for next 24 hours.”* | Predicts upcoming vessel arrivals based on AIS trends. |
| *“Estimate CO₂ emissions for current port activity.”* | Calculates expected emissions from current ship movements. |
| *“Analyze congestion risk at Port of Gothenburg.”* | Provides congestion probability using vessel density and arrival times. |

---


# Eagleeye

<img width="1901" height="856" alt="Screenshot 2025-10-03 212829" src="https://github.com/user-attachments/assets/5f1fb2ae-4c4a-4da2-967f-00fb71b4da81" />


<img width="1917" height="862" alt="Screenshot 2025-10-03 212913" src="https://github.com/user-attachments/assets/d5eeebd2-9496-4c51-90de-6f3775daecda" />
