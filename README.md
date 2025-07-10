# -Build-Your-Own-Private-ChatGPT-Bot-with-PDFs--N8N


# 🧠 RAG Chatbot with Qdrant, Hugging Face & OpenAI using n8n

This project showcases how to build a local **Retrieval-Augmented Generation (RAG)** chatbot using the [n8n](https://n8n.io) automation tool, [Qdrant](https://qdrant.tech) as the vector store, [Hugging Face](https://huggingface.co) for generating embeddings, and [OpenAI](https://openai.com) for generating intelligent responses.

---

## 📌 Project Architecture

### 🔴 Data Ingestion Workflow
**Purpose**: Embed and store documents into Qdrant for later retrieval.

- **Trigger**: Form Submission (for uploading files)
- **Splitter**: `Recursive Character Text Splitter` to break documents into chunks
- **Embedding Generator**: `Hugging Face Embeddings` to create vector representations
- **Loader**: `Default Data Loader` to prepare document format
- **Vector Store**: `Qdrant Vector Store` for storing embeddings

### 🟢 RAG Chatbot Workflow
**Purpose**: Retrieve relevant information from documents and answer questions.

- **Trigger**: Chat message received
- **AI Agent**: Uses `OpenAI Chat Model` with `Simple Memory`
- **Retriever**: Qdrant fetches top similar chunks for a given query
- **Response Generator**: OpenAI model uses retrieved context to answer the user query

---

## 🚀 Getting Started

### Prerequisites

- [n8n](https://docs.n8n.io/getting-started/installation/) installed
- Qdrant (run locally via Docker or hosted)
- API Keys:
  - Hugging Face (for embeddings)
  - OpenAI (for LLM)

---

### 🔧 Setup

1. **Clone Repository**
   ```bash
   git clone https://github.com/your-username/rag-chatbot-n8n.git
   cd rag-chatbot-n8n

Configure n8n Workflows

Open n8n in browser: http://localhost:5678

Import data_ingestion.json and rag_chatbot.json from /workflows

Configure credentials:

Hugging Face API Key

OpenAI API Key

Qdrant endpoint

Test It

Upload a document via form

Send a chat message like:

"What is the refund policy in the document?"






---

## 🧩 Architecture

1. PDF → Text Splitter → Embedding → Qdrant
2. User input → Vector Search → Inject context → LLM
3. Return the Answer!

![image](https://github.com/user-attachments/assets/e86e72be-42a5-459c-a350-9d8e406cb297)



---

## 📦 Requirements

N8N 
opem api etc
