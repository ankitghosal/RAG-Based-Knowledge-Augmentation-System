# 🌟RAG Based Knowledge Augmentation System 💎
### using Llama3, Langchain and ChromaDB
## Project Objective

In this notebook, we build a **Retrieval Augmented Generation (RAG)** system using **Llama 3**, **LangChain**, and **ChromaDB**. The goal is to enable question-answering over external documents (not part of the model’s training data) without fine-tuning the Large Language Model (LLM).

The system follows a two-step process:

1. **Retrieval** – relevant document chunks are fetched from a vector database.
2. **Generation** – the LLM uses the retrieved context to produce accurate answers.

This implementation uses a real-world dataset (EU AI Act 2023) to demonstrate how RAG improves factual correctness and reduces hallucinations.

---

## Definitions

* **LLM (Large Language Model)** – A deep learning model trained on large text corpora for NLP tasks
* **Llama 3** – Open-source LLM by Meta, used here via HuggingFace Transformers
* **LangChain** – Framework for building LLM-powered applications with chaining and orchestration
* **Vector Database** – Stores high-dimensional embeddings for semantic search
* **ChromaDB** – Lightweight, persistent vector database used for document retrieval
* **Embeddings** – Numerical vector representations of text generated using Sentence Transformers
* **RAG (Retrieval Augmented Generation)** – Combines retrieval systems with LLMs for grounded responses

---

## Model Details

* **Model**: Llama 3
* **Variant**: 8B Chat (HuggingFace format)
* **Framework**: Transformers
* **Optimization**: Quantization using `bitsandbytes` for efficient inference

The model is integrated via a HuggingFace pipeline and used as the **generator** in the RAG system.

---

## System Architecture

The RAG pipeline in this notebook consists of:

### 1. Document Processing

* Source: **EU AI Act (2023)**
* Documents are split into smaller chunks for efficient retrieval

### 2. Embedding Generation

* Uses **Sentence Transformers / HuggingFace embeddings**
* Converts text chunks into vector representations

### 3. Vector Storage

* Stored in **ChromaDB** with persistence enabled
* Enables fast semantic similarity search

### 4. Retrieval + Generation

* LangChain connects the retriever and LLM
* Relevant chunks are retrieved and passed to Llama 3 for answer generation

---

## What is a Retrieval Augmented Generation (RAG) System?

Large Language Models are powerful but limited to their training data and may hallucinate when handling unseen information.

RAG solves this by integrating external knowledge sources:

* **Retriever**: Finds relevant document chunks using embeddings and vector similarity
* **Generator**: Produces answers grounded in retrieved context

This approach ensures:

* More accurate answers
* Reduced hallucination
* Up-to-date and domain-specific knowledge integration

---

## Conclusion 

In this notebook, we demonstrate how combining **LangChain, ChromaDB, and Llama 3** creates an effective RAG system capable of answering questions about the EU AI Act with improved reliability. Future improvements can focus on better embeddings, chunking strategies, and advanced retrieval techniques.

**Future Work** ⚡✨

To further enhance the solution, we will focus on refining the RAG implementation. This will involve optimizing the document embeddings and exploring the use of more intricate RAG architectures.



#### **If you like this LLM Project do drop ⭐ to this repo**
#### Follow me on [![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ankitghosal/) &nbsp; [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ankitghosal)

---
