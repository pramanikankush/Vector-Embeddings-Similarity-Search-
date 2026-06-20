# Vector Embeddings & Similarity Search

A comprehensive, beginner-friendly Google Colab project that teaches **Vector Embeddings**, **Semantic Search**, and **Vector Databases** from first principles.

The notebook demonstrates the same semantic search workflow across multiple vector databases, allowing direct comparison of architecture, usability, and retrieval quality.

---

## Project Goals

This project answers three important questions:

1. What are embeddings and how do they work?
2. What problem do vector databases solve?
3. How do FAISS, ChromaDB, Pinecone, and Weaviate compare in real-world RAG systems?

By the end of this notebook, you will understand how modern AI systems like ChatGPT, Perplexity, Claude, and enterprise RAG applications retrieve information using vector search.

---

## Learning Outcomes

### Vector Embeddings

- What embeddings are
- How text becomes vectors
- Semantic meaning in vector space
- Embedding dimensions
- Transformer-based embedding models

### Similarity Search

- Cosine Similarity
- Euclidean Distance (L2)
- Dot Product
- k-Nearest Neighbors (kNN)
- Approximate Nearest Neighbor (ANN)

### Vector Databases

- FAISS
- ChromaDB
- Pinecone
- Weaviate

### Retrieval Systems

- Top-K Search
- Metadata Filtering
- Semantic Search
- Retrieval-Augmented Generation (RAG)

---

## Architecture

```text
Document
    │
    ▼
Embedding Model
    │
    ▼
Vector Embedding
    │
    ▼
Vector Database
    │
    ▼
Similarity Search
    │
    ▼
Top-K Results
```

---

## Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Core Programming |
| Google Colab | Development Environment |
| Sentence Transformers | Embedding Generation |
| FAISS | Local Vector Search |
| ChromaDB | Persistent Vector Storage |
| Pinecone | Managed Cloud Vector Database |
| Weaviate | Open-Source Vector Database |
| NumPy | Numerical Operations |
| Pandas | Data Handling |

---

## Embedding Model

The notebook uses:

```python
sentence-transformers/all-MiniLM-L6-v2
```

Features:

- 384-dimensional embeddings
- Lightweight
- Fast inference
- Excellent semantic search performance
- Beginner-friendly

---

## Vector Databases Covered

### 1. FAISS

Developed by Meta AI.

**Best For**

- Research
- Prototyping
- Local semantic search
- High-speed retrieval

**Pros**

- Extremely fast
- No external service required
- GPU support
- Production proven

**Cons**

- No built-in metadata filtering
- Manual persistence management

---

### 2. ChromaDB

Open-source embedding database optimized for AI applications.

**Best For**

- Local RAG systems
- LangChain projects
- Small-to-medium datasets

**Pros**

- Simple API
- Persistent storage
- Metadata support
- Easy setup

**Cons**

- Not designed for massive scale

---

### 3. Pinecone

Managed cloud-native vector database.

**Best For**

- Production RAG
- Enterprise AI systems
- Large-scale deployments

**Pros**

- Fully managed
- Automatic scaling
- Metadata filtering
- High availability

**Cons**

- Usage-based pricing

---

### 4. Weaviate

Open-source vector database with advanced search capabilities.

**Best For**

- Enterprise search
- Hybrid retrieval
- Knowledge graphs

**Pros**

- GraphQL support
- Hybrid search
- Rich filtering

**Cons**

- More complex setup

---

## Project Workflow

```text
Text Documents
      │
      ▼
Generate Embeddings
      │
      ▼
Store Vectors
      │
      ▼
Create Index
      │
      ▼
User Query
      │
      ▼
Generate Query Embedding
      │
      ▼
Similarity Search
      │
      ▼
Top Matching Documents
```

---

## Example Query

### Query

```text
What is Retrieval Augmented Generation?
```

### Retrieved Result

```text
RAG combines retrieval systems with language models to generate grounded answers.
```

---

## Project Structure

```text
.
├── README.md
├── Vector_Embeddings_Similarity_Search_Colab.ipynb
└── assets/
```

---

## Installation

### Colab

Simply open:

```text
Vector_Embeddings_Similarity_Search_Colab.ipynb
```

and run all cells.

### Local Environment

```bash
pip install sentence-transformers
pip install faiss-cpu
pip install chromadb
pip install pinecone
pip install weaviate-client
pip install pandas
pip install numpy
```

---

## Example Code

### Generate Embeddings

```python
from sentence_transformers import SentenceTransformer

model = SentenceTransformer(
    "sentence-transformers/all-MiniLM-L6-v2"
)

embedding = model.encode(
    "What is machine learning?"
)

print(embedding.shape)
```

Output:

```text
(384,)
```

---

## Similarity Search Example

```python
query = "Explain machine learning"

results = vector_db.search(
    query,
    top_k=3
)
```

---

## Use Cases

### AI Chatbots

Retrieve relevant context before generation.

### Enterprise Search

Search internal documents semantically.

### Recommendation Systems

Find similar products, articles, or users.

### Knowledge Bases

Power intelligent document assistants.

### Retrieval-Augmented Generation (RAG)

Provide grounded context to LLMs.

---

## Who Should Use This Project?

- Data Science Students
- AI Engineers
- ML Engineers
- RAG Developers
- LangChain Learners
- GenAI Enthusiasts

---

## Key Concepts Covered

- Embeddings
- Semantic Search
- Vector Similarity
- Cosine Similarity
- Euclidean Distance
- Dot Product
- kNN Search
- ANN Search
- Vector Indexing
- Retrieval Systems
- Vector Databases
- RAG Fundamentals

---

## Future Improvements

- Hybrid Search
- Metadata Filtering
- Reranking
- Qdrant Integration
- Milvus Integration
- LangChain Pipelines
- Production RAG Architecture
- Agentic Retrieval Systems

---

## References

- FAISS Documentation
- ChromaDB Documentation
- Pinecone Documentation
- Weaviate Documentation
- Sentence Transformers Documentation

---

## License

MIT License

---

## Author

**Ankush**
Data Science | Agentic AI | RAG Engineering | Generative AI
