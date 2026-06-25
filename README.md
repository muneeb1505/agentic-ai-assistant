# Agentic AI Assistant with RAG & Multi-Tool Orchestration

An advanced Agentic AI Assistant built using LangGraph and LangChain that combines Retrieval-Augmented Generation (RAG), tool calling, persistent memory, and real-time utility tools into a single intelligent system.

Unlike traditional chatbots, this assistant can dynamically decide when to retrieve information from uploaded documents, perform web searches, calculate results, fetch weather data, convert currencies, retrieve stock prices, and maintain conversation context across multiple chat sessions.

---

## 🚀 Features

### 🤖 Agentic AI Workflow
- Built with LangGraph state-based orchestration
- Dynamic tool selection and execution
- Multi-step reasoning capabilities
- Tool-aware conversational flow

### 📄 Retrieval-Augmented Generation (RAG)
- Upload PDF documents directly from the UI
- Automatic document chunking and embedding
- Semantic search using FAISS
- Context-aware question answering over uploaded documents

### 🛠 Multi-Tool Orchestration

#### 🔍 Web Search
- Real-time information retrieval using DuckDuckGo

#### 🧮 Calculator
- Addition
- Subtraction
- Multiplication
- Division

#### 🌤 Weather Tool
- Current weather information for any city

#### 💱 Currency Converter
- Live currency conversion using exchange rates

#### 📈 Stock Market Tool
- Retrieve latest stock prices

#### 📚 RAG Tool
- Query uploaded PDFs using semantic search

---

## 💾 Persistent Conversation Memory

- SQLite-based checkpointing
- Thread-specific conversations
- Resume previous chats
- Persistent LangGraph state management

---

## 💬 Multi-Session Chat System

- Create multiple chat threads
- Switch between conversations
- Independent document context per chat
- Session-specific memory

---

## 🏗 Architecture

```text
User
 │
 ▼
Streamlit Frontend
 │
 ▼
LangGraph Agent
 │
 ├─────────────► Web Search
 │
 ├─────────────► Calculator
 │
 ├─────────────► Weather Tool
 │
 ├─────────────► Currency Converter
 │
 ├─────────────► Stock Price Tool
 │
 └─────────────► PDF RAG Tool
                     │
                     ▼
                 FAISS Vector Store
                     │
                     ▼
              HuggingFace Embeddings

                     ▼
             Qwen2.5-72B-Instruct
                     │
                     ▼
                Final Response
```

---

## 🛠 Tech Stack

### LLM
- Qwen2.5-72B-Instruct
- HuggingFace Inference API

### Agent Framework
- LangGraph
- LangChain

### Vector Database
- FAISS

### Embeddings
- BAAI/bge-small-en-v1.5

### Frontend
- Streamlit

### Database
- SQLite

### Document Processing
- PyPDFLoader
- RecursiveCharacterTextSplitter

### External APIs
- DuckDuckGo Search
- Alpha Vantage API
- Weather API
- ExchangeRate API

---

## 📂 Project Structure

```text
agentic-rag/
│
├── chatbot_rag_backend.py
├── chatbot_rag_frontend.py
├── chatbot.db
├── .env
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/agentic-rag.git

cd agentic-rag
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root using the provided `.env.example` template:

```env
HUGGINGFACEHUB_API_TOKEN=YOUR_HUGGINGFACE_TOKEN
ALPHA_VANTAGE_API_KEY=YOUR_ALPHA_VANTAGE_API_KEY
WEATHER_API_KEY=YOUR_WEATHER_API_KEY
EXCHANGE_RATE_API_KEY=YOUR_EXCHANGE_RATE_API_KEY
```

Alternatively, copy the example file:

```bash
cp .env.example .env
```

Then replace the placeholder values with your own API keys.
---

## ▶️ Run Application

```bash
streamlit run chatbot_rag_frontend.py
```

---

## 📖 Usage

### Upload a PDF

1. Start a new chat.
2. Upload a PDF document.
3. Wait for indexing to complete.
4. Ask questions related to the document.

### Examples

#### RAG Queries

```text
Summarize this document.

What are the key findings?

Explain chapter 3.
```

#### Web Search

```text
Search latest AI news.
```

#### Weather

```text
What is the weather in Mumbai?
```

#### Currency Conversion

```text
Convert 100 USD to INR.
```

#### Stock Market

```text
What is the current stock price of AAPL?
```

#### Calculator

```text
What is 125 * 84?
```

---

## 🔥 Key Highlights

- Agentic AI Architecture
- Retrieval-Augmented Generation (RAG)
- Multi-Tool Orchestration
- LangGraph Workflow Management
- Persistent Conversation Memory
- Multi-Session Chat Support
- FAISS Semantic Search
- Real-Time Utility Tools
- Streamlit Interface
- Open-Source LLM Integration

---

## 🎯 Learning Outcomes

This project demonstrates practical experience with:

- Agentic AI Systems
- LangGraph Workflows
- Tool Calling & Function Execution
- Retrieval-Augmented Generation (RAG)
- Vector Databases
- LLM Application Development
- Conversational Memory Management
- AI System Orchestration

---

## 🚧 Future Improvements

- Multi-PDF Retrieval
- Source Citations in Responses
- Hybrid Search (BM25 + FAISS)
- PostgreSQL Support
- User Authentication
- Conversation Export
- Multi-Agent Collaboration
- Evaluation & Monitoring Pipeline

---

## ⭐ Project Focus

This project was built to explore modern Agentic AI patterns by combining:

- Reasoning with Large Language Models
- Tool Usage
- Retrieval-Augmented Generation
- Stateful Conversations
- Workflow Orchestration

into a production-style AI assistant architecture.

---

## 👨‍💻 Author

Built as part of an AI Engineering portfolio focused on Agentic AI, RAG systems, and LLM application development.
