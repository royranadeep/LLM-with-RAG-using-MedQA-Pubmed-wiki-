# MedQA RAG Project
This repository contains code and notebooks developed for exploring and enhancing medical question answering using Retrieval-Augmented Generation (RAG) techniques. The project leverages Llama-3 and Llama-2 models, integrates external knowledge sources (e.g., PubMed, Wikipedia), and experiments with domain-specific models to improve performance on the MedQA dataset.

## Project Overview
The goal of this project is to improve the accuracy and reliability of medical question answering systems by integrating external knowledge through RAG techniques. Key aspects of the project include context summarization, domain-specific modeling, and evaluating different retrieval strategies (e.g., full-text vs. abstract retrieval).

## File Descriptions

### 1. Llama3_MedQA_Classification.ipynb
Purpose: Classifies the medical categories of questions in the MedQA dataset.

Description: This notebook processes the MedQA dataset, categorizes the questions into various medical fields (e.g., cardiovascular, gastrointestinal), and evaluates the model's performance based on these classifications.
### 2. Llama3_MedQA_Cluster.ipynb
Purpose: Tests Llama models on a University computing cluster.

Description: This notebook runs experiments on different settings of the Llama models in a clustered environment to optimize performance and efficiency.
### 3. Llama3_MedQA_Baseline.ipynb
Purpose: Establishes baseline accuracy for the MedQA dataset using Llama-3 and Llama-2 models.

Description: This notebook calculates the initial performance of the models on the dataset without any additional data augmentation or RAG techniques.
### 4. Llama3_RAG_CS_Logit.ipynb
Purpose: Calculates logit values for different RAG settings.

Description: This file computes logit values for the baseline model (no RAG) and RAG models using PubMed and Wikipedia data, providing insight into model confidence across different retrieval contexts.
### 5. Llama3_RAG_Context_Summary_FAISS.ipynb
Purpose: Implements context summarization using the FAISS index.

Description: This notebook focuses on summarizing retrieved context to reduce noise and improve model performance. It uses the FAISS index for efficient similarity search and context integration.
### 6. Llama3_RAG_Direct_Context.ipynb
Purpose: Integrates Wikipedia text directly into the RAG pipeline as context.

Description: This file retrieves relevant text from Wikipedia and directly integrates it into the question answering pipeline, using it as context to enhance response accuracy.
### 7. Llama3_RAG_Domain_Models.ipynb
Purpose: Experiments with domain-specific models (e.g., BioBERT, PubMedBERT) for embedding creation.

Description: This notebook evaluates the impact of domain-based models on embedding quality and overall performance in medical question answering.
### 8. Llama3_RAG_FAISS.ipynb
Purpose: Implements context creation using the FAISS index with full-text PubMed articles.

Description: This file retrieves full-text articles from PubMed, indexes them with FAISS, and uses the retrieved context to improve the RAG pipeline's performance.
### 9. Llama3_RAG_FAISS_Abstract.ipynb
Purpose: Implements context creation using the FAISS index with abstract-only PubMed articles.

Description: This notebook retrieves abstract-level articles from PubMed, indexes them with FAISS, and integrates the context into the RAG pipeline.
### 10. Llama3_RAG_Wiki_Source.ipynb
Purpose: Implements the RAG pipeline using Wikipedia data with FAISS indexing.

Description: This file retrieves relevant Wikipedia passages, indexes them using FAISS, and integrates them into the question answering pipeline.
### 11. Logit_Evaluation.ipynb
Purpose: Performs experiments with logit values for each option per question.

Description: This notebook evaluates logit values to analyze model confidence and performance across different retrieval settings and question-answer pairs.
### 12. PubMed Data Crawling.ipynb
Purpose: Extracts data from PubMed.

Description: This notebook handles the web scraping and extraction of relevant PubMed articles for use in the RAG pipeline.
### 13. Wiki Data Crawling.ipynb
Purpose: Extracts data from Wikipedia.

Description: This notebook is responsible for scraping and extracting Wikipedia data, which is later indexed and used as context in the RAG pipeline.
### 14. llama3-with-langchain.ipynb
Purpose: Initial exploration of Llama models' baseline performance in a Kaggle environment.

Description: This was the first file created to test Llama model performance on the MedQA dataset using a basic setup in Kaggle before advancing to more complex RAG implementations.

## Getting Started
To get started with the code in this repository:

#### Install Dependencies
Ensure that all required Python packages (e.g., transformers, faiss, torch, etc.) are installed. The code is there in the files, and inline instructions would help the intallations.

#### Prepare Data Sources
Download and prepare the MedQA dataset and external data sources such as PubMed and Wikipedia, which are used in the retrieval-augmented generation pipeline.

#### Run the Notebooks
Open the notebooks in a Jupyter environment and execute the cells to experiment with the models, retrieval techniques, and various configurations.

## Contributions
This project explores various methods to improve medical question answering through retrieval-augmented generation, leveraging external knowledge from PubMed and Wikipedia, and experimenting with domain-specific models.
