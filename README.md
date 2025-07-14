# 🧠 ASKyourPDF

ASKyourPDF is an AI-powered PDF question-answering tool that uses **Retrieval-Augmented Generation (RAG)**. It allows users to upload a PDF and ask questions about its content using **Nomic embeddings** and **LLaMA 3** for local language understanding.

---

## 🚀 Features

- 📄 Upload and interact with your PDFs
- 🧠 Powered by `nomic-embed-text` for vector embeddings
- 🤖 Uses `llama3` via [Ollama](https://ollama.com) for local LLM inference
- 🔍 RAG pipeline for accurate and contextual responses
- 🖥️ Streamlit-based frontend (or easily replaceable with a custom UI)

---

## 📁 Project Structure

```
ASKyourPDF/
├── src/
│   ├── app/              # Streamlit application
│   │   ├── components/   # UI components (chat, PDF viewer, sidebar)
│   │   └── main.py       # Main app file
│   └── core/             # Core logic
│       ├── document.py   # PDF processing & chunking
│       ├── embeddings.py # Nomic embedding integration
│       ├── llm.py        # LLaMA model integration
│       └── rag.py        # RAG pipeline logic
├── data/
│   ├── pdfs/             # Uploaded PDFs
│   │   └── sample/       # Sample PDF
│   └── vectors/          # Chroma vector DB
├── tests/                # Unit tests
├── run.py                # Entry point
```

---

## 🧩 Requirements

- Python 3.9+
- [Ollama](https://ollama.com/) (for running `llama3` and `nomic-embed-text`)
- Chroma DB
- Streamlit

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/ram-rk-cmd/ASKyourPDF.git
cd ASKyourPDF
```

### 2. Set Up Python Environment

```bash
python -m venv venv
.env\Scriptsctivate  # On Windows
# Or:
# source venv/bin/activate  # On macOS/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Pull Required Ollama Models

```bash
ollama pull llama3
ollama pull nomic-embed-text
```

### 5. Run the App

```bash
python run.py
```

Then open your browser to:  
📍 `http://localhost:8501`

---

## 📦 Tech Stack

- **LLM**: LLaMA 3 via Ollama (`llama3`)
- **Embeddings**: Nomic (`nomic-embed-text`)
- **Vector DB**: Chroma
- **Frontend**: Streamlit (can be swapped with custom UI)
- **Frameworks**: Python, FastAPI (optional), LangChain-style logic

---

## 🛠️ To-Do / Enhancements

- [ ] Add support for multiple PDFs
- [ ] Add custom UI with FastAPI + React
- [ ] Enable persistent session memory
- [ ] Dockerize the project

---

## 🧪 Running Tests

```bash
pytest tests/
```

---

## 📜 License

MIT License – see `LICENSE` file for details.

---

## 🙋‍♂️ Author

Made with ❤️ by [@ram-rk-cmd](https://github.com/ram-rk-cmd)
