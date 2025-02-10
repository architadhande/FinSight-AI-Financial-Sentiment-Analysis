# FinSight-AI: Financial Sentiment Analysis

## Project Overview

FinSight-AI is a machine learning-driven text classification system designed to analyze financial news headlines and predict market sentiment. By leveraging a fine-tuned DistilBERT model, the system classifies headlines as positive or negative, providing valuable insights for investors and business professionals. The model is deployed using Google Cloud's Vertex AI for real-time analysis.

## Project Files

This repository contains the following key files:

1. **FinSight-AI Project Report**: A comprehensive document detailing the project's objectives, dataset, modeling process, deployment architecture, challenges faced, and solutions implemented.

2. **Web Scraping Script (`finsight-ai-442823-74c796148fec.json`)**: A JSON file containing configurations and credentials used for scraping financial news headlines from sources such as CNBC, The Guardian, and Reuters.

3. **GCP Implementation Notebook (`finsight-ai-implementation.ipynb`)**: A Jupyter Notebook demonstrating the implementation of the sentiment analysis model on Google Cloud Platform (GCP), including steps for data preprocessing, model training, and deployment on Vertex AI.

## Problem Statement

Financial news headlines significantly influence investor behavior and market movements. However, manually analyzing the vast amount of news data is impractical. This project aims to automate the sentiment analysis of financial news to assist in investment decision-making.

## Solution Approach

1. **Data Collection**: Scraped 32,770 financial news headlines from reputable sources, focusing on U.S. businesses and the economy between March 2018 and July 2020.

2. **Data Preprocessing**: Labeled headlines with sentiment indicators (positive = 0, negative = 1) and tokenized the text using DistilBertTokenizer, ensuring uniform input length for the model.

3. **Model Development**: Fine-tuned a DistilBERT model for binary classification, utilizing mixed-precision training on GPU to enhance performance.

4. **Deployment**: Deployed the trained model on Google Cloud's Vertex AI for scalable, real-time sentiment analysis.

## Methodology

- **Data Preprocessing**: Tokenized headlines, padded/truncated to 32 tokens, and encoded labels for model compatibility.

- **Model Training**: Employed the Adam optimizer and mixed-precision training to fine-tune the DistilBERT model, achieving a validation accuracy of 100% on the dataset.

- **Deployment Architecture**: Utilized Google Cloud Storage for data and model storage, Vertex AI for model hosting, and configured autoscaling to handle varying request volumes.

## Challenges and Solutions

- **Quota Management**: Encountered CPU quota limitations in the `us-west4` region during deployment. Addressed this by requesting quota increases, considering migration to regions with higher available quotas, and optimizing resource allocation.

## Future Work

- **Scalability Enhancements**: Plan to further optimize the deployment for efficiency and scalability, ensuring robust performance under increased load.

- **Feature Expansion**: Explore additional features such as multi-class sentiment analysis and integration with other financial data sources for comprehensive market insights.

## Acknowledgments

This project was developed by Archita Dhande.

---

*Note: For detailed information, please refer to the FinSight-AI Project Report included in this repository.*
