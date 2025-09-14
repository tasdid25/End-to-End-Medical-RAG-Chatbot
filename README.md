
# MediQuery AI: Technical Overview

## Architecture
MediQuery AI implements a Retrieval-Augmented Generation (RAG) system that grounds medical responses in relevant literature through vector-based document retrieval.

## Core Technologies

### Data Processing
- **Document Handling**: `PyPDFLoader` for PDF extraction
- **Text Processing**: Semantic chunking for optimal context retrieval

### Embedding & Retrieval
- **Vector Embeddings**: HuggingFace's `all-MiniLM-L6-v2` model (384-dimensional)
- **Vector Database**: ChromaDB for persistent storage and similarity search
- **Retrieval Mechanism**: Cosine similarity for finding relevant medical context

### Language Model
- **LLM Integration**: GROQ API with Llama-3 70B model
- **Context Window**: Optimized prompt engineering for medical domain
- **Response Generation**: Fact-grounded answers synthesized from retrieved documents

### Application Framework
- **Web Interface**: Flask-based API and UI
- **Security**: Environment variables for API key management
- **Deployment**: Local CPU-based inference for accessibility

## Data Flow
1. **Indexing**: Medical PDFs → Text Chunks → Vector Embeddings → ChromaDB
2. **Querying**: User Query → Query Embedding → Similarity Search → Context Retrieval → LLM Response

This RAG architecture ensures accurate medical information delivery while maintaining natural conversational abilities of large language models.

## Features
- **PDF Knowledge Base**: Automatically processes and indexes medical documents
- **Advanced Embeddings**: Uses HuggingFace's sentence-transformers for semantic understanding
- **RAG System**: Combines retrieval of relevant documents with generative AI for accurate and context-aware responses
- **Pinecone Vector Store**: Efficient and flexible vector database for storing and retrieving medical information
- **Conversational UI**: User-friendly interface for medical queries
- **Context-Aware Responses**: Retrieves and synthesizes information from multiple sources

## Installation

### Prerequisites
- Python 3.8+
- Anaconda or Miniconda (recommended)

# How to run?
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
GROQ_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


```bash
# run the following command to store embeddings to pinecone
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```





