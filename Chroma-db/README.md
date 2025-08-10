# Chroma DB – Overview

**Chroma DB** is an open-source **vector database** designed for storing and retrieving **embeddings**—numerical vector representations of text, images, audio, or other data—so they can be quickly searched and matched by similarity.

## 📌 Purpose
- Commonly used in **Retrieval-Augmented Generation (RAG)** pipelines with LLMs to store document chunks as vectors and fetch the most relevant ones during queries.

## ⚙️ How It Works
1. Convert your data (e.g., text) into embeddings using a model.
2. Store these vectors in Chroma along with **metadata** (e.g., source, title).
3. Convert the query into a vector.
4. Chroma finds the most similar vectors using **vector similarity search**.
5. Retrieve the most relevant results and optionally feed them into an LLM.

## ✨ Features
- Lightweight and serverless (runs locally or embedded in apps).
- Persistent storage (saves to disk).
- Easy Python API (`pip install chromadb`).
- Supports metadata-based filtering alongside vector search.
- Integrates with **FAISS** for faster indexing.

## 🔍 Similarity Search in ChromaDB
- **Default Metric** → **Cosine Similarity**
    - Measures the angle between vectors, making it ideal for semantic similarity in embeddings.
    - Formula:  
      \[
      \text{cosine\_similarity}(A,B) = \frac{A \cdot B}{\|A\| \|B\|}
      \]
- **Why Cosine?**
    - Works well for embeddings where magnitude isn't as important as direction (meaning).
- **Other Metrics?**
    - Chroma’s default in-memory implementation uses cosine similarity.
    - When integrated with **FAISS** or other ANN backends, you can also use:
        - **L2 Distance (Euclidean distance)**
        - **Dot Product**
    - Metric choice depends on the embedding model and the application.

## 📌 Summary
ChromaDB is a **simple, developer-friendly tool** for embedding storage + similarity search, especially suited for AI applications like chatbots, semantic search, and RAG systems.