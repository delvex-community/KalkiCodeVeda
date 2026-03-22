# Course Table of Contents: LLM + RAG with OSS & Azure Implementations

## Part 1: Core Concepts (3–4 Hours)

### Introduction to LLMs & RAG

- **Understanding LLMs:**  
    - Tokens, context, hallucination

- **Need for RAG:**  
    - Grounding, domain specificity, trust

- **RAG Pipeline Breakdown:**  
    - Document ingestion & preprocessing  
    - Chunking strategies & embeddings  
    - Retrieval → Vector search → Answer generation

### Open-Source Vector Databases – Selection Guide

| Database   | Description | References |
|------------|-------------|------------|
| **FAISS**  | Local, high-performance, GPU-ready similarity search library | [Wikipedia](https://en.wikipedia.org/wiki/FAISS) |
| **Chroma** | Lightweight, developer-friendly starter DB | [DataCamp](https://www.datacamp.com/tutorial/chroma-vector-database) |
| **Qdrant** | Rust-based, API service, filters, real-time updates | [AIMultiple](https://www.aimultiple.com/qdrant/), [DataCamp](https://www.datacamp.com/tutorial/qdrant-vector-database) |
| **Weaviate** | Cloud-native, modular, hybrid search integration | [AIMultiple](https://www.aimultiple.com/weaviate/), [DataCamp](https://www.datacamp.com/tutorial/weaviate-vector-database) |
| **Milvus** | Distributed, scalable, production-grade | [Wikipedia](https://en.wikipedia.org/wiki/Milvus) |
| **pgvector (Postgres)** | Relational + vector search in one | [AIMultiple](https://www.aimultiple.com/pgvector/) |

**When to Choose What:**
- FAISS: Fast local prototyping, GPU acceleration, maximum control
- Qdrant/Weaviate/Milvus: Managed or cluster deployments with filtering and scale
- pgvector: Simplicity and unified storage alongside relational data

### Azure Vector Search Fundamentals

- **Azure AI Search:**  
    - Vector indexing, hybrid (vector + keyword), filtering, multimodal support  
    - [Microsoft Learn](https://learn.microsoft.com/en-us/azure/search/vector-search-overview), [Azure Docs](https://learn.microsoft.com/en-us/azure/search/)  
- **Enterprise Features:**  
    - Relevance tuning, security, integration with Azure ecosystem  
    - [Microsoft Learn](https://learn.microsoft.com/en-us/azure/search/security-overview)

---

## Part 2: Business Use Case Implementations

Each module provides OSS + Azure paths, with both code and low/no-code options.

### Use Case 1: Customer Support Chatbot (FAQ & Policy Queries)
- **OSS Path:** LangChain or LlamaIndex + FAISS (quick setup)
- **Azure Path:** Azure OpenAI + Azure AI Search in AI Studio

### Use Case 2: Enterprise Knowledge Assistant (HR/Policy Data)
- **OSS:** LlamaIndex + FAISS, optionally scale to Qdrant or Milvus
- **Azure:** Blob Storage + Azure AI Search + Azure OpenAI

### Use Case 3: Financial Research Bot (Earnings Reports & Filings)
- **OSS:** Haystack + Qdrant/Milvus for filtering and scale
- **Azure:** Azure AI Search (hybrid search) + Azure OpenAI

### Use Case 4: Legal Document Analyzer (Clause Comparison)
- **OSS:** LangChain + FAISS for precise control, or Weaviate for hybrid filtering
- **Azure:** AI Studio RAG pipelines with Azure AI Search

### Use Case 5: E-commerce Product Q&A Tool
- **OSS (No-Code):** FlowiseAI + FAISS/Chroma → upgrade to Qdrant as needed
- **Azure (Low-Code):** Azure AI Studio with built-in AI Search vector index

---

## Part 3: Productionizing RAG Systems (Optional Advanced Add-on)

- Monitoring retrieval accuracy (e.g., LangSmith or custom evals)
- Safety & guardrails (moderation, prompt injection, fallback strategies)
- Cost optimizations (caching, batch queries, hybrid search)
- Architecture scaling (Docker/K8s, multi-region deployment)

---

## Summary Table

| Part      | Focus Area      | OSS Tools (emphasis)                              | Azure Tools                          |
|-----------|----------------|---------------------------------------------------|--------------------------------------|
| Part 1    | Concepts        | FAISS, Chroma, Qdrant, Weaviate, Milvus, pgvector | Azure AI Search hybrid indexing      |
| Use Cases | 5 Scenarios     | LangChain/LlamaIndex/Haystack + vectorDB          | Azure OpenAI + AI Search (in Studio) |
| Optional  | Production      | Monitoring, safety, scaling frameworks            | Secure Azure deployment patterns     |