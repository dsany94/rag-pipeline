# rag-pipeline
Retrieval-Augmented Generation (RAG) pipeline using OpenAI Embeddings, FAISS for dense vector search, BM25 for lexical reranking, and GPT-4 for contextual answer generation. Built in Google Colab with Google Drive integration.

# 🧠 Retrieval-Augmented Generation (RAG) Pipeline

This project implements a full Retrieval-Augmented Generation (RAG) pipeline using:

- 🧬 **OpenAI Embeddings** (`text-embedding-ada-002`)
- 🔍 **FAISS** for fast vector similarity search
- 📚 **BM25** lexical reranking via `rank_bm25`
- 💬 **OpenAI GPT-4** for final answer generation
- 📁 **Google Drive** integration for document loading

---

## 📂 Project Structure

- `IDS575_Assignment2.ipynb`: Main notebook that implements the end-to-end pipeline
- `requirements.txt`: Python package dependencies (generated from Colab)
- `README.md`: Project overview and instructions

---

## 🚀 Features

- ✅ Loads `.txt` documents from Google Drive
- ✅ Splits text into manageable chunks using LangChain
- ✅ Generates OpenAI embeddings and stores them in a FAISS index
- ✅ Performs hybrid retrieval: FAISS + BM25 reranking
- ✅ Uses GPT-4 to generate responses based on top-ranked context

---

## ⚙️ How to Use

1. **Open the notebook in Google Colab**  
   [Click here to launch](https://colab.research.google.com/drive/16SVnI28BcAUTy-9uLf4PLU2jCjhuZPE-)

2. **Update the OpenAI API key** in Colab using:
   ```python
   os.environ["OPENAI_API_KEY"] = "your-api-key"

3. Mount Google Drive and make sure .txt files are placed in:
/content/drive/My Drive/Sample_Data/
