<!-- Add banner here -->
<img src="img/banner.jpg" width="70%" height="40%">

# Scalable K-means++
<!-- Add buttons here -->
![GitHub last commit](https://img.shields.io/github/last-commit/bilalsp/scalable-K-meansPP)
![GitHub pull requests](https://img.shields.io/github/issues-pr/bilalsp/scalable-K-meansPP)
![GitHub issues](https://img.shields.io/github/issues-raw/bilalsp/scalable-K-meansPP)
![GitHub stars](https://img.shields.io/github/stars/bilalsp/scalable-K-meansPP)

<!-- Describe your project in brief -->
In this project, we implement  `Scalable Kmeans++` using PySpark framework 
based on research paper `Scalable K Means++` by Bahmani et al. in 2012.

# Table of contents
- [Description](#Description)
- [Result](#Results)
- [Conclusion](#Conclusion)
- [References](#Reference)


## Description
K-means remains one of the most popular clustering algorithms. This algorithm has been used in many fields such us machine learning, pattern recognition and bioinformatics. However, the original k-means algorithm with random initialization suffers with lot of weakness. For example. A proper initialization is crucial for reciveing successful results and for large dataset, it may take long time to achive convergent.

1. <B>K-means++</B> algorithm overcomes the weekness of original kmeans by finding k better initial centers. But, it has downside due its inherent sequentical nature, which limits its efficiency ( O(n) ) and  also limits its applicability to large data sets or data with large k since the whole algorithm is not scalable.

2. <B>K-means||</B>, aka Scalable K-means++, which was proposed by Bahmani et al. in 2012, oversamples by sampling each points independently with a larger probability, which results into updating the distribution much less frequently, with efficiency ( O(log n) ), which forms k-means++ in both sequential and parallel settings.

## Results

|                       | Scalable KMeans++ | KMeans++      |  
| :-------------------: | :---------------: | :-----------: |  
| Initialization Time   | 0.01299 sec       | 0.17689 sec   |  
| Clustering Cost       | 891.761           | 1987.0044     | 
| Accuracy              | 0.9938            | 0.9628        | 

## Conclusion
In this project, we implemented `Scalable Kmeans++` algorithm using using PySpark framework 
based on research paper `Scalable K Means++` by Bahmani et al. in 2012 and we observed in an 
experiements that `Scalable K Means++` takes less time than `K Means++` to initialize the certriods of the
cluster.

## Reference
Bahman Bahmani, Benjamin Moseley, Andrea Vattani, Ravi Kumar, and Sergei Vassilvitskii. 2012. Scalable k-means++. Proc. VLDB Endow. 5, 7 (March 2012), 622–633. DOI:https://doi.org/10.14778/2180912.2180915







