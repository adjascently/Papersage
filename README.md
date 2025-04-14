# PaperSage: An LLM-Powered Research Assistant

**PaperSage** is an intelligent research assistant that helps users navigate large collections of academic research papers with ease.  
Built using a Retrieval-Augmented Generation (RAG) workflow, PaperSage combines powerful retrieval techniques and large language models to answer research queries with citations from uploaded PDFs.

---

## ✨ Features
- 📄 Upload and process full-text research papers (PDFs)
- 🔎 Semantic chunking and vector embeddings using **BAAI/bge-large-en-v1.5**
- 🗄️ Efficient retrieval from a **vector database** (via **LlamaIndex**)
- 🤖 Contextualized answer generation using **Gemma 3 LLM** (via **Ollama**)
- ✅ Lightweight answer verification module to check factual consistency
- 🖥️ Streamlit-powered user interface for interactive document querying

---

## 🚀 How It Works
1. **Document Upload**: Upload PDF papers or technical documents via the Streamlit app.
2. **Chunking & Embedding**:  
   - PDFs are split into semantic chunks (500–1,000 tokens) while preserving important metadata like titles, authors, and publication year.
   - Each chunk is embedded using a high-quality embedding model and stored in a vector database.
3. **Question Asking**:  
   - User queries are embedded and matched to the most relevant document chunks.
4. **Answer Generation**:  
   - Retrieved chunks are passed to the **Gemma 3** model to generate a contextualized, source-backed answer.
5. **Verification**:  
   - Generated answers are assessed for factual consistency against the retrieved text, and confidence scores are provided.

---

## 🗃️ Dataset
- **User-Uploaded PDFs**: Research papers, manuals, reports, etc.
- **External Data**: arXiv dataset (Machine Learning `cs.LG`, AI `cs.AI`, Computation and Language `cs.CL` categories) — 150,000+ papers.

Special handling ensures accurate parsing of:
- Mathematical notations (LaTeX)
- Figures, tables, and structured data

---

## 🛠️ Tech Stack
- **Embedding Model**: `BAAI/bge-large-en-v1.5`
- **Vector Database**: FAISS / Chroma (via LlamaIndex)
- **LLM for Answer Generation**: Gemma 3 (via Ollama server)
- **Frontend**: Streamlit
- **Backend Libraries**: PyMuPDF, LlamaIndex, Ollama, FAISS
- **Deployment**: Local / Self-hosted (Streamlit + ngrok)

---

## 📈 Current Progress
- ✅ RAG pipeline implemented
- ✅ Streamlit app with file upload and Q&A
- ✅ Prototype verification module
- 🔄 Working on improving chunking strategies and prompt engineering
- 🔄 Evaluating different embedding models for retrieval fidelity

---

## 🧠 Future Work
- Improve retrieval ranking using hybrid sparse-dense retrievers
- Enhance the verification mechanism using entailment models (e.g., DeBERTa, EntailmentGraph-BERT)
- Add support for multimodal inputs (tables, figures)
- Implement continual learning with user feedback

---

## 📚 References
- [LlamaIndex GitHub](https://github.com/jerryjliu/llama_index) — Retrieval Augmented Generation (RAG) library
- Lightning AI and Gemma 3 model documentation
- ArXiv dataset for Machine Learning and AI research papers



---

# 🧩 Contributing
Contributions, ideas, and bug reports are welcome!  
Please create an issue or open a pull request.

---

# 📜 License
This project is licensed under the MIT License.

