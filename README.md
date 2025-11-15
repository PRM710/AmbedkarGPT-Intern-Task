# Ambedkar Q&A System --- Setup Guide

This project uses **LangChain + ChromaDB + FAISS + Ollama (Mistral
7B)**\
to create a fully local RAG-based Q&A system.

------------------------------------------------------------------------

## ✅ 1. Install Ollama & Pull Mistral Model

Make sure **Ollama** is installed.

Then pull the model:

    ollama pull mistral

------------------------------------------------------------------------

## ✅ 2. Clone the Repository

    git clone https://github.com/PRM710/BR_LLM.git
    cd BR_LLM

------------------------------------------------------------------------

## ✅ 3. Backend Setup

### ▶ Step 1 --- Enter Backend Folder

    cd backend

### ▶ Step 2 --- Create Virtual Environment

    python -m venv venv

### ▶ Step 3 --- Activate venv

**Windows:**

    venv\Scripts\activate

**Mac/Linux:**

    source venv/bin/activate

------------------------------------------------------------------------

## ✅ 4. Install Python Dependencies (Exact Versions)

Install **in this exact order**:

    pip install langchain==0.1.16
    pip install langchain-community
    pip install langchain-text-splitters
    pip install chromadb
    pip install sentence-transformers
    pip install ollama
    pip install faiss-cpu

------------------------------------------------------------------------

## ✅ 5. Run the Backend

### ▶ Run using Python only (simple mode)

    python main.py

### ▶ Run API server (for frontend integration)

    uvicorn server:app --reload

API will start at:

    http://127.0.0.1:8000

------------------------------------------------------------------------

## ✅ 6. Frontend Setup (React)

### ▶ Step 1 --- Enter frontend folder

    cd frontend

### ▶ Step 2 --- Install dependencies

    npm install
    npm install axios

### ▶ Step 3 --- Start development server

    npm run dev

Frontend will run on:

    http://localhost:5173

------------------------------------------------------------------------

## 🚀 API Endpoint

Send questions to:

    POST /ask

Body:

``` json
{ "question": "Your question here" }
```

------------------------------------------------------------------------

## 🎉 You're Ready!

Your full RAG system (Backend + Frontend + Ollama Mistral) is now
running locally.
