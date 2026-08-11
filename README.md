# HR Assistant RAG

A retrieval-augmented generation (RAG) assistant for HR policy questions. This repository includes a sample Streamlit app and a CLI demo that use HR policy documents to answer employee questions.

## Project Structure

- `Basic-Rag/`
  - `app.py` - Streamlit chat app for the HR policy assistant.
  - `main.py` - CLI demo that runs a few sample HR questions.
  - `requirements.txt` - package dependencies for the sample app.
  - `data/hr_policy.txt` - HR policy text used by the assistant.
  - `data/faiss_index/` - prebuilt FAISS vector store files.
  - `hr_assistant/` - core assistant code, including pipeline, embeddings, vector store, logger, and tools.
  - `docs/` - project documentation and research notes.

## Features

- Build a conversational HR policy assistant
- Answer questions from a company HR policy document
- Supports both Streamlit web UI and command-line demo
- Uses LangChain-style components and vector search

## Setup

1. Create and activate a Python virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r Basic-Rag/requirements.txt
```

3. If needed, install any additional packages referenced in `Basic-Rag/requirements.txt`.

## Run the Streamlit App

```bash
cd Basic-Rag
streamlit run app.py
```

Then open the local Streamlit URL shown in the terminal.

## Run the CLI Demo

```bash
cd Basic-Rag
python main.py
```

## Notes

- The assistant code lives in `Basic-Rag/hr_assistant/`.
- The app loads the HR policy document and uses vector search to provide grounded answers.
- Use `docs/` for guides, logger setup, LangSmith notes, and prompt-injection findings.

## License

Add your license and additional project details here as needed.
