# NotebookLM Clone

A full-stack RAG (Retrieval-Augmented Generation) application allowing users to upload documents (PDF/TXT) and converse with them in real time. It uses a modern architecture with React/Vite for the frontend, Express for the backend, and Qdrant as the vector database.

## Features
- **Dynamic File Upload & Indexing**: Upload documents which are chunked, embedded, and indexed automatically in the background.
- **Asynchronous Polling**: Scalable polling architecture to prevent browser timeouts for large documents.
- **Real-time Chat**: Ask questions directly grounded in your uploaded documents.
- **Modern UI**: Clean, responsive, and dark-themed interface built with TailwindCSS v4 and Framer Motion.
- **Markdown Support**: AI responses render with clean formatting, including code blocks and lists.

## Tech Stack
- **Frontend**: React 19, Vite 5, TailwindCSS v4, Lucide React, Framer Motion
- **Backend**: Express, Multer, LangChain
- **Vector Database**: Qdrant (Docker)
- **LLM/Embeddings**: OpenRouter API (`text-embedding-3-small`, `openai/gpt-oss-20b:free`)

## Setup Instructions

### 1. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` directory and add your OpenRouter API key:
```env
OPENROUTER_API_KEY=your_api_key_here
```

Start the Qdrant vector database using Docker:
```bash
docker compose up -d
```

Start the backend server:
```bash
node index.js
```

### 2. Frontend Setup

Open a new terminal window:
```bash
cd frontend
npm install
npm run dev
```

The frontend will run on `http://localhost:5173`. Open your browser and start asking questions!
