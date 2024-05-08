# Semantic Search and Clustering with NLP and M.L.

This document outlines the methods used in a project that integrates advanced Natural Language Processing (NLP) and machine learning techniques for semantic search and clustering on text data. Here, we focus on the methodologies of text embedding using Sentence Transformers, dimensionality reduction via Principal Component Analysis (PCA), and clustering using K-Means. We also explore semantic similarity search using Euclidean distance.

## Introduction

This project aims to enhance information retrieval by processing text data through semantic understanding, making it highly relevant for applications requiring content-based filtering and organization.

## Text Embedding with Sentence Transformers

### Overview
Text embedding transforms textual data into high-dimensional vectors that encapsulate semantic meanings, enabling complex NLP tasks such as semantic search.

### Application
We utilize the pre-trained model `all-mpnet-base-v2` from Sentence Transformers, which excels in converting diverse text inputs into semantic vectors.

![image](https://github.com/letalboy/PDF2Vector/assets/63066865/309f5627-a576-49b2-b6c2-9582a9405040)

## Dimensionality Reduction with PCA

### Theory
PCA tackles the challenge of high-dimensional data by reducing its dimensions, thereby simplifying computations and enabling effective data visualization.

### Implementation
We apply PCA to condense the text vectors into three principal components, maintaining the most significant variance present in the original data.

![pca](https://github.com/letalboy/PDF2Vector/assets/63066865/718315dc-03e7-4410-930e-11f78f11069f)

## Data Visualization

Using Plotly Express, we create interactive 3D scatter plots to visualize the text data in the reduced space, aiding in the understanding of document distribution and clustering.

![newplot (1)](https://github.com/letalboy/PDF2Vector/assets/63066865/79cdc017-44a4-475a-93d3-faca91744b79)

## Semantic Similarity Search

Semantic similarity search involves finding texts that are close in meaning to a given query.

### Theory of Euclidean Distance

Euclidean distance measures the straight-line distance between two points in space, used here to assess semantic closeness between the query vector and document vectors.

### Practical Application

The query text is embedded into the semantic space, and the Euclidean distance to each document vector is computed. Documents are then ranked by these distances.

![similarity_distance](https://github.com/letalboy/PDF2Vector/assets/63066865/7635aa54-742d-4b9b-b827-a40e13d20c88)

## Clustering with K-Means

K-Means clustering organizes documents into clusters based on their proximity in the reduced vector space, optimizing the homogeneity within clusters.

### Theory
K-Means minimizes variance within clusters, effectively categorizing documents into thematically coherent groups.

### Implementation
Documents are partitioned into three clusters, each represented by the nearest centroid.

## Conclusion

The combination of these advanced techniques forms a robust framework for semantic analysis, enhancing the efficiency and insightfulness of information retrieval systems. This approach is not only practical for technical applications but also provides educational value by illustrating core concepts in semantic text analysis.

---

## Requirements For Installation:

1. You probably will want to create a venv, you can do so using the following:

```shell
py -m venv .venv
```

2. Activate the env

```shell
.\.venv\Scripts\activate
```

3. Install jupter, this needs to be manually:

```shell
pip install -U jupyter notebook tqdm
```

4. Install the requirements:

```shell
pip install -r requirements.txt
```

---

Base for embeddings: https://zilliz.com/learn/all-mpnet-base-v2-enhancing-sentence-embedding-with-ai
