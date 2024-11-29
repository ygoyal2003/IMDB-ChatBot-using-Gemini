# IMDb ChatBot using Gemini

This project implements a Retrieval-Augmented Generation (RAG) pipeline for answering user queries about movies. It integrates a movie database with Google's PaLM API and Pinecone to retrieve relevant movie metadata and generate accurate, context-aware answers.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Workflow](#workflow)
- [Setup Instructions](#setup-instructions)
- [Contributing](#contributing)

## Overview
This chatbot leverages Retrieval-Augmented Generation to enhance question answering capabilities. It combines the power of vector databases and large language models (LLMs) to provide detailed responses about movies, including their descriptions, genres, and IMDb links.

## Features
- **Movie Database Integration**: Extracts titles, genres, descriptions, and IMDb source links from a CSV file.
- **Vector Search**: Stores high-dimensional embeddings of movie data in Pinecone for similarity-based retrieval.
- **Google PaLM LLM**: Uses Google's PaLM API for contextually relevant and meaningful text generation.
- **RAG Architecture**: Combines document retrieval with LLM generation for dynamic responses.
- **Custom Prompts**: Allows precise control over responses through tailored prompts.
- **Scalability**: Modular design supports integration with various datasets and LLMs.

## Technologies Used
- **Python**
- **SentenceTransformers** for embedding generation
- **Pinecone** for vector database storage and retrieval
- **Google Generative Language API (PaLM)** for text generation
- **Pandas** for data manipulation

## Workflow
1. **Embedding Creation**: 
   - Generate embeddings for movie data using SentenceTransformers.
2. **Vector Database Setup**: 
   - Store embeddings in Pinecone for efficient similarity-based search.
3. **Query Handling**: 
   - Retrieve relevant documents from Pinecone based on user queries.
   - Generate responses using the Google PaLM API.
4. **Output**: 
   - Provide well-structured answers along with IMDb source links.

### Workflow Diagram
1. **Load Movie Dataset**  
   ↓  
2. **Generate Embeddings** (SentenceTransformers)  
   ↓  
3. **Store Embeddings in Pinecone Index**  
   ↓  
4. **User Query**  
   ↓  
5. **Retrieve Relevant Documents** (Pinecone)  
   ↓  
6. **Answer Query** (Google PaLM API)  
   ↓  
7. **Return Answer with Source**

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- Google Cloud Platform account
- Pinecone account

### Steps
1. **Set Up Pinecone**:
   - Sign up at [Pinecone](https://www.pinecone.io) and obtain an API key.
   - Initialize Pinecone and create an index for storing embeddings.
   
2. **Enable Google PaLM API**:
   - Create a project on [Google Cloud Platform](https://console.cloud.google.com).
   - Enable the **Generative Language API**.
   - Install and configure `google-generativeai`.

3. **Install Dependencies**:
   

4. **Load Movie Dataset**:
   - Use a CSV file containing movie metadata (titles, genres, descriptions, etc.).

5. **Generate and Store Embeddings**:
   - Generate text embeddings with SentenceTransformers.
   - Store embeddings in the Pinecone index.

6. **Run the Chatbot**:
   - Process user queries, retrieve relevant movie metadata, and generate answers using Google PaLM.

## Contributing
Contributions are welcome! Please fork this repository, make changes, and submit a pull request for review.

