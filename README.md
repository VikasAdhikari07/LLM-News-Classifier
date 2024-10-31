# Unsupervised NLP Clustering of News Queries

This project demonstrates an unsupervised NLP approach for clustering unlabeled news-related queries. Using `bert-base-uncased` model embeddings, dimensionality reduction with UMAP, and K-means clustering, this project identifies meaningful groups within a dataset of news queries. The clustering approach allows for an efficient way to categorize queries without prior labeled data, relying on manual label assignment post-clustering.

## Project Overview

Given an unlabeled dataset of news-related queries, this project aims to uncover underlying topics and themes by:
1. Extracting sentence embeddings using `bert-base-uncased` with SimpleTransformers’ `RepresentationModel`.
2. Applying UMAP for dimensionality reduction for visualization.
3. Using K-means clustering to group similar queries.
4. Determining the optimal number of clusters using the Elbow Method.
5. Assigning labels manually to the identified clusters.

## Approach

### 1. Sentence Embedding
- **Model**: `bert-base-uncased` (Google's pre-trained BERT model).
- **Tool**: `RepresentationModel` from the SimpleTransformers library.
- The model converts each query into a high-dimensional vector embedding, capturing the semantic meaning of the text.

### 2. Plotting The Sentence Vectors by Reducing with UMAP
- **UMAP (Uniform Manifold Approximation and Projection)** is applied to reduce the embeddings' dimensionality, allowing for a 2D visualization of the data.
- This visualization helps to understand the clustering behavior of queries visually, identifying patterns in the data.

### 3. K-means Clustering
- **K-means** is used for clustering the reduced embeddings into distinct groups.
- The optimal number of clusters is determined through the **Elbow Method**, ensuring that the clusters best represent the underlying topics.

### 4. Manual Label Assignment
- Each cluster is manually analyzed, and a relevant label is assigned based on the overall theme of the queries within the cluster.

## Project Files

- **README.md**: This documentation file.
- **Unlabeled_Clustering.ipynb**: Notebook for manual label assignment and detailed cluster analysis.

## Requirements

1. **Python 3.7+**
2. **Packages**:
   - `simpletransformers`
   - `transformers`
   - `umap-learn`
   - `scikit-learn`

Install the dependencies using:
```bash
pip install simpletransformers transformers umap-learn scikit-learn matplotlib
```

## Results

This project successfully clustered news queries into distinct topics, providing an interpretable structure to the dataset. UMAP and K-means proved effective for grouping similar queries, and the final manual labeling provided meaningful category names for each cluster.

### Limitations
- **Manual Labeling**: The labels are manually assigned, which may introduce subjective bias.
- **Dimensionality Reduction**: UMAP projection can sometimes lead to loss of subtle semantic differences.
- **Cluster Granularity**: The optimal number of clusters balances generality and specificity, but some topic overlap may still occur.

## Conclusion

This approach highlights the power of combining `bert-base-uncased` embeddings with clustering techniques in an unsupervised NLP task. 
