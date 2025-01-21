Most of the traditional clustering techniques, such as k-means, hierarchical and fuzzy clustering, can be used to group data without supervision.

However, when applied to tasks with arbitrary shape clusters, or clusters within a cluster, the traditional techniques might be unable to achieve good results. That is, elements in the same cluster might not share enough similarity or the performance may be poor. Additionally, Density-based clustering locates regions of high density that are separated from one another by regions of low density. Density, in this context, is defined as the number of points within a specified radius.

In this section, the main focus will be manipulating the data and properties of DBSCAN and observing the resulting clustering.



Import the following libraries:

numpy as np
DBSCAN from sklearn.cluster
make_blobs from sklearn.datasets.samples_generator
StandardScaler from sklearn.preprocessing
matplotlib.pyplot as plt


Data generation
The function below will generate the data points and requires these inputs:

centroidLocation: Coordinates of the centroids that will generate the random data.
Example: input: [[4,3], [2,-1], [-1,4]]
numSamples: The number of data points we want generated, split over the number of centroids (# of centroids defined in centroidLocation)
Example: 1500
clusterDeviation: The standard deviation of the clusters. The larger the number, the further the spacing of the data points within the clusters.
Example: 0.5
