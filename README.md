# machine_learning_project-unsupervised-learning
## Project/Goals
The objective of the project is to utilize unsupervised learning techniques to gain insight on customer purchasing patterns utilizing the *Wholesale Data* datset.
The ultimate goal of the project is to gain insights from the data utilizing PCA, kmeans and hierarchical clustering and communicate these insights to stakeholders using appropriate visualizations and metrics to make informed decisions based on historical customer purchase data.

##Process

### 1st Step: data analysis
The first step of this project was to access and explore a dataset comprised of volume data with key metrics represented by product types. I started by analyzing the data utilizing the EDA process. I began by looking at key metrics within the descriptive statistics and checking the data frame for completion.
**Key takeaways**
- based on the pairplot data, we can see some positive correlation between:
- Grocery and detergent paper
- milk and detergent paper
- There also appears to be some sporadic outliers and significant pockets of data.
- 30,000 seems to be the upper limit for the vast majority for multiple columns within our dataset.

In order to identify and remove outliers, I set the upper limit for our dataset to 30,000 units of measurement. After assessing the mean and other statistical parameters of the dataset, I still feel as if this number is quite high. However, this number was chosen because it could be universally applied, to remove any extreme values, while maintaining some of our larger quantities, as many of our columns are exhibiting some correlations. The "Grocery" value was utilized as the main determining factor in this decision, as it had the most outliers, but still provided significant value to my analysis. 
My initial thought is that Grocery is a cumulative measurement, as it is significantly larger than other values, incorporating multiple columns. 
under normal circumstances, I would attempt to prove this by quantifying the values, but I will refrain to stay within the scope of this project.

### Step 2 : Data Preprocessing
This step involved addressing outliers and normalizing the data.

### Step 3 Training model implementation
I utilized Kmeans to segment customers into distinct groups based on purchasing patterns. After utilizing the Elbow Method to determine the optimal number of clusters, I applied KMeans clustering and assigned cluster labels to each data point. The Clusters indicated 4 distinct customer purchasing patterns which could represent different customers based on volume. 

Hierarchical clustering was used to create segmentation of customers, highlighting the hierarchical purchasing pattern in customer.
PCA was used to transform data into a lower-dimensional space while preserving the essential variance in the data. 

### Conclusion
- Kmeans seems to be the most effective at clustering
- Variables above 10k became significantly less clustered, and to fine tune the model, could be considered outliers. 
- based on the pair plot data, we can see some positive correlation between: Grocery and detergent paper, milk and detergent paper
- in regard to kmeans, anything beyond 4k provided no significant clustering, which was consistent across the dataset. 
