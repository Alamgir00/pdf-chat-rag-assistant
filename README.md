# PDF Chat Assistant – RAG Application

An AI-powered PDF question-answering application built using Retrieval-Augmented Generation (RAG).

## Overview

Upload PDF documents and ask questions about their contents. The application retrieves relevant document chunks and generates context-based answers using an LLM.

## Technology Stack

- Python 3.12
- LangChain
- OpenAI GPT-4o-mini
- Hugging Face Embeddings
- all-MiniLM-L6-v2
- ChromaDB
- Gradio
- PyPDF

## Architecture

PDF Upload → PyPDFLoader → Text Chunking → Embeddings → ChromaDB → Semantic Search → GPT-4o-mini → Gradio Chatbot

## Features

- PDF document upload
- Text extraction and chunking
- Embedding generation
- Vector database storage
- Semantic similarity search
- Context-based AI responses
- Source page references
- Interactive chatbot

## Installation

```bash
git clone https://github.com/Alamgir00/pdf-chat-rag-assistant.git
cd pdf-chat-rag-assistant

python3 -m venv venv
source venv/bin/activate

python -m pip install -r requirements.txt

cp .env.example .env
```

Add your OpenAI API key to `.env`.

## Run Application

```bash
python pdf_chat.py
```

For private local testing, use `demo.launch(share=False)`.

## Example Testing

Tested using Docker Fundamentals.pdf.

| Question | Result |
|---|---|
| What is Docker? | Answer generated |
| What is a container? | Answer generated |
| What is Kubernetes? | Not found in document |

## Learning Outcomes

- Embeddings
- Text chunking
- Vector databases
- Semantic search
- RAG architecture
- Prompt engineering
- LLM integration
- Gradio application development

## Future Enhancements

- Multiple PDF support
- Persistent vector storage
- Integrated reranking
- Chat history
- Retrieval evaluation
- Secure deployment

## Security

Never upload API keys, `.env` files, virtual environments, or confidential documents.
