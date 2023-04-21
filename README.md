# Machine-Learning-BSAN607-CA-06


Description of Dataset

The dataset is from a file called "Mall_Customers.csv" which contains information regarding CustomerID, their gender, age, annual income in U.S. Dollars, and a spending score that was calculated based on spending behavior.

Steps for Data Preprocessing, Feature Selection and scaling

First, I loaded the dataset using Pandas and checked for missing values. In this case, there were no missing values, so I didn't need to handle them. Then, I checked the distribution of features using histograms and boxplots to gain insights about the data. I then chose the appropriate features for clustering based on the task at hand. In this case, I chose 'Annual Income' and 'Spending Score' as they were the most relevant features to determine customer segments based on their spending behavior. I finally performed feature scaling using the StandardScaler from Scikit-Learn to ensure that all the features were on the same scale. Standardization is important in clustering because it helps to avoid features with larger magnitudes from dominating the clustering process. In this case, I scaled the 'Annual Income' and 'Spending Score' features.

Determining optimal number of clusters

For each number of clusters k ranging from 2 to 10, i calculated the Silhouette score using the Silhouette Coefficient function from Scikit-Learn. Then I plotted a line graph of the Silhouette scores for each number of clusters and identified the optimal number of clusters as the one with the highest average Silhouette score. In this case, the optimal number of clusters was 5. Then the model was trained using 5 clusters and from there, I was able to see the cluster assignments for each data point.

Description of Clusters and Characteristics

The visualization seemed to put all the entries into 5 clusters. Each taking up a quadrant of the graph with one of the clusters being a "goldi-locks" middleground. The x axis shows annual income while the y axis shows their spending score. From that I discerned that each cluster represented a group of wealthy people who lived frugally, wealthy people that spent a lot of money, poor people who spent a lot of money, poor people that didn't spend that much money, and middle class people who lived within their means.
