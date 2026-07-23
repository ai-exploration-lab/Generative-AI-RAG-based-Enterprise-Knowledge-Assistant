# PolicyAssist AI - Enterprise RAG Knowledge Assistant

> **A Retrieval-Augmented Generation (RAG) based AI assistant for querying enterprise PDF documents using semantic search and Large Language Models (LLMs).**

---

# Project Overview

PolicyAssist AI is an end-to-end Retrieval-Augmented Generation (RAG) application that enables users to ask natural language questions from enterprise PDF documents.

Instead of relying solely on a Large Language Model (LLM), the system first retrieves the most relevant information from enterprise documents using semantic similarity search and then generates accurate, context-aware responses.

This project demonstrates the complete RAG workflow using LangChain, Hugging Face, Sentence Transformers, FAISS, and FLAN-T5.

---

# Features

- PDF document ingestion
- Automatic document parsing
- Intelligent text chunking
- Hugging Face sentence embeddings
- FAISS vector database
- Semantic similarity search
- Retrieval-Augmented Generation (RAG)
- Context-aware answer generation
- Interactive Question & Answer interface
- Easily extendable for multiple enterprise documents

---

# Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Core Programming Language |
| LangChain | RAG Pipeline |
| Hugging Face Transformers | LLM Integration |
| Sentence Transformers | Text Embeddings |
| FAISS | Vector Database |
| FLAN-T5 | Large Language Model |
| PyPDF | PDF Processing |
| Jupyter Notebook | Development Environment |

---

# Architecture

```text
                    ┌─────────────────────┐
                    │ Enterprise PDF Docs │
                    └──────────┬──────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │ PyPDF Document Loader   │
                  └──────────┬──────────────┘
                             │
                             ▼
             ┌─────────────────────────────────┐
             │ Recursive Character Splitter    │
             └──────────┬──────────────────────┘
                        │
                        ▼
         ┌──────────────────────────────────────┐
         │ Sentence Transformer Embeddings      │
         └──────────┬───────────────────────────┘
                    │
                    ▼
          ┌────────────────────────────┐
          │ FAISS Vector Database      │
          └──────────┬─────────────────┘
                     │
             User Question
                     │
                     ▼
          ┌────────────────────────────┐
          │ Semantic Similarity Search │
          └──────────┬─────────────────┘
                     │
                     ▼
          Relevant Document Chunks
                     │
                     ▼
          ┌────────────────────────────┐
          │ FLAN-T5 Language Model     │
          └──────────┬─────────────────┘
                     │
                     ▼
            Context-Aware Answer
```

---

# Project Workflow

```text
Load PDF Documents
        │
        ▼
Extract Text
        │
        ▼
Split Documents into Chunks
        │
        ▼
Generate Embeddings
        │
        ▼
Store Embeddings in FAISS
        │
        ▼
User Asks Question
        │
        ▼
Retrieve Relevant Chunks
        │
        ▼
Generate Prompt
        │
        ▼
FLAN-T5 Generates Response
        │
        ▼
Display Final Answer
```

---

# Folder Structure

```text
Generative-AI-RAG-based-Enterprise-Knowledge-Assistant/

│
├── documents/
│   └── medical_policy.pdf
│
├── PolicyAssist_AI.ipynb
│
├── requirements.txt
│
└── README.md
```

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/Generative-AI-RAG-based-Enterprise-Knowledge-Assistant.git

cd Generative-AI-RAG-based-Enterprise-Knowledge-Assistant
```

---

## 2. Create a Virtual Environment

### macOS / Linux

```bash
python3 -m venv venv

source venv/bin/activate
```

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

---

## 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

---

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook:

```text
PolicyAssist_AI.ipynb
```

---

# How to Run the Project

Run each notebook cell in the following order:

```text
Cell 1
│
├── Load PDF Documents
│
▼
Cell 2
│
├── Split Documents into Chunks
│
▼
Cell 3
│
├── Generate Embeddings
│
▼
Cell 4
│
├── Create FAISS Vector Database
│
▼
Cell 5
│
├── Create Retriever
│
▼
Cell 6
│
├── Load FLAN-T5 Model
│
▼
Cell 7
│
├── Create Prompt Template
│
▼
Cell 8
│
├── Build RAG Pipeline
│
▼
Cell 9
│
└── Ask Questions
```

---

# End-to-End Execution Flow

```text
                START
                  │
                  ▼
        Load PDF Documents
                  │
                  ▼
      Extract Text from PDFs
                  │
                  ▼
      Split into Smaller Chunks
                  │
                  ▼
Generate Sentence Embeddings
                  │
                  ▼
 Store Embeddings in FAISS
                  │
                  ▼
        User Asks Question
                  │
                  ▼
Retrieve Similar Chunks
                  │
                  ▼
      Generate Prompt
                  │
                  ▼
      FLAN-T5 Generates Answer
                  │
                  ▼
      Display Final Response
                  │
                  ▼
                 END
```

---

# Example Questions

- What documents are required for cashless hospitalization?
- What is covered under the medical insurance policy?
- Can dependents be added after enrollment?
- What are the exclusions under the insurance policy?
- What is the waiting period?
- Who is eligible under this policy?
- Is maternity covered?
- What is the claim settlement process?

---

# Sample Output

**Question**

```text
What documents are required for cashless hospitalization?
```

**Answer**

```text
The insured employee must provide the required identity proof,
health insurance ID card, hospital admission details, and complete
the cashless request form. The hospital then submits the request
to the insurance provider for authorization.
```

---

# Components Used

| Component | Description |
|------------|-------------|
| PyPDFLoader | Reads PDF documents |
| RecursiveCharacterTextSplitter | Splits documents into chunks |
| HuggingFaceEmbeddings | Generates vector embeddings |
| FAISS | Stores vector embeddings |
| Retriever | Retrieves relevant chunks |
| Prompt Template | Creates contextual prompts |
| FLAN-T5 | Generates context-aware answers |

---

# Future Enhancements

- Streamlit Web Application
- FastAPI Backend
- REST APIs
- Multi-PDF Knowledge Base
- Chat Memory
- Source Citations
- Hybrid Search (Vector + Keyword)
- OpenAI / Azure OpenAI Integration
- RAGAS Evaluation
- Docker Deployment
- Kubernetes Deployment
- User Authentication
- Enterprise Document Management

---

# Author

**Mohammed H**

Senior Frontend Engineer
