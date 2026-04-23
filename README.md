# ☕️ Starbucks-NLP-Sentiment-Pipeline 
An end-to-end Natural Language Processing (NLP) pipeline analyzing thousands of Starbucks customer reviews using LDA topic modeling and an LSTM neural network  to uncover geographic business insights.

datasets:

☕️ Starbucks Reviews:
https://www.kaggle.com/datasets/harshalhonde/starbucks-reviews-dataset

🏫US Universities Dataset:
https://www.kaggle.com/datasets/rishidamarla/colleges-and-universities-in-the-us

This repository contains a complete Natural Language Processing (NLP) project built in Python. 

Impact:

📈 The goal of this project is to analyze thousands of Starbucks☕️ customer reviews📝 to determine how geographic locations (specifically college towns vs. regular locations) impact customer sentiment and operational friction.


<img width="825" height="585" alt="Regvscollegetown_starbucks_graph" src="https://github.com/user-attachments/assets/3fdb3579-c59c-478c-87de-a452bcb104dc" />


This pipeline was built in four distinct stages to clean the data, discover hidden themes, and predict future sentiment.

### 1. Unsupervised Topic Modeling (LDA)
Instead of manual tagging, we used Latent Dirichlet Allocation (via Gensim) to automatically cluster Lemmatized tokens into four distinct business themes.
<img width="924" height="459" alt="Screenshot 2026-04-22 at 9 16 54 PM" src="https://github.com/user-attachments/assets/60a255f9-2e99-4b13-97f1-9a8d5e0f609e" />

### 2. Deep Learning Sentiment Prediction (LSTM)
To predict sentiment, we translated the text into mathematical vectors using Word2Vec embeddings and fed them into a Long Short-Term Memory (LSTM) neural network.

* **Overall Accuracy:** 89.36%
* **Model Interpretability:** The model successfully learned high-weight negative signals (e.g., the word "always" appeared in 100% of negative reviews in the test set).



<img width="739" height="589" alt="Screenshot 2026-04-22 at 9 18 58 PM" src="https://github.com/user-attachments/assets/5d1d5b10-c93c-4daf-b26b-440a018ba8af" />


<img width="793" height="598" alt="Screenshot 2026-04-22 at 9 22 26 PM" src="https://github.com/user-attachments/assets/dcc744de-e1bb-412d-af61-1379452375ad" />


<img width="920" height="504" alt="Screenshot 2026-04-22 at 9 22 45 PM" src="https://github.com/user-attachments/assets/ef4ffc98-4619-4508-8022-e5e717eea32e" />


## 🎯 Conclusion: Hypothesis Validated
The initial hypothesis was **CORRECT!**. 

By enriching the raw review data with geographic university mapping, the analysis confirmed that proximity to a college campus fundamentally alters customer sentiment. College town locations exhibit tangibly lower average ratings compared to standard commuter locations. 

Furthermore, the LDA topic modeling and LSTM feature importance metrics revealed the *why*: the drop in sentiment in college towns is driven primarily by operational friction in **Customer Service and Wait Times**, rather than Product Quality. This proves that geographic demographic data can be successfully leveraged to predict specific operational bottlenecks and deploy targeted business solutions.

more info!:
🔑 Key Features of this Pipeline:

⚙️ **NLP & Text Preprocessing:** Deconstructed and "built up" the English language for machine comprehension. By utilizing Tokenization and WordNet Lemmatization, I stripped away grammatical noise and standardized the vocabulary. This was a crucial foundational step, without translating messy, raw human text into a clean, structured format, the downstream AI models would be completely unable to learn the true semantic context of the reviews.

📈 **Data Enrichment:** Pandas-driven spatial joins with US University datasets.

🦾🚀 **Unsupervised Learning:** Latent Dirichlet Allocation (LDA) via Gensim to automatically discover hidden business themes (e.g., Speed of Service, Product Quality).

🤖 **Deep Learning:** A Long Short-Term Memory (LSTM) neural network using Word2Vec embeddings to predict binary sentiment with 89% accuracy.
