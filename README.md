# K_mean_clustering_matlab
This topic provides an introduction to k-means clustering and an example that uses the Statistics and Machine Learning Toolbox™ function kmeans to find the best clustering solution for a data set.

Introduction to k-Means Clustering
k-means clustering is a partitioning method. The function kmeans partitions data into k mutually exclusive clusters and returns the index of the cluster to which it assigns each observation. kmeans treats each observation in your data as an object that has a location in space. The function finds a partition in which objects within each cluster are as close to each other as possible, and as far from objects in other clusters as possible. You can choose a distance metric to use with kmeans based on attributes of your data. Like many clustering methods, k-means clustering requires you to specify the number of clusters k before clustering.

Unlike hierarchical clustering, k-means clustering operates on actual observations rather than the dissimilarity between every pair of observations in the data. Also, k-means clustering creates a single level of clusters, rather than a multilevel hierarchy of clusters. Therefore, k-means clustering is often more suitable than hierarchical clustering for large amounts of data.

Each cluster in a k-means partition consists of member objects and a centroid (or center). In each cluster, kmeans minimizes the sum of the distances between the centroid and all member objects of the cluster. kmeans computes centroid clusters differently for the supported distance metrics. For details, see 'Distance'.

You can control the details of the minimization using name-value pair arguments available to kmeans; for example, you can specify the initial values of the cluster centroids and the maximum number of iterations for the algorithm. By default, kmeans uses the k-means++ algorithm to initialize cluster centroids, and the squared Euclidean distance metric to determine distances.

When performing k-means clustering, follow these best practices:

Compare k-means clustering solutions for different values of k to determine an optimal number of clusters for your data.

Evaluate clustering solutions by examining silhouette plots and silhouette values. You can also use the evalclusters function to evaluate clustering solutions based on criteria such as gap values, silhouette values, Davies-Bouldin index values, and Calinski-Harabasz index values.

Replicate clustering from different randomly selected centroids and return the solution with the lowest total sum of distances among all the replicates.
