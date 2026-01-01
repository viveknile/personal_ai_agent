# 🤖 AI Chatbot Agent

**LangGraph · Groq · Streamlit · FastAPI**

An **agentic AI chatbot application** built using **LangGraph ReAct agents** and **Groq LLMs**, with a **Streamlit frontend** and a **FastAPI backend**.
The chatbot supports **dynamic model selection**, **system prompts**, and **optional web search (RAG-style tool usage)**.

---

## 📌 Features

* 🧠 Agentic AI using **LangGraph (ReAct pattern)**
* ⚡ Ultra-fast inference with **Groq LLMs**
* 🌐 Optional web search using **Tavily**
* 🎛 Dynamic model & system prompt selection
* 🖥 Streamlit-based interactive UI
* 🔌 FastAPI backend (production-ready architecture)
* 🔄 Clean separation of UI, API, and agent logic

---

## 🏗️ Architecture

```
User
 │
 ▼
Streamlit Frontend (frontend.py)
 │  HTTP POST
 ▼
FastAPI Backend (backend.py)
 │
 ▼
LangGraph ReAct Agent (ai_agent.py)
 │
 ├─ Groq LLM (ChatGroq)
 └─ Tavily Search Tool (Web Search)
```

---

## 🧩 Tech Stack

### Frontend

* **Streamlit**

### Backend

* **FastAPI**
* **Uvicorn**
* **Pydantic**

### AI / Agent Layer

* **LangGraph**
* **LangChain**
* **Groq (ChatGroq)**
* **Tavily Search**

### Utilities

* **Python 3.10+**
* **Requests**
* **python-dotenv**

---

## 📂 Project Structure

```
AI-Agent-Chatbot/
│
├── frontend.py        # Streamlit UI
├── backend.py         # FastAPI server
├── ai_agent.py        # LangGraph agent logic
├── requirements.txt
├── .env               # API keys (not committed)
└── README.md
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

> ⚠️ Never commit `.env` files to GitHub.

---

## 📦 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/AI-Agent-Chatbot.git
cd AI-Agent-Chatbot
```

---

### 2️⃣ Create Virtual Environment

```bash
python -m venv aichatboat
```

Activate it:

**Windows**

```bash
aichatboat\Scripts\activate
```

**Mac / Linux**

```bash
source aichatboat/bin/activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

### ✅ Step 1: Start the Backend (FastAPI)

```bash
python backend.py
```

Expected output:

```
Uvicorn running on http://127.0.0.1:9999
```

Swagger UI:

```
http://127.0.0.1:9999/docs
```

---

### ✅ Step 2: Start the Frontend (Streamlit)

Open a **new terminal** (same virtual environment):

```bash
streamlit run frontend.py
```

The UI will open automatically in your browser.

---

## 🧪 How It Works

1. User enters a query in the Streamlit UI
2. Streamlit sends a POST request to `/chat`
3. FastAPI validates the request
4. LangGraph agent processes the query
5. Optional Tavily web search is triggered
6. Groq LLM generates the response
7. Final answer is sent back to the UI

---

## ⚠️ Common Issues & Fixes

### ❌ ConnectionError (Port 9999)

**Reason:** Backend is not running
**Fix:** Start `backend.py` before Streamlit

---

### ❌ Groq BadRequest (message content error)

**Reason:** Non-string content passed to Groq
**Fix:** Handled internally by enforcing string input

---

## 🚀 Future Enhancements

* 💬 Conversation memory (chat history)
* 🔊 Voice input / output
* 🔁 Streaming responses (token-by-token)
* 🤖 Multi-LLM support (OpenAI, Gemini)
* 🐳 Docker & cloud deployment
* 🔐 Authentication & user sessions

---

## 🧠 Key Learnings

* Demonstrates **Agentic AI** using LangGraph
* Clean separation of concerns (UI / API / AI)
* Tool calling & RAG-style search integration
* Scalable and production-friendly architecture

---

## 📄 License

This project is for **learning and demonstration purposes**.
Add a license if you plan to open-source or distribute.

---

## 👤 Author

**Vivek Nile**
---

Just tell me 👍
