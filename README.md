# RAG Document Query System

Intelligent document retrieval system using vector embeddings and semantic search.

## 🎯 Objective
Process company documents into searchable vector embeddings for AI-powered question answering.

## 📋 Part 1: Document Ingestion Pipeline ✅

**Pipeline Steps:**
1. Load `.txt` documents from `docs/` folder
2. Split into 800-character chunks
3. Generate embeddings via OpenAI API
4. Store vectors in ChromaDB

## 🛠️ Technologies

**Libraries:**
- `langchain` - LLM application framework
- `chromadb` - Vector database
- `langchain-openai` - OpenAI embeddings integration
- `python-dotenv` - Environment management

**Embedding Model:**
- OpenAI `text-embedding-3-small` (1536 dimensions)
- Requires API key in `.env` file

**Database:**
- ChromaDB (vector storage at `db/chroma_db/`)
- HNSW indexing with cosine similarity

## 📄 Documents
5 company files: Google, Microsoft, Nvidia, SpaceX, Tesla (~2,246 chunks)

## 🚀 Quick Start
```bash
# Install dependencies
pip install -r requirements.txt

# Add API key to .env
OPENAI_API_KEY=your-key-here

# Run pipeline
python ingestion_pipeline.py
```

## 📁 Structure
```
RAG/
├── ingestion_pipeline.py    # Main script
├── .env                     # API key
├── docs/                    # Input documents
└── db/chroma_db/           # Vector database
```

## ⚙️ Config
- Chunk size: 800 chars
- Chunk overlap: 0
- Similarity: Cosine
- Encoding: UTF-8

## 🔜 Next
Query system → LLM integration → Chat interface

