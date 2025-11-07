# RAG-Tutorials

# 🧠 RAG-Application

**Retrieval-Augmented Generation (RAG)** based question-answering system built as a learning and experimentation project.

This project is inspired by Krish Naik’s RAG tutorials and extended with custom improvements and structured modular design.

---

## 🚀 Overview

RAG combines two powerful ideas:
1. **Retrieval** – fetch relevant context from your knowledge base.
2. **Generation** – use an LLM to create natural, context-aware answers.

The pipeline flow:
1. Load documents and create text chunks.
2. Convert text into embeddings using `SentenceTransformers`.
3. Store vectors in a vector database (e.g. `ChromaDB`).
4. On user query, convert query → vector → find top-matching chunks.
5. Augment LLM prompt with retrieved text for grounded answers.

---

## 🧩 Tech Stack
- **Python 3.11+**
- **LangChain** – orchestration framework  
- **Sentence Transformers** – embedding model  
- **ChromaDB / FAISS** – vector database  
- **PyMuPDF / TextLoader** – document parsing  
- **OpenAI / Local LLM** – response generation  

---

## 🧠 Core Files
| File | Description |
|------|--------------|
| `src/data_loader.py` | Load and preprocess PDFs/texts |
| `src/embedding.py` | Generate sentence embeddings |
| `src/vectorstore.py` | Store and retrieve vectors |
| `src/search.py` | Query vector store and retrieve top matches |
| `app.py` | Main script for query-answer interaction |

---

## ⚙️ Setup

1. **Create virtual environment**
   ```bash
   python -m venv rag_env
   rag_env\Scripts\activate
   pip install -r requirements.txt
