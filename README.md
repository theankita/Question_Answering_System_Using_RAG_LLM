# Intelligent Document Question Answering System using RAG and Large Language Models

## Overview

This project is an AI-powered Intelligent Document Question Answering System built using Retrieval Augmented Generation (RAG), FAISS Vector Database, Sentence Transformers, and Large Language Models.

The system allows users to upload PDF documents and ask questions based on their content. It retrieves the most relevant chunks from the document and generates accurate answers using a locally running LLM via Ollama.

The system can:

* Extract text from PDF documents
* Split text into meaningful overlapping chunks
* Generate semantic embeddings
* Store embeddings in FAISS vector database
* Perform fast semantic search
* Retrieve relevant context for a question
* Generate context-aware answers using Llama3

---

## Features

* Upload PDF documents for analysis
* Automatic text extraction from PDFs
* Intelligent chunking with overlap handling
* Semantic embeddings using Sentence Transformers
* Fast similarity search using FAISS
* Local LLM integration via Ollama
* Context-aware question answering
* Streamlit-based interactive UI
* Real-time document querying system
* RAG (Retrieval Augmented Generation) pipeline implementation

---

## Technologies Used

### Programming Language
* Python

### Web Framework
* Streamlit

### Machine Learning / AI
* Sentence Transformers
* FAISS
* Ollama
* Llama3

### Libraries
* PyPDF2
* NumPy
* Requests
* Streamlit

### Concepts
* Retrieval Augmented Generation (RAG)
* Vector Embeddings
* Semantic Search
* Prompt Engineering
* Large Language Models (LLMs)
* Vector Databases

## Project Structure

```bash
Intelligent_Document_QA_System/
│
├── app.py
├── requirements.txt
├── Uploaded_PDFs/
├── FAISS_Vector_DB/
├── Embedding_Model/
└── README.md
````
## Architecture Flow (RAG Pipeline)

```text
PDF Upload
    ↓
Extract Text from PDF
    ↓
Split Text into Overlapping Chunks
    ↓
Convert Chunks into Embeddings
    ↓
Store Embeddings in FAISS Index
    ↓
User Asks Question
    ↓
Convert Question into Embedding
    ↓
Retrieve Relevant Chunks
    ↓
Combine Context
    ↓
Send Prompt to LLM (Llama3 via Ollama)
    ↓
Generate Final Answer
```

## Core Modules

### 1. PDF Processing

Uses PyPDF2 to extract readable text from uploaded PDF files.

### 2. Text Chunking

Large text is split into smaller overlapping chunks (e.g., 500 chars with 100 overlap) to improve retrieval quality.

### 3. Embedding Generation

Sentence Transformers model (`all-MiniLM-L6-v2`) converts text into dense vector representations.

### 4. Vector Database (FAISS)

FAISS is used to store embeddings and perform fast similarity search.

### 5. Semantic Search

The user query is converted into embeddings and matched with stored document vectors.

### 6. LLM Integration

Ollama runs Llama3 locally and generates answers based only on retrieved context.

### 7. Prompt Engineering

Strict prompts ensure the model:

* Uses only provided context
* Avoids hallucination
* Produces structured answers

## Streamlit UI Features

* Clean modern interface
* PDF upload system
* Extracted text preview
* Chunk and embedding statistics
* Context viewer (expandable)
* Question input box
* Real-time answer generation
* Sidebar with project details

## How to Run the Project

### Step 1: Clone Repository

```bash
git clone [https://github.com/your_username/your_repository](https://github.com/theankita/Question_Answering_System_Using_RAG_LLM).git
```

### Step 2: Create Virtual Environment

```bash
python3 -m venv venv
```

### Step 3: Activate Environment

```bash
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows
```

### Step 4: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 5: Install Ollama

Download from:
[https://ollama.com](https://ollama.com)

Run model:

```bash
ollama run llama3
```

### Step 6: Run Application

```bash
streamlit run app.py
```

---

## Requirements

```txt
streamlit
PyPDF2
faiss-cpu
numpy
requests
sentence-transformers
torch
torchvision
transformers
scikit-learn
scipy
```

---

## Future Improvements

* Multi-document Q&A support
* Chat history memory
* Voice-based querying
* Cloud deployment (AWS / Azure)
* GPU acceleration for embeddings
* Highlight answers inside PDF
* Export chat results

## Author

Ankita Dnyanoba Shinde

GitHub: [https://github.com/theankita](https://github.com/theankita)
