Vector Embeddings & Similarity Search — Colab Notebook
A comprehensive, beginner-friendly Google Colab notebook that teaches vector embeddings from first principles and implements the same semantic search task using four different vector databases.

Notebook: Vector_Embeddings_Similarity_Search_Colab.ipynb

Overview
This project answers three core questions:

What are embeddings and why do they work?
What is a vector database and when do you need one?
How do FAISS, ChromaDB, Pinecone, and Weaviate compare in practice?
You get one clean codebase that runs end-to-end in Colab, with identical data and queries across all four tools so you can compare fairly.

What You'll Learn
Concepts

Embeddings: turning text into meaning vectors
Cosine similarity vs Euclidean distance
Exact nearest neighbor (kNN) vs Approximate Nearest Neighbor (ANN)
When to choose local vs managed vector DBs
Hands-on

Generate 384-dim embeddings with sentence-transformers/all-MiniLM-L6-v2
Build indexes, insert vectors, and run top-k similarity search
See real similarity scores for each tool
Tools Covered
1. FAISS (CPU)
Type: In-memory library by Meta
Use when: prototyping, research, billion-scale local search
Pros: fastest, zero dependencies, full control
Cons: you manage persistence and metadata
2. ChromaDB
Type: Open-source embedded database
Use when: local RAG apps, persistent storage without a server
Pros: pip install and go, automatic disk persistence
Cons: single-node only
3. Pinecone
Type: Managed cloud vector DB
Use when: production, serverless, need autoscaling
Pros: zero ops, metadata filtering, hybrid search
Cons: requires API key, usage-based pricing
4. Weaviate
Type: Open-source search engine
Use when: you need hybrid (vector + BM25 keyword) search
Pros: GraphQL API, embedded mode works in Colab
Cons: slightly steeper learning curve
Requirements
Google Colab (recommended) or Python 3.9+
No API keys needed for FAISS, ChromaDB, Weaviate embedded
Pinecone: free API key from https://app.pinecone.io (optional)
All packages are installed inside the notebook:
