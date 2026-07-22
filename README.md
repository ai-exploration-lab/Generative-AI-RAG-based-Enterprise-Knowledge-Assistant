# PolicyAssist AI - Enterprise RAG Knowledge Assistant

A Retrieval-Augmented Generation (RAG) based Generative AI assistant that allows users to ask questions from enterprise PDF documents.

The system retrieves relevant information from documents using semantic search and generates context-aware answers using Large Language Models (LLMs).

## Project Overview

This project demonstrates an end-to-end RAG pipeline:

PDF Documents
      |
Document Loading
      |
Text Chunking
      |
Embedding Generation
      |
FAISS Vector Database
      |
Semantic Retrieval
      |
LLM Response Generation


## Features

- PDF document ingestion
- Text chunking and preprocessing
- HuggingFace sentence embeddings
- FAISS vector similarity search
- Retrieval-Augmented Generation
- Context-aware answers
- Source document tracking
- Basic RAG response evaluation
- Interactive Q&A interface


## Tech Stack

- Python
- LangChain
- HuggingFace Transformers
- Sentence Transformers
- FAISS
- FLAN-T5
- PyPDF


## Workflow

1. Load PDF documents
2. Split documents into smaller chunks
3. Generate embeddings
4. Store embeddings in FAISS vector database
5. Retrieve relevant chunks based on user query
6. Generate answers using LLM


## Example Questions

- What documents are required for cashless hospitalization?
- Can dependents be added after enrollment?
- What are the exclusions under the insurance policy?


## Future Enhancements

- Streamlit web interface
- FastAPI backend
- RAGAS evaluation
- Docker deployment
- Cloud deployment
- User authentication

