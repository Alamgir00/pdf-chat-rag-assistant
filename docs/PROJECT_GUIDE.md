# Technical Project Guide

## 1. Objective

Build a PDF question-answering application using Retrieval-Augmented Generation.

## 2. Indexing Pipeline

1. PyPDFLoader extracts PDF text and page metadata.
2. RecursiveCharacterTextSplitter divides text into chunks.
3. Hugging Face all-MiniLM-L6-v2 generates embeddings.
4. ChromaDB stores document chunks and their vectors.

## 3. Retrieval and Generation

1. User submits a question.
2. ChromaDB performs similarity search.
3. Up to four relevant chunks are retrieved.
4. Retrieved content is assembled into context.
5. Page references are included.
6. GPT-4o-mini generates the response.
7. Gradio displays the answer.

## 4. Source Files

| File | Purpose |
|---|---|
| embeddings.py | Embedding generation |
| chunk.py | Text chunking |
| index.py | Vector database indexing |
| rag.py | Retrieval and generation |
| rerank.py | CrossEncoder reranking demonstration |
| pdf_chat.py | PDF chatbot application |

## 5. Security

- Store API keys in environment variables.
- Never commit `.env`.
- Exclude virtual environments and local databases.
- Avoid public sharing links for confidential documents.

## 6. Future Improvements

- Multiple PDF support
- Persistent indexing
- Retrieval reranking
- Chat history
- Authentication
- Retrieval evaluation
