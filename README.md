# scalable_kmeans
An attempt to implement scalable kmeans++ algorithm
Now we're going to parallelize scalable kmeans pp on the Hadoop platform..

## Introduction:

K-means is one of the widely used data processing algorithms. However the initialization in the algorithm is crucial for obtaining a good solution. K-means++ caters to this, by obtaining an initial set of centers that is close to the optimum solution. But k-means++ is a sequential algorithm and is inefficient over large data-set, k-passes need to be made over the entire data to find a set of good initial centers. It is important to reduce the number of passes made to get good initialization. The algorithm implemented, k-means|| obtains optimal solution after a logarithmic number of passes. It is also possible to bring down the number of passes to a constant number.
