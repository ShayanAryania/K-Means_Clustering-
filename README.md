# K-Means_Clustering
K-means is a data clustering approach for unsupervised machine learning that can separate unlabeled data into a predetermined number of disjoint groups of equal variance – clusters – based on their similarities.

It’s a popular algorithm thanks to its ease of use and speed on large datasets. In this blog post, we look at its underlying principles, use cases, as well as benefits and limitations.

What is k-means clustering?
K-means is an iterative algorithm that splits a dataset into non-overlapping subgroups that are called clusters. The amount of clusters created is determined by the value of k – a hyperparameter that’s chosen before running the algorithm.
How does k-means clustering work?
First, the algorithm selects k initial points, where k is the value provided to the algorithm.

Each of these serves as an initial centroid for a cluster – a real or imaginary point that represents a cluster’s center. Then each other point in the dataset is assigned to the centroid that’s closest to it by distance.

After that, we recalculate the locations of the centroids. The coordinate of the centroid is the mean value of all points of the cluster. You can use different mean functions for this, but a commonly used one is the arithmetic mean (the sum of all points, divided by the number of points).

Once we have recalculated the centroid locations, we can readjust the points to the clusters based on distance to the new locations.

The recalculation of centroids is repeated until a stopping condition has been satisfied.

Some common stopping conditions for k-means clustering are:

The centroids don’t change location anymore.
The data points don’t change clusters anymore.
Finally, we can also terminate training after a set number of iterations.
How to choose the k value?
The end result of the algorithm depends on the number of сlusters (k) that’s selected before running the algorithm. However, choosing the right k can be hard, with options varying based on the dataset and the user’s desired clustering resolution.

The smaller the clusters, the more homogeneous data there is in each cluster. Increasing the k value leads to a reduced error rate in the resulting clustering. However, a big k can also lead to more calculation and model complexity. So we need to strike a balance between too many clusters and too few.

What is the difference between kNN and k-means?
Since both k-nearest neighbors (kNN) and k-means clustering use a hyperparameter called k, they can be mistaken for each other. Let’s look at the differences between these machine learning algorithms.

The main difference between the two algorithms is that k-means is a clustering algorithm, while k-nearest neighbors is a classification algorithm.

K-means is an unsupervised algorithm. It divides an unlabeled set of data into clusters based on the patterns that the data exhibits. The clusters are created by the algorithm and might not map to any “human” concepts.

In contrast, kNN is a supervised algorithm. It uses a distance function to find the closest labeled points to a given unlabeled point, the classes of which are then used to classify that point. This enables you to use a previously labeled data set to label new data points. The classes used for labeling are already predetermined: there is no way to create new ones.

The k value in k-means refers to the amount of clusters that will be created by the algorithm, while the k in kNN refers to the number of points (nearest neighbors) that will be used to classify any given point.
