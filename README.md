# MedQA RAG Project
This repository contains code and notebooks developed for exploring and enhancing medical question answering using Retrieval-Augmented Generation (RAG) techniques. The project leverages Llama-3 and Llama-2 models, integrates external knowledge sources (e.g., PubMed, Wikipedia), and experiments with domain-specific models to improve performance on the MedQA dataset.

## Project Overview
The goal of this project is to improve the accuracy and reliability of medical question answering systems by integrating external knowledge through RAG techniques. Key aspects of the project include context summarization, domain-specific modeling, and evaluating different retrieval strategies (e.g., full-text vs. abstract retrieval).

## File Descriptions
### Model Development and Evaluation
1. Llama3_MedQA_Classification.ipynb: Classifies medical questions in the MedQA dataset into key medical categories (e.g., cardiovascular, gastrointestinal).

2. Llama3_MedQA_Cluster.ipynb: Tests various Llama model configurations on a university computing cluster for performance optimization.

3. Llama3_MedQA_Baseline.ipynb: Establishes baseline accuracy for the MedQA dataset using Llama-3 and Llama-2 models without RAG.

4. Llama3_RAG_CS_Logit.ipynb: Calculates logit values for different RAG settings, including baseline (no RAG), PubMed, and Wikipedia data.

5. Llama3_RAG_Context_Summary_FAISS.ipynb: Implements context summarization using the FAISS index to reduce noise and improve model performance.

6. Llama3_RAG_Domain_Models.ipynb: Experiments with domain-specific models (e.g., BioBERT, PubMedBERT) for creating embeddings to improve medical question answering.

### Context Retrieval

7. Llama3_RAG_FAISS.ipynb: Implements context creation using the FAISS index with full-text PubMed articles.

8. Llama3_RAG_FAISS_Abstract.ipynb: Implements context creation using the FAISS index with abstract-only PubMed articles.

9. Llama3_RAG_Wiki_Source.ipynb: Implements the RAG pipeline using Wikipedia data indexed with FAISS.

10. Llama3_RAG_Direct_Context.ipynb: Integrates text from Wikipedia directly into the RAG pipeline as context to enhance response accuracy.

### Additional Notebooks
11. Logit_Evaluation.ipynb: Conducts experiments and analysis on logit values for each option per question, examining model confidence and performance.

12. PubMed_Data_Crawling.ipynb: Extracts relevant articles from PubMed to be used as external knowledge in the RAG pipeline.

13. Wiki_Data_Crawling.ipynb: Extracts relevant data from Wikipedia for integration into the RAG pipeline.

14. llama3-with-langchain.ipynb: An initial exploration notebook testing the baseline performance of Llama models in a Kaggle environment.

## Getting Started
To get started with the code in this repository:

#### Install Dependencies
Ensure that all required Python packages (e.g., transformers, faiss, torch, etc.) are installed. The code is there in the files, and inline instructions would help the intallations.

#### Prepare Data Sources
Download and prepare the MedQA dataset and external data sources such as PubMed and Wikipedia, which are used in the retrieval-augmented generation pipeline.

#### Run the Notebooks
Open the notebooks in a Jupyter environment and execute the cells to experiment with the models, retrieval techniques, and various configurations.

## Contributions
This project explores advanced techniques to enhance medical question answering through Retrieval-Augmented Generation. Contributions are welcome! Feel free to clone the repository, experiment with different methods, and suggest improvements.
