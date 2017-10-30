# scalable_kmeans
An attempt to implement scalable kmeans++ algorithm
Now we're going to parallelize scalable kmeans pp on the Hadoop platform..

## Introduction:

K-means is one of the widely used data processing algorithms. However the initialization in the algorithm is crucial for obtaining a good solution. K-means++ caters to this, by obtaining an initial set of centers that is close to the optimum solution. But k-means++ is a sequential algorithm and is inefficient over large data-set, k-passes need to be made over the entire data to find a set of good initial centers. It is important to reduce the number of passes made to get good initialization. The algorithm implemented, k-means|| obtains optimal solution after a logarithmic number of passes. It is also possible to bring down the number of passes to a constant number.

## Review of literature:

K-means++ selects the first center uniformly at random from the data. Rest of the of the centers are selected with a probability proportional to their contribution to the overall error for the previous selections. The algorithm exploits the fact that a good clustering is spread out, such that while selecting a new cluster head priority is given to those nodes that are farther away from the previously selected centers. K-means++ initialization has a time complexity of O (log k) for finding the optimum solution. K-means++ is not parallelizable as selecting the ith center requires the information of previously chosen i-1 centers. So for large data-set, for which most of the processing can be done in parallel, the application needs to wait for the clustering to be completed in sequential processing. 
