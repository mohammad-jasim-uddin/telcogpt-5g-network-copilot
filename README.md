# TelcoGPT – 5G Network Operations Copilot

TelcoGPT is a portfolio-ready AI project for telecom network operations.  
It uses Hugging Face embeddings, FAISS vector search, LangChain, and Streamlit to answer LTE/5G troubleshooting questions from telecom documents.

This project connects directly with:

- MSc in Mobile & Personal Communications
- BSc in Computer Science & Engineering
- Generative AI / Hugging Face skills
- Telecom / Network Operations domain knowledge
- AI Engineer, GenAI Engineer, Data/AI and MLOps job applications

## Features

- Telecom-focused RAG assistant
- Hugging Face sentence-transformer embeddings
- FAISS vector database
- Streamlit chatbot interface
- Source-grounded answers
- Supports `.txt` and `.pdf` files
- Includes sample LTE/5G knowledge base
- Local fallback LLM mode
- Hugging Face endpoint mode
- Clean GitHub-ready structure

## Architecture

```text
Telecom Documents
        |
        v
Document Loader
        |
        v
Text Chunking
        |
        v
Hugging Face Embeddings
        |
        v
FAISS Vector Database
        |
        v
Retriever
        |
        v
LLM Answer Generator
        |
        v
Streamlit Chatbot
```

## Folder Structure

```text
telcogpt-5g-network-copilot/
│
├── app.py
├── ingest.py
├── rag_pipeline.py
├── config.py
├── requirements.txt
├── README.md
├── .env.example
│
├── data/
│   └── sample_telecom_knowledge.txt
│
├── vectorstore/
├── screenshots/
├── src/
│   ├── document_loader.py
│   ├── prompts.py
│   └── utils.py
│
└── tests/
    └── test_project_structure.py
```

## Installation

```bash
cd telcogpt-5g-network-copilot

python -m venv venv
```

Activate virtual environment:

Windows:
```bash
venv\Scripts\activate
```

Mac/Linux:
```bash
source venv/bin/activate
```

Install dependencies:
```bash
pip install -r requirements.txt
```

## Environment Setup

Copy `.env.example` to `.env`.

Windows:
```bash
copy .env.example .env
```
Mac/Linux:
```bash
cp .env.example .env
```

Default mode is local:
```env
TELCOGPT_LLM_MODE=local
```
For Hugging Face endpoint mode:
```env
TELCOGPT_LLM_MODE=endpoint
HUGGINGFACEHUB_API_TOKEN=your_token_here
```

## Build Vector Database

```bash
python ingest.py
```

## Run the App
```bash
streamlit run app.py
```

## Example Questions
```text
What causes RRC connection failure?
How do I troubleshoot high packet loss in an LTE site?
What is the eNodeB reset procedure?
Why does handover failure happen?
Generate an incident summary for a 5G site outage.
```

## Add Your Own Telecom Documents

Put your telecom `.txt` or `.pdf` files inside the `data/` folder, then rebuild the vector database:

```bash
python ingest.py
```

## Portfolio CV Description

**TelcoGPT – 5G Network Operations Copilot**  
Built a Hugging Face-powered Retrieval-Augmented Generation chatbot for telecom network operations. The system uses sentence-transformer embeddings, FAISS vector search, LangChain, and an LLM pipeline to answer LTE/5G troubleshooting questions from technical documents. Demonstrated practical skills in Generative AI, Hugging Face, RAG, vector databases, prompt engineering, Python, Streamlit, and telecom domain problem-solving.


## LinkedIn Post

Introducing TelcoGPT – 5G Network Operations Copilot

I'm excited to share my AI engineering portfolio project, combining telecommunications expertise with Generative AI, Machine Learning and Agentic AI.

The project explores how artificial intelligence can support modern telecommunications network operations.

Key capabilities:

🔹 Retrieval-Augmented Generation (RAG)

🔹 5G network KPI analysis

🔹 Machine learning-based fault classification

🔹 Network anomaly detection

🔹 Explainable AI using SHAP

🔹 Multi-agent incident management

🔹 Interactive Streamlit dashboards

Technology stack: Python, LangChain, LangGraph, FAISS, Scikit-learn, XGBoost and Streamlit.

This project demonstrates my interest in applying AI to real-world telecommunications and network operations challenges.

🔗 GitHub Repository: \[https://github.com/mohammad-jasim-uddin/telcogpt-5g-network-copilot\]

I would welcome feedback, suggestions and collaboration from AI engineers, data scientists and telecommunications professionals.

If you find this project useful, please consider giving it a ⭐ on GitHub.

#ArtificialIntelligence #MachineLearning #GenerativeAI #AgenticAI #Telecommunications #5G #Python #DataScience #OpenSource #GitHub
```
```

**Notes**

The first run may take time because Hugging Face models are downloaded locally.
For low-resource computers, endpoint mode is recommended.

</> Bash
git clone https://github.com/mohammad-jasim-uddin/telcogpt-5g-network-copilot.git
cd telcogpt-5g-network-copilot
pip install -r requirements.txt
python ingest.py
streamlit run app.py

**Support the project**
If TelcoGPT is useful to you, consider giving the repository a ⭐.
