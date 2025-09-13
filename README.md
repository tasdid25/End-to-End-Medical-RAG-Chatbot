# Medical-Chatbot-Project

## Overview
A specialized medical information retrieval system using state-of-the-art large language models (LLM) and vector databases. This chatbot leverages GROQ's API to provide accurate, contextualized responses to medical queries based on a curated database of medical literature.

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
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
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





