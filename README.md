# 📊 Financial Report Intelligence Assistant

A Retrieval-Augmented Generation (RAG) application that answers natural language questions using publicly available SEC 10-K annual reports from multiple companies.

The application retrieves relevant sections from annual reports using semantic vector search and generates responses grounded only in the retrieved document context.

---

## Features

- Retrieval-Augmented Generation (RAG)
- Multi-document semantic search
- Question answering over SEC 10-K annual reports
- Sentence Transformer embeddings
- Chroma vector database
- Local LLM inference with Ollama
- Source attribution for retrieved information

---

## Dataset

This project uses publicly available SEC Form 10-K annual reports from:

- Microsoft
- Apple
- Alphabet (Google)
- NVIDIA

The reports are used solely for educational and portfolio purposes.

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| Language | Python |
| Notebook | Jupyter Notebook |
| Document Loader | LangChain PyPDFLoader |
| Text Splitter | RecursiveCharacterTextSplitter |
| Embedding Model | all-MiniLM-L6-v2 (Sentence Transformers) |
| Vector Database | ChromaDB |
| Framework | LangChain |
| LLM Runtime | Ollama |

---

## Project Workflow

```text
SEC 10-K Reports (PDF)
        │
        ▼
PyPDFLoader
        │
        ▼
Section Detection
        │
        ▼
Recursive Character Chunking
        │
        ▼
Sentence Transformer Embeddings
        │
        ▼
Chroma Vector Database
        │
        ▼
Similarity Search
        │
        ▼
Ollama
        │
        ▼
Grounded Answer with Sources
```

---

## Repository Structure

```
.
├── Financial Report RAG.ipynb
├── 10k_Microsoft.pdf
├── 10K_Apple.pdf
├── 10K_Alphabet.pdf
├── 10K_Nvidia.pdf
└── README.md
```

---

## How It Works

1. Load multiple SEC 10-K reports using `PyPDFLoader`.
2. Detect report sections using predefined section headings.
3. Split the reports into overlapping text chunks.
4. Generate vector embeddings using Sentence Transformers.
5. Store embeddings in a Chroma vector database.
6. Retrieve the most relevant chunks based on the user's query.
7. Send the retrieved context to a local LLM running with Ollama.
8. Return an answer supported by the retrieved document sources.

---

## Example Questions

- What are Microsoft's primary business segments?
- Compare Microsoft's and Alphabet's artificial intelligence strategies.
- Summarize Apple's main risk factors.
- Which companies discuss generative AI?
- What common business risks are shared across the reports?

---

## Example Output

**Question**

> Compare Microsoft's and Alphabet's artificial intelligence strategies.

**Answer**

The assistant retrieves the most relevant sections from both annual reports and generates a response based only on the retrieved context.

**Sources**

- Microsoft | Business
- Alphabet | Business

---

## Libraries Used

- LangChain
- ChromaDB
- Sentence Transformers
- Ollama
- PyPDF
- Python

---

## Disclaimer

This project uses publicly available SEC Form 10-K annual reports obtained from company filings.

The application is intended for educational and portfolio purposes only and should not be considered financial or investment advice.
