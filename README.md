# Starbucks-NLP-Sentiment-Pipeline
An end-to-end NLP pipeline analyzing Starbucks customer reviews using LDA topic modeling and an LSTM neural network to uncover geographic business insights.

This repository contains a complete Natural Language Processing (NLP) project built in Python. The goal of this project is to analyze thousands of Starbucks customer reviews to determine how geographic locations (specifically college towns vs. regular locations) impact customer sentiment and operational friction.

Key Features of this Pipeline:

Text Preprocessing: Tokenization and Lemmatization using WordNet.

Data Enrichment: Pandas-driven spatial joins with US University datasets.

Unsupervised Learning: Latent Dirichlet Allocation (LDA) via Gensim to automatically discover hidden business themes (e.g., Speed of Service, Product Quality).

Deep Learning: A Long Short-Term Memory (LSTM) neural network using Word2Vec embeddings to predict binary sentiment with 89% accuracy.
