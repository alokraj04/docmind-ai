# 📄 DocMind AI

<div align="center">

### Intelligent PDF Question Answering using RAG, LangChain, FAISS & OpenAI

Upload PDF documents, ask questions in natural language, and receive accurate, context-aware answers powered by Large Language Models (LLMs).

</div>

---

## 📖 About The Project

**DocMind AI** is an AI-powered document intelligence application that allows users to interact with PDF documents conversationally. Instead of manually searching through lengthy documents, users can upload a PDF and ask questions in plain English.

The application extracts text from uploaded documents, converts it into vector embeddings, stores them in a FAISS vector database, and retrieves the most relevant information using semantic similarity search. The retrieved context is then passed to an OpenAI Large Language Model to generate accurate and context-aware responses.

This project demonstrates the practical implementation of a **Retrieval-Augmented Generation (RAG)** pipeline using modern AI frameworks.

---

# ✨ Features

- 📄 Upload PDF documents
- 💬 Ask questions in natural language
- 🧠 Context-aware AI responses
- 🔍 Semantic document search
- ⚡ Fast vector similarity search using FAISS
- 🤖 Powered by OpenAI Language Models
- 🎯 Accurate answers based on uploaded documents
- 🌐 Clean and interactive Streamlit interface

---

# 🖼️ Application Preview

## Upload PDF

Upload any PDF document and begin interacting with it.

![Upload Interface](Outputs/upload-interface.png)

---

## Example 1 – Research Paper Question Answering

The application retrieves relevant information from a research paper and answers questions about the machine learning models discussed.

**Question**

> Which Machine Learning Models are used in this project?

![Research Paper Query](Outputs/research-paper-query.png)

---

## Example 2 – Spam Detection Paper

The application successfully identifies information from another research paper and generates a contextual answer.

**Question**

> Which models are used?

![Spam Detection Query](Outputs/spam-detection-query.png)

---

# 🏗️ System Architecture

```text
                  User Uploads PDF
                         │
                         ▼
                PDF Text Extraction
                     (PyPDF2)
                         │
                         ▼
                  Text Chunking
                         │
                         ▼
             OpenAI Embedding Generation
                         │
                         ▼
              Store Embeddings in FAISS
                         │
                         ▼
                 User Asks Question
                         │
                         ▼
           Convert Question to Embedding
                         │
                         ▼
          Similarity Search using FAISS
                         │
                         ▼
          Retrieve Relevant Document Chunks
                         │
                         ▼
              OpenAI Large Language Model
                         │
                         ▼
                AI Generated Response
```

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Core Programming Language |
| Streamlit | User Interface |
| LangChain | LLM Orchestration |
| OpenAI API | Large Language Model |
| FAISS | Vector Database |
| PyPDF2 | PDF Text Extraction |
| Tiktoken | Token Management |
| python-dotenv | Environment Variable Management |

---

# 📂 Project Structure

```text
DocMind-AI/
│
├── DocGenius/
│   └── PDFChat.py
│
├── Outputs/
│   ├── upload-interface.png
│   ├── research-paper-query.png
│   └── spam-detection-query.png
│
├── app.py
├── README.md
├── requirements.txt
└── .gitignore
```

---

# ⚙️ Installation

## 1. Clone the repository

```bash
git clone https://github.com/yourusername/docmind-ai.git
```

---

## 2. Navigate to the project

```bash
cd docmind-ai
```

---

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Configure Environment Variables

Create a `.env` file in the project root.

```env
OPENAI_API_KEY=your_openai_api_key
```

---

## 5. Run the application

```bash
streamlit run app.py
```

The application will launch automatically in your browser.

---

# 🚀 How It Works

1. The user uploads a PDF document.
2. The application extracts all textual content from the document.
3. The extracted text is divided into smaller chunks.
4. Each chunk is converted into vector embeddings.
5. FAISS stores these embeddings for efficient semantic retrieval.
6. When the user asks a question, the query is embedded.
7. FAISS retrieves the most relevant document chunks.
8. The retrieved context is passed to the OpenAI language model.
9. The model generates a contextual response grounded in the uploaded document.

---

# 📦 Required Libraries

- streamlit
- langchain
- faiss-cpu
- PyPDF2
- tiktoken
- python-dotenv
- openai

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

# 🔮 Future Enhancements

- Support for multiple PDF uploads
- Chat history
- Source citations with page numbers
- PDF summarization
- Multi-document comparison
- Local LLM support using Ollama
- Docker support
- Cloud deployment
- Authentication and user accounts

---


