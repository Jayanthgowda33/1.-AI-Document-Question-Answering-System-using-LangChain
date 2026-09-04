# 📄 AI Document Q&A System

> Upload any PDF and ask questions in plain English — powered by LLMs, RAG, and semantic search.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green?style=flat&logo=fastapi)
![LangChain](https://img.shields.io/badge/LangChain-latest-orange?style=flat)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-red?style=flat&logo=streamlit)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)

---

## 🔍 What It Does

This project lets you upload a PDF document and ask natural language questions about its contents. Instead of reading through pages manually, just type your question and get an accurate, context-aware answer instantly.

**Example:**
> Upload a 50-page company policy document → Ask *"What is the leave policy for new employees?"* → Get a precise answer in seconds.

---

## ✨ Features

- 📁 **PDF Upload** — Upload any PDF document through a clean web interface
- 🧠 **Semantic Search** — Finds the most relevant sections using FAISS/ChromaDB vector search
- 💬 **Natural Language Q&A** — Ask questions in plain English, get intelligent answers
- ⚡ **Fast Inference** — Powered by Groq API for ultra-fast LLM responses
- 🔄 **RAG Pipeline** — Retrieval-Augmented Generation ensures answers are grounded in your document
- 🖥️ **Interactive UI** — Clean Streamlit frontend for easy interaction

---

## 🏗️ System Architecture

```
User Uploads PDF
      │
      ▼
 PDF Parsing & Text Chunking
      │
      ▼
 Embedding Generation
      │
      ▼
 Vector Store (FAISS / ChromaDB)
      │
  User Query
      │
      ▼
 Semantic Search → Retrieve Top Chunks
      │
      ▼
 Groq LLM API → Generate Answer
      │
      ▼
 Answer displayed in Streamlit UI
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | Python 3.10+ |
| Backend API | FastAPI |
| Frontend UI | Streamlit |
| LLM Framework | LangChain |
| Vector Database | FAISS / ChromaDB |
| LLM Provider | Groq API |
| PDF Processing | PyPDF2 / pdfplumber |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or higher
- A free [Groq API key](https://console.groq.com)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Jayanthgowda33/ai-document-qa.git
cd ai-document-qa

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set up environment variables
cp .env.example .env
# Add your Groq API key to .env file
```

### Running the App

```bash
# Start the FastAPI backend
uvicorn app.main:app --reload

# In a new terminal, start the Streamlit frontend
streamlit run frontend/app.py
```

Then open your browser at `http://localhost:8501`

---

## 📁 Project Structure

```
ai-document-qa/
├── app/
│   ├── main.py          # FastAPI app entry point
│   ├── routes/          # API route handlers
│   ├── services/        # RAG pipeline, LLM integration
│   └── utils/           # PDF parsing, chunking helpers
├── frontend/
│   └── app.py           # Streamlit UI
├── requirements.txt
├── .env.example
└── README.md
```

---

## 📸 Demo

> _Add a screenshot or screen recording of your app here_
>
> **Tip:** Use [Loom](https://loom.com) to record a quick demo and paste the link here — this impresses recruiters!

---

## 🔑 Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key_here
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repo
2. Create your branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 👤 Author

**Jayanth Gowda S K**
- 📧 gowdajayanth837@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/jayanth-gowda-b62344351)
- 🐙 [GitHub](https://github.com/Jayanthgowda33)

---

## 📄 License

This project is licensed under the MIT License.

---

⭐ **If you found this useful, please give it a star!** It helps others discover the project.
