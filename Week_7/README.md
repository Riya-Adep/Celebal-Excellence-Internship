# Week 7 Assignment | Data Science Internship – Celebal Technologies
## 📚 Retrieval-Augmented Generation (RAG) Pipeline using LangChain, FAISS & TinyLlama

This project demonstrates the implementation of an **end-to-end Retrieval-Augmented Generation (RAG)** pipeline capable of answering questions from custom documents.

Unlike traditional Large Language Models (LLMs), which rely solely on their pre-trained knowledge, this system retrieves the most relevant information from uploaded documents before generating an answer. This significantly improves factual accuracy while reducing hallucinations.

The project uses a **Blockchain Technology PDF** as the knowledge source and enables users to ask natural language questions related to its contents.

---

# 📌 Project Overview

The complete workflow consists of:

- Loading PDF documents
- Extracting text from documents
- Splitting text into semantic chunks
- Generating vector embeddings
- Creating a FAISS vector database
- Retrieving relevant document chunks
- Generating grounded answers using TinyLlama
- Validating the complete RAG pipeline

---

# 🧠 What is Retrieval-Augmented Generation (RAG)?

Retrieval-Augmented Generation (RAG) combines **Information Retrieval** with **Large Language Models**.

Instead of relying only on the knowledge stored inside an LLM, the system first retrieves relevant information from external documents and then uses that retrieved context to generate accurate responses.

### RAG Workflow

```text
User Question
      │
      ▼
Generate Query Embedding
      │
      ▼
FAISS Vector Search
      │
      ▼
Retrieve Relevant Chunks
      │
      ▼
TinyLlama
      │
      ▼
Grounded Answer
```

---

# 📂 Project Structure

```text
Week-7-RAG-Pipeline/

│── Week7_Riya_Adep.ipynb
│── README.md
│── requirements.txt
│
└── documents/
      └── Blockchain_Technology.pdf
```

---

# 📄 Knowledge Base

Instead of using a structured dataset, this project uses a **Blockchain Technology PDF** as the knowledge source.

The uploaded document is processed automatically by the RAG pipeline.

Document Processing Pipeline:

- PDF Loading
- Text Extraction
- Recursive Character Chunking
- Vector Embedding Generation
- FAISS Index Creation

---

# ⚙️ Technologies Used

- Python
- LangChain
- Hugging Face Transformers
- Sentence Transformers
- FAISS
- TinyLlama-1.1B-Chat
- PyPDF
- Google Colab

---

# 🏗️ System Architecture

### Step 1
Document Loading

↓

### Step 2
Text Chunking

↓

### Step 3
Embedding Generation

↓

### Step 4
FAISS Vector Database

↓

### Step 5
Retriever

↓

### Step 6
TinyLlama Language Model

↓

### Step 7
Grounded Answer Generation

---

# 🧩 Embedding Model

| Component | Model |
|-----------|-------|
| Embedding Model | sentence-transformers/all-MiniLM-L6-v2 |
| Embedding Dimension | 384 Dimensions |

The embedding model converts every document chunk into a semantic vector representation.

---

# 🗄️ Vector Database

FAISS (Facebook AI Similarity Search)

Purpose:

- Fast similarity search
- Efficient vector indexing
- Semantic document retrieval
- Scalable search over document embeddings

---

# 🤖 Language Model

**TinyLlama-1.1B-Chat-v1.0**

TinyLlama is used as the language model responsible for generating grounded responses from the retrieved document context.

Why TinyLlama?

- Lightweight
- Open-source
- Runs in Google Colab
- No API Key Required
- Suitable for RAG demonstrations

---

# 📊 System Configuration

| Parameter | Value |
|-----------|-------|
| Chunk Size | 500 Characters |
| Chunk Overlap | 50 Characters |
| Embedding Model | all-MiniLM-L6-v2 |
| Embedding Dimension | 384 |
| Vector Store | FAISS |
| Retriever | Similarity Search |
| LLM | TinyLlama-1.1B-Chat |
| Programming Language | Python |

---

# 🔍 Validation

The RAG pipeline was validated using multiple natural language questions related to the uploaded Blockchain document.

Example Questions:

- What is Blockchain?
- What are the key characteristics of Blockchain?
- What is Proof of Work?
- What are the different types of Blockchain?
- What are the challenges of Blockchain Technology?

The system successfully retrieved the most relevant document chunks before generating grounded responses.

---

# 📈 Key Features

- PDF Document Ingestion
- Recursive Character Chunking
- Semantic Embedding Generation
- FAISS Vector Search
- Context Retrieval
- Grounded Question Answering
- Interactive User Input
- Validation Logs
- System Metrics Report

---

# 📌 Observations

- Successfully implemented an end-to-end Retrieval-Augmented Generation (RAG) pipeline.
- Semantic embeddings enabled retrieval based on meaning rather than exact keyword matching.
- FAISS efficiently indexed document embeddings for fast similarity search.
- TinyLlama generated context-aware responses using retrieved document chunks.
- Chunk overlap improved context preservation across document boundaries.
- The modular pipeline can be extended to support multiple documents and domains.

---

# 🚀 Future Improvements

- Implement Hybrid Search (Keyword + Semantic Search)
- Add Cross-Encoder Re-ranking
- Integrate ChromaDB or Pinecone
- Support Multiple PDF Documents
- Add Conversation Memory
- Deploy as a Streamlit Web Application
- Integrate OpenAI or Llama 3 models

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git
```

Install the required dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```text
Week7_Riya_Adep.ipynb
```

using:

- Google Colab
- Jupyter Notebook
- VS Code
---

# 📖 Key Learning Outcomes

- Retrieval-Augmented Generation (RAG)
- LangChain Framework
- Text Chunking
- Semantic Embeddings
- FAISS Vector Database
- Similarity Search
- Prompt Engineering
- Context-Aware Question Answering
- Large Language Models (LLMs)

---

# 👩‍💻 Author

**Riya Adep**

MCA Student
Data Science Internship – Celebal Technologies
