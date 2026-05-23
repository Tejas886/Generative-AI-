AI-Powered RAG Chatbot using Ollama & Qdrant
A Retrieval-Augmented Generation (RAG) application built using Python, LangChain, Ollama, and Qdrant for document-based question answering.

Features
PDF document ingestion
Text preprocessing and chunking
Embedding generation using Ollama
Vector storage with Qdrant
Semantic search and retrieval
Local LLM integration for question answering
Tech Stack
Python
LangChain
Ollama
Qdrant
Docker
YAML
Project Structure
Rag/
│── ingestion.py
│── query.py
│── config.yaml
│── requirements.txt
│── utils/
│── qdrant_data/
│── hr_policy_detailed_5_pages.pdf
Installation
1. Create Virtual Environment
python -m venv .venv
2. Activate Virtual Environment
Windows
.\.venv\Scripts\activate
Linux/Mac
source .venv/bin/activate
3. Install Dependencies
pip install qdrant-client pypdf langchain langchain-community pyyaml requests
Setup Ollama
Install Ollama Model
ollama run llama3.2:3b
Pull Embedding Model
ollama pull nomic-embed-text
Start Ollama
ollama serve
Setup Qdrant using Docker
docker run -d -p 6335:6333 qdrant/qdrant

Access Qdrant Dashboard:

http://localhost:6335/dashboard
Run the Project
Ingest Documents
python ingestion.py
Query the Chatbot
python query.py
Workflow
Load PDF documents
Preprocess and split text into chunks
Generate embeddings using Ollama
Store embeddings in Qdrant
Retrieve relevant chunks during queries
Generate responses using LLM
Future Improvements
Streamlit UI integration
Multi-document support
Cloud deployment
Authentication and API support
