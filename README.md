# PDF Chatbot using Gemini 1.5 Flash and LangChain

This repository contains a chatbot that can answer questions and summarize content from a PDF document. It uses Google's Gemini 1.5 Flash model for language generation and LangChain for text processing and chunking.

## 🧠 Project Overview

The chatbot is designed to:
- Load a PDF file and extract clean text using PyMuPDF (`fitz`)
- Split the text into smaller chunks while retaining page numbers
- Generate embeddings using Gemini's embedding model
- Store and retrieve embeddings using DocArray for fast similarity search
- Answer general questions or summarize specific pages using Gemini
- Maintain chat history for contextual responses

## ✨ Features

- 📄 Load and process unstructured PDF documents
- ✂️ Split long text into manageable chunks with page metadata
- 🔍 Semantic search using Gemini embeddings
- 🧠 Context-aware responses with chat history
- 🔐 Secure API key input using `getpass`
- 📚 Summarize specific pages or answer general questions

## ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/moni0811/Chatbot_implementation_using_RAG.git
   cd Chatbot_implementation_using_RAG
   ```
2. Install dependencies:
   ```
   pip install langchain_google_genai langchain_community langchain docarray pymupdf google.generativeai
   ```

## 🧩 Dependencies
- langchain_google_genai
- langchain_community
- langchain
- docarray
- PyMuPDF (fitz)
- google.generativeai
 - os, re, getpass

# 🚀 Usage

- Run the script:
    - Enter your Gemini API key securely when prompted.
    - Provide the path to your PDF file.
    - Start chatting! Example queries:
      - “What is the context of this PDF?”
      - “Summarize page 50”
      - “Who are the authors?”

# 📌 Notes
- The chatbot uses Gemini 1.5 Flash for both summarization and question answering.
- Chat history is included in prompts for better contextual understanding.
- Page-specific queries are handled by retaining metadata during chunking.
