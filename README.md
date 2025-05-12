# Customer-Segmentation-using-clustering
Academic project
## 1.  Introduction: 
### 1.1 Clustering: 
• In the previous assignment we have implemented machine learning classification models like decision 
trees and support vector machines. These classification models are called supervised learning models 
cause the data that we have used in developing these models is labelled. 
• Unlike decision trees and SVMs, clustering models are unsupervised learning algorithms cause the 
data used with these models is not labelled, means the data is not segregated into different classes. 
• Clustering analysis is an unsupervised technique in data mining which is performed to organize a set 
of data points into groups or clusters based on the similarities. The points from the same cluster are 
more similar to each other compared to the points from a different cluster. 
### 1.2 Significance of clustering: 
• Clustering helps us to identify and group similar patterns of data which allows businesses to understand 
the customers more clearly. This will help in identifying groups with similar interests or preferences 
such that businesses can focus on them. 
• Business can target customers of same tastes or purchasing patterns with better marketing strategies. 
### 1.3 Steps involved in clustering analysis: 
• After assigning the points to the initial centroids we will caluculate the new centroids by taking 
the mean of all the data points assigned to each cluster based on the initial centroids. 
• Model selection: Selecting an appropriate clustering model is very important and depends upon 
several factors such as the characteristics of the dataset like size, cluster shape, and density etc. 
• Data preparation: After selecting an appropriate model for our use case we need to prepare our data 
for clustering. Data preparation involves cleaning the data, filling missing values, normalising etc. 
Clustering algorithms like K-means are sensitive to the scale of measurement and outliers. If the 
features are measured on different scales, they should be scaled to a similar range using StandardScalar.  
• Clustering: In this step we will apply the selected clustering model on the processed dataset to group 
the data points into clusters based on the similarities. Different algorithms perform clustering in a 
different way, and each has its own pros and cons. 
• Evaluation: After the clustering is done, we access the performance and efficiency of the algorithm is 
assessed by using metrics like Silhouette Score, Within-Cluster Sum of Squares (WCSS), 
Dendrograms and cluster size distribution. 
### 1.4 Different types of clustering algorithms implemented: 
#### 1. K – means Clustering: 
• K-means clustering is a widely used partitioning type clustering algorithm. In this algorithm 
the data points are partitioned into a defined number (K) of clusters each cluster is represented 
by a centroid. 
• So first we will randomly select k initial centroids from the dataset. Instead of selecting these 
centroids randomly we can also use methds like k-means++ for better starting points. 
• Then in the next step we will assign each data point from the dataset to the nearest centroid 
based up on the distance between them. 
• Then we will reassign the points in the dataset to the new centroids. 
• We will repeat thes setps till the centoids won’t change or the datapoints stops changing from 
one cluster to another. 
• Evaluation metrix such as Within-cluster sum of squares WCSS are used to assess the clustering 
algorithm performance. It measures the sum of squared distances between data points and their 
centroids, and we need to minimise it. 
#### 2. Hierarchical Clustering: 
• Hierarchical clustering produces a set of nested clusters organised as a hierarchical tree called 
dendrograms. 
• Dendrograms are a tree like structures that records the sequences of merges or splits. 
• There are 2 types of hierarchical clustering’s they are: 
o Agglomerative: It is like a bottom-up approach. In this type of clustering we start with 
each data point as a separate cluster and will merges the closest cluster iteratively until 
we are left with only one cluster. 
o Divisive: it is like a Top-Down approach. In this clustering algorithm we start with one 
large cluster containing all the data points and will splits the clusters iteratively until 
each point becomes a separate cluster. 
o We use  linkage methods like Max, Min, average and ward’s method for determining 
the distance between clusters. This distance decides which clusters to be combined in 
each iteration. 
#### 3. Density based Clustering (DBSCAN): 
1. Fresh: Annual spending on fresh produce. (Continuous) 
2. Milk: Annual spending on dairy based products. (Continuous) 
• Density based clustering algorithms group the data points based on density. These are very 
useful for identifying clusters of different shapes and sizes and also handles noise effectively. 
• In density-based clustering we will define parameters like Epsilon and MinPts for determining 
the radius or neighbourhood distance around a data point and the minimum number of points 
required to form a cluster or dense region 
• After defining the epsilon and MinPts we will identify the core, border and noise points to form 
dense regions 
• Core points are the once that are inside the defined radius epsilon and should have neighbours. 
• Border points are the points which don’t have any neighbours but are within the distance of a 
core points. 
• Noise points are described as the points which are neither core nor border points. 
• Density clustering algorithms like DBSCAN starts with a point and if it is considered as acore 
point it forms a new cluster and then expands to include all the other core and border points. 
• The cluster continues to grow as long as the algorithm can find new core points.
