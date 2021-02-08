# Scalable K-means++

This respository has parallel implementation on "Scalable Kmeans++" using PySpark framework based on research paper "Scalable K Means++" proposed by Bahmani, Moseley, Vattani, Kumar and Vassilvitskii in 2012.

Original k-means algorithm with random initialization suffers with lot of problems. For example. A proper initialization is crucial for reciveing successful results and for large dataset, it may take long time to achive convergent.

1. <B>K-means++</B> algorithm overcomes the weekness of original kmeans by finding k better initial centers. But, it has downside due its inherent sequentical nature, which limits its efficiency ( O(n) ) and  also limits its applicability to large data sets or data with large k since the whole algorithm is not scalable.

2. <B>k-means||</B>, aka Scalable k-means++, which proposed by this paper, oversamples by sampling each points independently with a larger probability, which results into updating the distribution much less frequently, with efficiency ( O(log n) ), which forms k-means++ in both sequential and parallel settings.
