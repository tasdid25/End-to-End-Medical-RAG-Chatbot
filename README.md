
# MediQuery AI: Technical Overview

## Architecture
MediQuery AI implements a Retrieval-Augmented Generation (RAG) system that grounds medical responses in relevant literature through vector-based document retrieval.

## Key Features

- **RAG Architecture**: Combines retrieval and generation for factually accurate medical responses
- **HuggingFace Embeddings**: Utilizes all-MiniLM-L6-v2 for semantic document encoding
- **Pinecone Vector Database**: Enables efficient similarity search across medical literature
- **GROQ API Integration**: Leverages openai/gpt-oss-20b model for high-quality response generation
- **Medical Knowledge Base**: Incorporates specialized medical PDFs for domain-specific expertise
- **Flask Web Interface**: Provides intuitive access to AI-powered medical information

## Core Technologies

### Data Processing
- **Document Handling**: `PyPDFLoader` for PDF extraction
- **Text Processing**: Semantic chunking for optimal context retrieval

### Embedding & Retrieval
- **Vector Embeddings**: HuggingFace's `all-MiniLM-L6-v2` model (384-dimensional)
- **Vector Database**: Pinecone for scalable vector storage and similarity search
- **Retrieval Mechanism**: Cosine similarity for finding relevant medical context

### Language Model
- **LLM Integration**: GROQ API with openai/gpt-oss-20b model
- **Context Window**: Optimized prompt engineering for medical domain
- **Response Generation**: Fact-grounded answers synthesized from retrieved documents

### Application Framework
- **Web Interface**: Flask-based API and UI
- **Security**: Environment variables for API key management
- **Deployment**: Local CPU-based inference for accessibility

## Data Flow
1. **Indexing**: Medical PDFs → Text Chunks → Vector Embeddings → Pinecone
2. **Querying**: User Query → Query Embedding → Similarity Search → Context Retrieval → LLM Response

This RAG architecture ensures accurate medical information delivery while maintaining natural conversational abilities of large language models.



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


### Author
Tasdid Hasnat 
Contact: tasdidnirzor@gmail.com


