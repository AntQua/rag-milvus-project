# RAG with Milvus

## Description
This project implements a Retrieval-Augmented Generation (RAG) system using Milvus as the vector database. It demonstrates the end-to-end process of:
- Setting up Milvus for storing and querying vector data.
- Preparing data for the knowledge base, including chunking and embedding.
- Populating the database with embeddings and creating efficient vector search indexes.
- Using RAG to retrieve relevant data and enhance LLM responses with contextual knowledge.

## Key Features
- Integration with Milvus for scalable vector storage and retrieval.
- Efficient query handling with semantic search.
- Examples of using OpenAI embeddings for creating and querying vector representations.
- Jupyter notebooks for easy experimentation and reproducibility.

## Technologies Used
- Python
- Milvus
- LangChain
- OpenAI API
- Docker

## Setup and Usage

### Step 1: Docker Compose Setup
The milvus-standalone-docker-compose.yml file sets up four containers:
- etcd Container: Stores metadata for Milvus.
- MinIO Container: Provides object storage for collections and indexes.
- Milvus Server: Runs as a standalone service, listening on Port 19530.
- Attu: A web-based user interface for managing and viewing Milvus.

- Start the containers using: 
  ```bash
  docker-compose -f milvus-standalone-docker-compose.yml up -d
- Verify that the containers are running:
  ```bash
  docker ps

### Step 2: Download the Project Files
- Clone this repository to your local directory:
  ```bash
  git clone https://github.com/AntQua/rag-milvus-project.git
  cd rag-milvus-project

### Step 3: Access the Attu Web UI
- Open a browser and go to: http://localhost:8000.
- Connect to the Milvus server using:
Host: localhost
Port: 19530

### Step 4: Set Up Python Environment using Anaconda
- Create a virtual environment:
  ```bash
  conda create --name Milvus python=3.11.5
  conda activate Milvus
- Install Jupyter Notebook:
  ```bash
  conda install -c conda-forge notebook

### Step 5: Start Jupyter Notebook
- Navigate to the folder containing the project files:
    ```bash
  cd /path/to/rag-milvus-project
- Start the Jupyter Notebook server:
    ```bash
    jupyter notebook
- Open the notebooks in your browser and explore the provided examples.
