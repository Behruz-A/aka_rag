# RAG API

Simple, production-minded RAG service using FastAPI, Pydantic, Qdrant, and TinyLlama LLM.

## Setup
1. Create a virtual environment and install dependencies (PowerShell, from the project directory):

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

2. Configure `.env` with `QDRANT_URL`, `QDRANT_API_KEY`,
   `QDRANT_COLLECTION`, `EMBEDDING_MODEL`, `LLM_MODEL`, and
   `LLM_MAX_NEW_TOKENS`. `LLM_DEVICE` defaults to `cpu`.

3. Start the server using the same Python environment:

```powershell
.\.venv\Scripts\python.exe -m uvicorn app.main:app --reload
```

Open http://127.0.0.1:8000/docs after startup completes. On first startup,
the application downloads the embedding and language models and connects to
Qdrant, so internet access and a working Qdrant configuration are required.

