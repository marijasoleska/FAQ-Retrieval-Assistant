# FAQ Retrieval Assistant

## Overview
This project implements a simple **FAQ Retrieval Assistant** that retrieves the most relevant answers from a knowledge base using **semantic similarity**.

The system supports **multilingual queries** (e.g. English and Macedonian) and returns:
- The **top 3 most relevant FAQs**
- The **best matching answer**
- A **confidence score** for each result

## Approach

1. **Data Preparation**
   - A small FAQ dataset is created with question–answer pairs.
   - Only the questions are embedded.

2. **Embedding Generation**
   - A multilingual sentence embedding model (`paraphrase-multilingual-MiniLM-L12-v2`) is used.
   - Supports 50+ languages including English and Macedonian
   - Embeddings are normalized to allow cosine similarity comparison.

3. **Query Processing**
   - The user enters a question.
   - The query is embedded using the same model.
   - Cosine similarity is calculated between the query and stored FAQ embeddings.

4. **Retrieval**
   - The top 3 most similar FAQs are retrieved.
   - The most relevant answer is returned with a confidence score.

## Tools Used

- **Python**
- **SentenceTransformers**
- **NumPy**
- **Pandas**
- **Scikit-learn**

## How to Run the Project

### 1.Install dependencies
bash
pip install sentence-transformers pandas numpy scikit-learn

### 2. Run the notebook

### 3. Enter a question

Example:
Enter your question: I forgot my password
The system will return:
### Top 3 relevant FAQs
### Confidence scores
### Best matching answer
