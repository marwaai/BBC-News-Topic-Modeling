# 📰 BBC News Topic Modeling (LDA vs. NMF)

## 📌 Project Overview
This project focuses on **Topic Modeling** using the BBC News dataset. The goal is to automatically discover hidden themes across news articles. I implemented and compared two unsupervised learning algorithms: **Latent Dirichlet Allocation (LDA)** and **Non-Negative Matrix Factorization (NMF)**.

## 📊 Key Results
Based on the Coherence Score ($C_v$), the NMF model outperformed the LDA model:
* **NMF Coherence Score:** 0.51 (Best Performer)
* **LDA Coherence Score:** 0.44

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **NLP Libraries:** Gensim, NLTK
* **Visualization:** pyLDAvis
* **Data Handling:** Pandas, NumPy

## 💡 Technical Challenge: NMF Visualization
While using `pyLDAvis` with Gensim's NMF model, I encountered a compatibility error:  
`AttributeError: 'Nmf' object has no attribute 'inference'`

**My Solution:**
I manually prepared the data for visualization by:
1. Extracting topic-term distributions directly from the NMF model.
2. Normalizing weights into probabilities.
3. Converting sparse matrices to dense arrays for compatibility.

## 🌐 Live Interactive Dashboards
Since I enabled GitHub Pages, you can explore the topic distributions interactively:
* 🟢 [**Interactive NMF Visualization**](https://marwaai.github.io/BBC-News-Topic-Modeling/nmf_visualization_fixed%20(1).html) 
* 🔵 [**Interactive LDA Visualization**](https://marwaai.github.io/BBC-News-Topic-Modeling/lda_visualization.html)

*(Note: Replace the links above with your actual GitHub Pages URLs if they differ)*

## 📁 Repository Structure
* `topic_model.ipynb`: Full implementation from preprocessing to evaluation.
* `nmf_visualization_fixed.html`: The corrected interactive dashboard for NMF.
* `lda_visualization.html`: The interactive dashboard for LDA.
