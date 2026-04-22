# 📄 RAG PDF Question Answering System using Gemini + Pinecone + LangChain

## 🚀 Project Overview

This project implements a **Retrieval-Augmented Generation (RAG) pipeline** that allows users to ask questions from a **PDF document** and receive **accurate context-based answers** using **Google Gemini**, **LangChain**, and **Pinecone Vector Database**.

Instead of generating generic answers like traditional LLMs, this system retrieves relevant information directly from the uploaded PDF and generates responses strictly based on document context.

---

## 🧠 Architecture Workflow

```
PDF Document
     ↓
PyPDFLoader
     ↓
Text Chunking
     ↓
Gemini Embeddings
     ↓
Pinecone Vector Database
     ↓
MultiQueryRetriever
     ↓
Gemini LLM
     ↓
Final Answer
```

---

## ⚙️ Tech Stack

* Python
* LangChain
* Google Gemini API
* Pinecone Vector Database
* PyPDF Loader
* RecursiveCharacterTextSplitter
* MultiQueryRetriever
* dotenv

---

## 📌 Features

* Ask questions from any PDF document
* Context-aware answers using Gemini LLM
* Embedding generation using Gemini embedding model
* Vector storage with Pinecone
* Multi-query retrieval optimization
* Reduced hallucination responses
* Production-style RAG pipeline architecture

---

## 📂 Project Workflow

### Step 1: Load PDF

PDF document is loaded using PyPDFLoader.

### Step 2: Split Document

Document is divided into smaller chunks using RecursiveCharacterTextSplitter.

```
chunk_size = 1000
chunk_overlap = 100
```

### Step 3: Generate Embeddings

Each chunk is converted into vector embeddings using Gemini embedding model:

```
models/embedding-001
```

### Step 4: Store Embeddings

Embeddings are stored inside Pinecone vector database for similarity search.

### Step 5: MultiQueryRetriever

Improves retrieval accuracy by generating multiple variations of the user query automatically.

Example:

User query:

```
Key highlights of budget
```

Generated variations:

```
main announcements
important findings
major points
```

### Step 6: Retrieval QA Chain

Relevant document chunks are retrieved and passed to Gemini LLM to generate final answers.

---

## 🔐 Environment Variables Setup

Create a `.env` file and add:

```
GOOGLE_API_KEY=your_gemini_api_key
PINECONE_API_KEY=your_pinecone_api_key
```

---

## 📦 Installation

Clone repository:

```
git clone https://github.com/Sanapd/RAG_GEMINI_PINECONE_PDF.git
```

Navigate into folder:

```
cd RAG_GEMINI_PINECONE_PDF
```

Create virtual environment:

```
python -m venv venv
```

Activate environment (Windows):

```
venv\Scripts\activate
```

Activate environment (Mac/Linux):

```
source venv/bin/activate
```

Install dependencies:

```
pip install -r requirements.txt
```

---

## ▶️ Run Project

Open and run:

```
RAG_GEMINI_PINECONE_PDF.ipynb
```

Example question:

```
What are the key highlights of this document?
```

---

## 🎯 Use Cases

* Research paper assistant
* Financial report analyzer
* Study material chatbot
* Enterprise document search
* Legal document QA system
* Policy document assistant

---

## 💼 Resume Project Description

Developed a document-based question-answering system using **LangChain, Google Gemini, and Pinecone** that retrieves relevant document chunks and generates accurate responses. Implemented embedding generation, vector storage, and multi-query retrieval optimization to improve response accuracy and reduce hallucinations.

---

## ⭐ Key Learning Outcomes

* Understanding RAG architecture
* Working with vector databases
* Implementing embedding pipelines
* Using Gemini API with LangChain
* Building document-based QA systems
* Improving retrieval using MultiQueryRetriever

---

## 👩‍💻 Author

**Bhumika Sanap**
