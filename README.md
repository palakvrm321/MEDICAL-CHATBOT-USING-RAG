# MEDICAL-CHATBOT-USING-RAG  
🔹 Project Flow
Phase 1 – Setup Memory for LLM (Knowledge Base)  
Load medical PDFs (guidelines, research papers, FAQs, etc.)  
Chunk documents into smaller pieces for better retrieval.  
Generate vector embeddings using a transformer-based embedding model.  
Store embeddings in FAISS (Facebook AI Similarity Search) vector database.  

Phase 2 – Connect Memory with LLM  
Set up LLM (Mistral via HuggingFace).  
Integrate LLM with FAISS for retrieval-based QA.  
Create a RAG Chain:  
User query → FAISS (retrieves relevant chunks) → Mistral generates response using context.  

Phase 3 – User Interface
Build Chatbot UI with Streamlit.  
Load FAISS vector store in cache for fast access.  
Enable RAG-powered conversation (retrieval + generation).  

🔹 Tools & Tech Stack  
Langchain → Orchestration of RAG pipeline.  
HuggingFace → Models (Mistral + Embeddings).  
FAISS → Vector DB.  
Streamlit → Chat UI.  
Python + VS Code → Development.  

🔹Technical Architecture (Simplified Flow)  
User asks a medical question.  
Query goes to RAG pipeline.  
FAISS retrieves top-k relevant medical chunks.  
Mistral LLM uses chunks as context → generates response.  
Answer displayed in Streamlit Chat UI.  
