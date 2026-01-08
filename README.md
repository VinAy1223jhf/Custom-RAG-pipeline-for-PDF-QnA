# 📄 Document Question Answering System (My First GenAI Project)

## 👋 Introduction

This project is my **starting point in Generative AI**.  
The goal was to move beyond simply *using* tools like ChatGPT or Gemini and instead **understand how document-based question answering systems actually work internally**.

This repository contains a **basic but complete implementation of a Retrieval-Augmented Generation (RAG) pipeline** built using LangChain in a Jupyter Notebook.

---

## 🎯 Why I Built This

While tools like ChatGPT allow document uploads and Q&A, their internal logic is abstracted away.  
I wanted to learn:

- How documents are split into chunks
- How embeddings are generated
- How vector databases work
- How relevant context is retrieved
- How an LLM uses retrieved context to generate answers

This project focuses on **learning the fundamentals**, not building a polished product.

---

## 🧠 Core Idea: Retrieval-Augmented Generation (RAG)

Instead of relying only on a language model’s internal knowledge, RAG works by:

Document → Chunking → Embeddings → Vector Store → Retrieval → LLM → Answer


The model answers questions **only after retrieving relevant document context**, which helps improve accuracy and reduce hallucinations.

---

## 🛠️ Tech Stack Used

- **Python**
- **Jupyter Notebook**
- **LangChain**
- **Google Generative AI (Embeddings + LLM)**
- **FAISS** (Vector Store)
- **PyPDFLoader**

---

## 📂 What the Notebook Does

### 1. Load Documents
- Loads PDF documents using `PyPDFLoader`.

### 2. Split Text into Chunks
- Uses `RecursiveCharacterTextSplitter`.
- Chunk size and overlap are manually controlled to understand their impact.

### 3. Generate Embeddings
- Converts text chunks into vector embeddings.

### 4. Store Embeddings
- Stores vectors locally using FAISS.

### 5. Retrieve Relevant Context
- Retrieves the most relevant chunks based on the query.

### 6. Generate Answers
- Passes retrieved context to the LLM to generate answers grounded in the document.

---

## 🤔 How This Is Different from ChatGPT / Gemini Uploads

| Aspect | ChatGPT / Gemini | This Project |
|------|------------------|--------------|
| Pipeline visibility | Hidden | Fully visible |
| Control over chunking | No | Yes |
| Vector database access | No | Yes |
| Persistence | Temporary | Local & reusable |
| Learning value | Low | High |

This project helped me understand **what actually happens behind the scenes** when we upload documents to GenAI tools.

---

## 🚀 How to Run


```
pip install langchain faiss-cpu google-generativeai pypdf

1. Add your PDF file to the project directory.

2. Open the Jupyter notebook.

3. Run cells sequentially.

4. Ask questions about the document.

Example:

query = "What is the main topic discussed in the document?"
```


## 📌 Current Limitations

Single-document focused

No UI (not a chat app)

Basic prompt and retrieval logic

No source citations

These are intentional, as the project is meant for learning.

## 🔮 Future Improvements

Multi-document support

Saving & reloading FAISS index

Source-based answers

Web interface (Streamlit / FastAPI)

Experimenting with different embedding models

## 🧭 Final Note

This project represents my first hands-on step into Generative AI systems.
It prioritizes clarity and learning over abstraction and serves as a foundation for more advanced GenAI projects in the future.

👤 Author

Vinayak Garg
B.Tech (AI) | Exploring Generative AI

