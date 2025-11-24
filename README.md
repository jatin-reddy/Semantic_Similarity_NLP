# Semantic Similarity Analysis using Sentence-BERT

This project focuses on predicting whether two sentences convey the same meaning using **semantic similarity** techniques. The dataset used is the **Quora Question Pairs dataset**, which contains sentence pairs labeled as similar or not.

## Objectives Completed
- Understand the theory behind embeddings and similarity metrics  
- Import and visualize the dataset in Google Colab  
- Generate sentence embeddings using **Sentence-BERT**  
- Measure similarity between two questions using **cosine similarity**  
- Implement **K-Means clustering from scratch** to group semantically similar questions  
- Visualize embedding clusters using **PCA**  
- Explore additional clustering – **Agglomerative Clustering**
---

## 🛠️ Tech Stack
| Component | Choice |
|----------|--------|
| Embedding Model | `sentence-transformers/all-MiniLM-L6-v2` |
| Similarity Metric | Cosine similarity |
| Clustering | K-Means (from scratch), Agglomerative Clustering |
| Visualization | PCA |

## Dataset
**Quora Question Pairs** — contains 400K+ sentence pairs aimed at detecting duplicate/similar questions.

***Dataset***: https://www.kaggle.com/datasets/quora/question-pairs-dataset

## Key Steps

### Import & Explore Dataset
Exploratory analysis included:
- Missing-value inspection
- Distribution of duplicate vs non-duplicate pairs
- Sample question pair inspection

### Generate Embeddings
Embeddings were generated in batches using: sentence-transformers/all-MiniLM-L6-v2. This model is a **bi-encoder Sentence-BERT** highly optimized for semantic similarity tasks.

### Compute Semantic Similarity
Similarity between `question1` and `question2` embeddings was computed using **cosine similarity**: cos(A, B) = (A · B) / (||A|| ||B||)

Chosen because it captures *directional semantic closeness* even when vector magnitudes differ.

### Clustering
- **K-Means implemented from scratch** → baseline clustering performance
- **Agglomerative clustering** → hierarchical grouping of semantically similar questions

### Dimensionality Reduction & Visualization
- **PCA** (2 components) used to reduce dimensionality
- Scatter plots used to visualize cluster separation

## Results & Observations
- Sentence-BERT embeddings formed meaningful clusters.
- Cosine similarity aligned well with the labeled duplicates.

