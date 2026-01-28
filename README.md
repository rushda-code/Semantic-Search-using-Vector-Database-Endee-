#  Semantic Search using Endee Vector Database

------
-----

## Project Overview

This project implements a **semantic search system** over unstructured news articles using vector embeddings and similarity search.
The system demonstrates how modern vector databases like **Endee** can be used to store embeddings and retrieve semantically relevant documents efficiently.

The project uses the BBC News dataset and follows an end-to-end machine learning workflow including data preparation, embedding generation, and semantic retrieval.

---

## Problem Statement

Traditional keyword-based search often fails to capture the semantic meaning of user queries.
This project addresses that limitation by converting text into vector embeddings and retrieving documents based on **semantic similarity** rather than exact keyword matches.

---

## Dataset

* **BBC News Summary Dataset (Kaggle)**
* ~2,225 unstructured news articles
* Categories include: business, entertainment, politics, sport, and tech

Each article is treated as an independent document for vector indexing.

---

## System Design & Workflow

1. Load and preprocess unstructured news articles
2. Generate dense vector embeddings using a transformer-based model
3. Prepare vectors with metadata for storage in a vector database
4. Perform semantic search using cosine similarity
5. Conceptually map the workflow to Endee’s vector database operations

```
User Query
   ↓
Text Embedding
   ↓
Vector Database (Endee)
   ↓
Similarity Search
   ↓
Relevant Documents
```

---

## How Endee is Used

Endee acts as the **vector database layer** in this system.

In a production setup, Endee would:

* Store high-dimensional embeddings
* Index vectors efficiently
* Perform low-latency similarity search at scale

In this project, Endee’s behavior is **locally simulated** using cosine similarity to demonstrate how embeddings would be indexed and queried within Endee.

---

## Technologies Used

* Python
* Sentence Transformers (`all-MiniLM-L6-v2`)
* NumPy
* Pandas
* Scikit-learn
* Google Colab

---

## Setup & Execution

1. Open the Colab notebook
2. Upload the BBC News dataset ZIP file
3. Run cells sequentially from top to bottom
4. Enter a natural language query to test semantic search

---

## Example Query

```
"latest technology and software innovations"
```

### Retrieved Results

* Articles related to technology trends, digital innovation, and software developments
* Results are ranked based on semantic similarity scores

---

## Outcome

This project demonstrates a complete semantic search pipeline and mirrors how vector databases like Endee are used in real-world AI systems such as search engines, recommendation systems, and retrieval-augmented generation pipelines.

---

