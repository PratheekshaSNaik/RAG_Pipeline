# 🔎 RAG Pipeline (Retrieval-Augmented Generation)

A modular Python-based implementation of a simple Retrieval-Augmented Generation (RAG) system using keyword-based retrieval and LiteLLM for response generation.

This project demonstrates how modern AI systems combine **retrieval + generation** to produce grounded and context-aware responses.

---

## 🎯 Objective

Design and implement a simple RAG workflow:

```
User Question → Retrieve Relevant Documents → Send Context to LLM → Generate Answer
```

The goal is to understand how LLMs can reduce hallucination by grounding outputs in external knowledge sources.

---

## 🚀 Features

* 📚 Local knowledge base using text files
* 🔎 Keyword-based document retrieval
* 🤖 LLM integration via LiteLLM
* 🔐 Secure API key handling with dotenv
* 💻 Interactive CLI interface
* 🧩 Clean modular architecture

---

## 🛠️ Tech Stack

* Python
* LiteLLM
* Groq API
* python-dotenv

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/PratheekshaSNaik/RAG_Pipeline.git
cd RAG_Pipeline
```

### 2. Install dependencies

Since no virtual environment is used, install globally:

```bash
python -m pip install -r requirements.txt
```

Or manually:

```bash
python -m pip install litellm python-dotenv
```

---

## 🔐 Setup Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_key_here
```

⚠️ Make sure your `.env` file is NOT pushed to GitHub.

---

## 🚫 Important (Security)

Ensure `.env` is added to `.gitignore`:

```
.env
```

---

## ▶️ Run the Project

```bash
python main.py
```

The application will:

1. Accept a question via CLI
2. Retrieve relevant documents from `knowledge_base/`
3. Send retrieved context to the LLM
4. Generate and display the final answer

---

## 🏗 Architecture Overview

### 1️⃣ Retriever Layer (`retriever.py`)

* Loads documents from `knowledge_base/`
* Performs simple keyword-based matching
* Returns the most relevant document content

### 2️⃣ LLM Layer (`llm_layer.py`)

* Connects to Groq via LiteLLM
* Sends retrieved context + user query
* Generates final response

### 3️⃣ RAG Pipeline (`rag_pipeline.py`)

* Orchestrates retrieval and generation phases
* Acts as the workflow controller

### 4️⃣ CLI Interface (`main.py`)

* Handles user interaction
* Passes queries into the RAG pipeline

---

## 📁 Project Structure

```
RAG_PIPELINE/
│
├── __pycache__/
│   ├── llm_layer.cpython-314.pyc
│   ├── rag_pipeline.cpython-314.pyc
│   └── retriever.cpython-314.pyc
│
├── knowledge_base/
│   ├── ai_notes.txt
│   └── ml_notes.txt
│
├── llm_layer.py
├── retriever.py
├── rag_pipeline.py
├── main.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

---

## 🎓 Learning Outcomes

After completing this project, you will:

* Understand the fundamentals of RAG architecture
* Learn how retrieval improves LLM response grounding
* Build modular AI pipelines
* Separate retrieval logic from generation logic
* Implement secure API handling

---

## 🚀 Why This Matters

Modern AI systems are not standalone LLM calls.

They use:

* Retrieval systems
* Knowledge bases
* Modular orchestration
* Secure configuration management

This project builds foundational understanding of how production-level RAG systems are structured.

---

## 🔮 Future Improvements

* Replace keyword retrieval with embedding-based semantic search
* Integrate FAISS or a vector database
* Implement document chunking & scoring
* Add Streamlit / FastAPI web interface
* Add evaluation metrics

---

## 🙌 Acknowledgements

Groq for high-speed LLM inference

LiteLLM for unified model access

Open-source community
