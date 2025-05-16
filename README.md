# LangChain RAG Application

A simple Retrieval-Augmented Generation (RAG) application built with LangChain and Ollama that enables users to query a document collection using Llama 3.

## Overview

This command-line application lets you ask questions against a vector database of documents. The system retrieves relevant context and uses Llama 3 to generate answers based on that information.

## Features

- Local LLM inference using Llama 3 via Ollama
- Vector-based document retrieval with Chroma DB
- Interactive question-answering interface

## Prerequisites

- Ollama with Llama 3 model installed
- Python 3.8+
- Prepared Chroma database in `./chroma_db`

## Quick Start

1. Install dependencies:
   ```
   pip install langchain langchain-chroma langchain-community
   ```

2. Ensure Ollama is running with Llama 3:
   ```
   ollama pull llama3
   ```

3. Run the application:
   ```
   python rag_app.py
   ```

4. Ask questions at the prompt; type "exit" to quit

## How It Works

1. Your question triggers a search in the vector database for relevant documents
2. Retrieved documents are formatted as context
3. A RAG prompt combines your question with this context
4. Llama 3 generates an answer based on the provided information

## Customization

- Adjust retriever settings for different search behavior
- Use alternative Ollama models
- Modify the RAG prompt template

## Next Steps

- Add document ingestion capabilities
- Create a web interface
- Implement response streaming