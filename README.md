```markdown
# 📖 Context-Aware Chatbot with PDF Knowledge Base

This project is a **Context-Aware Chatbot** built as part of an internship task.  
It combines a **FastAPI backend** (for handling documents and AI models) with a **Next.js frontend** (for user interaction).  
The chatbot can read PDFs, store their embeddings in a vector database, and answer user queries using conversational context.

---

## 🚀 Features
- 📂 Upload PDFs and process them into embeddings using FAISS.
- 💬 Context-aware conversation — remembers previous user inputs during the session.
- 🤖 AI-powered answers using LLMs (Groq API + LangChain).
- 🌐 Frontend built with Next.js and React.
- ⚡ Backend built with FastAPI.
- 🔍 Retrieval-Augmented Generation (RAG) for document-based Q&A.

---

## 🏗️ Tech Stack
- **Frontend**: Next.js 13+, React, Axios, Tailwind CSS  
- **Backend**: FastAPI, LangChain, FAISS, HuggingFace Embeddings, Groq LLM  
- **Database**: FAISS vector store (local)  
- **Other Tools**: dotenv for environment variables  

---

## 📂 Project Structure
```

project-root/
│── backend/                # FastAPI backend
│   ├── main.py             # FastAPI entry point
│   ├── vectorstore/        # FAISS database storage
│   └── requirements.txt    # Backend dependencies
│
│── frontend/               # Next.js frontend
│   ├── app/                # Next.js pages/components
│   ├── components/         # Chat UI components
│   ├── package.json        # Frontend dependencies
│   └── README.md           # (this file)
│
└── .env                    # API keys and configs

````

---

## ⚙️ Setup Instructions

### 1. Clone the repository
```bash
git clone <repo-url>
cd project-root
````

---

### 2. Backend Setup (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

Create `.env` file inside `backend/`:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Run FastAPI:

```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

Backend available at: **[http://localhost:8000](http://localhost:8000)**

---

### 3. Frontend Setup (Next.js)

```bash
cd frontend
npm install
npm run dev
```

Frontend available at: **[http://localhost:3000](http://localhost:3000)**

---

## 🧑‍💻 Usage

1. Upload a PDF via the UI.
   → Backend processes and stores embeddings in FAISS.
2. Ask a question in the chat.
   → Backend retrieves relevant info and answers with context.
3. Continue asking follow-ups — chatbot remembers past questions.

---

## 📌 Internship Task Notes

* End-to-end **Context-Aware Conversational AI** system.
* Integrates **LLM + RAG + React UI**.
* Shows ability to handle **PDF ingestion, embeddings, and context-aware Q\&A**.

---

## 🔑 Environment Variables

* `GROQ_API_KEY` → Your Groq API key (required).

---

## 🚀 Future Improvements

* Multi-user sessions with persistent chat history.
* Support for DOCX/TXT uploads.
* Deployment (Vercel + Render/Heroku).