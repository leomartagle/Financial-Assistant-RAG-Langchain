# 📊 Financial Report Intelligence Assistant

A Retrieval-Augmented Generation (RAG) application that enables users to ask natural language questions about SEC 10-K annual reports from multiple companies.

Instead of relying on an LLM's general knowledge, the application retrieves the most relevant document sections using semantic vector search and generates answers grounded in the source documents.

---

## ✨ Features

- Multi-document Retrieval-Augmented Generation (RAG)
- Semantic search using vector embeddings
- Source-cited answers
- Cross-company comparison
- HTML document ingestion
- Metadata-aware retrieval
- Streamlit web interface
- Built with LangChain + ChromaDB

---

## Demo

### Example Questions

- What are Microsoft's primary business segments?
- Compare Microsoft's and Alphabet's AI strategies.
- What common business risks are shared across the companies?
- Which companies discuss Generative AI?
- Summarize Apple's Risk Factors section.

---

## Tech Stack

| Component | Technology |
|------------|------------|
| Language | Python |
| LLM | OpenAI GPT |
| Framework | LangChain |
| Vector Database | ChromaDB |
| Embeddings | OpenAI Embeddings |
| Frontend | Streamlit |
| Parsing | BeautifulSoup |
| Data Source | SEC 10-K HTML Reports |

---

## Project Architecture

```
SEC 10-K Reports (HTML)
            │
            ▼
HTML Parsing
            │
            ▼
Text Cleaning
            │
            ▼
Chunking
            │
            ▼
Generate Embeddings
            │
            ▼
ChromaDB Vector Store
            │
            ▼
Semantic Retrieval
            │
            ▼
OpenAI GPT
            │
            ▼
Source-Cited Response
```

---

## Example Query

**Question**

> Compare Microsoft's and Alphabet's AI strategies.

**Response**

The retrieved reports indicate that Microsoft emphasizes integrating AI across its cloud platform and productivity products, while Alphabet focuses on AI innovation through Google Search, Cloud, and Gemini models.

**Sources**

- Microsoft | Item 1. Business
- Alphabet | Item 1. Business

---

## Repository Structure

```
financial-report-intelligence-assistant/
│
├── app.py
├── requirements.txt
├── README.md
├── data/
│   ├── microsoft_2024.html
│   ├── apple_2024.html
│   ├── alphabet_2024.html
│   └── amazon_2024.html
│
├── src/
│   ├── parser.py
│   ├── chunker.py
│   ├── embeddings.py
│   ├── retriever.py
│   ├── prompt.py
│   └── utils.py
│
└── chroma_db/
```

---

## Key Features

- HTML-based document ingestion
- Metadata-aware chunking
- Cross-document retrieval
- Context-aware prompting
- Source attribution
- Vector similarity search

---

## Future Improvements

- Hybrid Search (BM25 + Vector Search)
- Reranking models
- Financial metric extraction
- Interactive charts
- Multi-year report comparison
- PDF support
- Docker deployment
- Authentication
- REST API

---

## Disclaimer

This project uses publicly available SEC 10-K annual reports for demonstration purposes.

It is intended for educational and portfolio use only and should not be considered financial or investment advice.
