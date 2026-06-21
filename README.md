# Multi-Agent Agentic RAG (CrewAI)

This project implements an Agentic Retrieval-Augmented Generation (RAG) workflow with **multiple role-based agents**:

- **Router Agent**: classifies each question into either `pdf` or `web` retrieval path
- **Retriever Agent**: executes the selected retrieval tool and returns a source-grounded answer

The system supports:
- PDF vector retrieval with FAISS
- Web retrieval with Tavily
- Step-level orchestration tracing and runtime visualization

## Project Files

- `multi_agent_rag_notebook.ipynb`: Jupyter notebook deliverable with full implementation and trace visualization
- `requirements.txt`: dependencies

## Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Configure the `.env` file in the project root (already created with defaults):

```env
# LLM credentials (use Azure OR OpenAI)
AZURE_OPENAI_API_KEY=
AZURE_OPENAI_ENDPOINT=https://openai-api-management-gw.azure-api.net
OPENAI_API_KEY=

# Web retrieval
TAVILY_API_KEY=
```

You can also adjust model defaults in `.env` (`AZURE_CHAT_MODEL`, `OPENAI_MODEL`, `AZURE_EMBEDDING_DEPLOYMENT`, etc.).

## Run Notebook

Open `multi_agent_rag_notebook.ipynb` and run cells in order.

The notebook includes:
- role definitions
- routing logic
- retrieval tool execution
- final answer generation with sources
- reasoning trace table and visualization
