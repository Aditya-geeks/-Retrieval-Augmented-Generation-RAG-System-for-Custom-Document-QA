# 📄 Retrieval-Augmented Generation (RAG) System for Custom Document Question Answering

> A local Retrieval-Augmented Generation (RAG) pipeline that enables users to ask natural language questions from their own PDF documents using LangChain, FAISS, BM25, and Google's FLAN-T5 model.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![LangChain](https://img.shields.io/badge/LangChain-Framework-green)
![FAISS](https://img.shields.io/badge/FAISS-VectorDB-orange)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)
![License](https://img.shields.io/badge/License-MIT-red)

---

# 📌 Overview

Large Language Models (LLMs) often generate incorrect or outdated information because they rely only on their pre-trained knowledge.

This project solves that problem using **Retrieval-Augmented Generation (RAG)**.

Instead of asking the LLM directly, the system first retrieves relevant information from uploaded PDF documents and then generates answers based only on those retrieved documents.

This significantly improves:
- ✅ Accuracy
- ✅ Reliability
- ✅ Explainability
- ✅ Reduced Hallucinations

---

# 🚀 Features

- 📄 Upload one or multiple PDF documents
- ✂ Automatic document chunking
- 🧠 Semantic embeddings using Sentence Transformers
- 🔍 Hybrid Retrieval (FAISS + BM25)
- 🤖 Context-aware answer generation using FLAN-T5
- ⚡ Fast semantic search
- 🎯 Reduced hallucinations
- 💻 Fully local pipeline (No paid APIs required)

---

# 🏗 System Architecture

```
                User Uploads PDF
                       │
                       ▼
             Text Extraction (PyPDF)
                       │
                       ▼
               Document Chunking
                       │
                       ▼
        Sentence Transformer Embeddings
                       │
                       ▼
               FAISS Vector Database
                       │
             + BM25 Keyword Search
                       │
                       ▼
           Retrieve Relevant Chunks
                       │
                       ▼
          Prompt + Retrieved Context
                       │
                       ▼
              Google FLAN-T5 Model
                       │
                       ▼
                Final Generated Answer
```

---

# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Programming Language | Python |
| Framework | LangChain |
| Embedding Model | all-MiniLM-L6-v2 |
| Vector Database | FAISS |
| Keyword Retrieval | BM25 |
| LLM | google/flan-t5-base |
| PDF Processing | PyPDF |
| Data Processing | Pandas, NumPy |

---

# 📂 Project Structure

```
RAG-System/
│
├── data/
│   ├── pdfs/
│
├── embeddings/
│
├── vector_store/
│
├── models/
│
├── app.py
├── rag_pipeline.py
├── requirements.txt
├── README.md
└── utils.py
```

---

# ⚙ Workflow

### Step 1
Upload PDF documents.

↓

### Step 2
Extract text from the PDFs.

↓

### Step 3
Split text into overlapping chunks.

↓

### Step 4
Generate embeddings using Sentence Transformers.

↓

### Step 5
Store embeddings inside FAISS.

↓

### Step 6
Create BM25 index for keyword search.

↓

### Step 7
User asks a question.

↓

### Step 8
Retrieve relevant chunks using:
- Semantic Search (FAISS)
- Keyword Search (BM25)

↓

### Step 9
Send retrieved context + question to FLAN-T5.

↓

### Step 10
Generate an accurate answer.

---

# 📊 Why Hybrid Search?

Instead of relying on only semantic search or only keyword search, this project combines both.

### FAISS

✔ Understands semantic meaning

Example:

Car ≈ Automobile

---

### BM25

✔ Finds exact keyword matches

Example:

"TensorFlow"

"LangChain"

---

Combining both improves retrieval accuracy for real-world enterprise documents.

---

# 🧠 Why RAG?

Traditional LLM

```
Question
     │
     ▼
    LLM
     │
     ▼
Answer (May Hallucinate)
```

RAG

```
Question
     │
     ▼
Retrieve Relevant Documents
     │
     ▼
 Context + Question
     │
     ▼
      LLM
     │
     ▼
Grounded Answer
```

Advantages:

- More accurate
- Less hallucination
- Uses private documents
- Easy to update knowledge
- No retraining required

---

# 📸 Sample Use Cases

- Company Knowledge Assistant
- Legal Document Search
- Research Paper QA
- Medical Documentation
- HR Policy Assistant
- University Notes Assistant
- Enterprise Chatbot

---

# 📈 Future Improvements

- Multi-PDF Chat
- Conversational Memory
- OCR Support
- Image-based PDF Support
- Citation Generation
- Source Highlighting
- Pinecone / Milvus Integration
- Streamlit Web Interface
- Docker Deployment
- Cloud Deployment (Azure/AWS/GCP)
- Multi-language Support

---

# 🎯 Learning Outcomes

Through this project I learned:

- Retrieval-Augmented Generation (RAG)
- LangChain
- Prompt Engineering
- Vector Databases
- FAISS
- BM25 Retrieval
- Sentence Embeddings
- Large Language Models
- Semantic Search
- Enterprise AI System Design

---

# 📌 Installation

```bash
git clone https://github.com/yourusername/RAG-System.git

cd RAG-System

pip install -r requirements.txt
```

Run the project

```bash
python app.py
```

---

# 📚 Requirements

```text
langchain
transformers
sentence-transformers
faiss-cpu
rank-bm25
numpy
pandas
pypdf
torch
scikit-learn
```

---

# 💡 Key Highlights

- End-to-End Local RAG Pipeline
- Hybrid Retrieval (FAISS + BM25)
- Open Source LLM
- Enterprise-ready Architecture
- No Paid API Required
- Optimized for Document Question Answering

---

# 👨‍💻 Author

**Aditya Kasara**

📧 Email: adityakasera678@gmail.com

🔗 LinkedIn: *(Add Your Profile)*

💻 GitHub: *(Add Your GitHub Profile)*

---

## ⭐ If you found this project useful, don't forget to Star the repository!
