# Netflix Movies and Tv Shows Clustering - ML Unsupervised
The Netflix Movies and TV Shows Clustering Project aims to cluster similar movies and TV shows available on Netflix into different clusters based on their content. The project uses unsupervised learning and Natural Language Processing (NLP) techniques to analyze the dataset, including K-Means, Hierarchical clustering, and DBSCAN algorithms.

#### <ins>Problem Statement</ins>
     This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flixable which is a third-party Netflix search engine.
     In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.
     Integrating this dataset with other external datasets such as IMDB ratings, rotten tomatoes can also provide many interesting findings.
     In this project, you are required to do :
     - Exploratory Data Analysis
     - Understanding what type content is available in different countries
     - Is Netflix has increasingly focusing on TV rather than movies in recent years.
     - Clustering similar content by matching text-based features
#### <ins>Dataset</ins>
     This dataset consists of tv shows and movies available on Netflix as of 2019.
     
     Attribute Information :
     show_id : Unique ID for every Movie / Tv Show
     type : Identifier - A Movie or TV Show
     title : Title of the Movie / Tv Show
     director : Director of the Movie / TV Show
     cast : Actors involved
     country : Country of production
     date_added : Date it was added on Netflix
     release_year : Actual Release year of the movie / TV show
     rating : TV Rating of the movie / TV show
     duration : Total Duration in minutes or number of seasons
     listed_in : Geners
     description : The Summary description
#### <ins>Data Cleaning and Data Preprocessing</ins>
     [1] Handling Duplicate Values :
     - Dataset having no duplicated values.
     [2] Handling Null / Missing Values :
     - Since there are many null values for features like director, cast, and country, those null values cannot be dropped; instead, they have been substituted with director Unavailable, Cast Unavailability, and Country Unavailable, accordingly.
     - Features such as date_added and rating have a very low number of null values, so we dropped those null values.
     [3] Handling Outliers :
     - Outliers from variable release_year are successfully treated using the interquartile range.
     [4] Feature Engineering :
     - Converted feature date_added to datetime and created new features from it, such as year_added, month_added, and day_added, before removing the feature date_added. 
     - The listed_in feature has been renamed to geners.
     - Because year cannot be a float, the feature release_year data type changed from float64 to int64.
#### <ins>Exploratory Data Analysis</ins>
     These following graphs and plots were primarily created using Matplotlib and the Seaborn package.
     - Bar plot, count plot, pair plot, dist plot, box plot, nad heatmap
     
     Performed EDA and reached the following conclusions:
     - More movies (69.14%) than TV shows (30.86%) are available on Netflix.
     - The majority of Netflix movies were released between 2015 and 2020, and the majority of - Netflix TV shows were released between 2018 and 2020.
     - The most movies and TV shows were released for public viewing on Netflix in 2017 and 2020, respectively, out of all released years.
     - From 2006 to 2019 Netflix is constantly releasing more new movies than TV shows, but in 2020, it released more TV shows than new movies, indicating that Netflix has been increasingly focusing on TV rather than movies in recent years.
     - More TV shows will be released for public viewing in 2020 and 2021 than at any other time in the history of Netflix.
     - The majority of TV shows and movies available on Netflix have a TV-MA rating, with a TV-14 rating coming in second.
     - The majority of movies added to Netflix in 2019 and the majority of TV shows added to - Netflix in 2020.
     - In 2019, Netflix added nearly one-fourth (27.71%) of all content (TV shows and movies).
     - The majority of the content added to Netflix was in October and January, respectively, but almost all months throughout the year saw Netflix adding content to its platform.
     - Netflix has more movies (69.14%) than TV shows (30.86%).
     - The majority of movies available on Netflix are produced in the United States, with India coming in second.
     - The United States and the United Kingdom are the two countries that produced the most of the TV shows that are available on Netflix.
     - Raul Campos and Jan Suter directed most of the movies available on Netflix for public viewing.
     - Alastair Fothergill directed most of the TV shows available on Netflix for public viewing.
     - International movies and the second-most popular dramas are available on Netflix as content.
     - Actors who have appeared in films and TV shows that are most available on Netflix are Lee, Michel, David, Jhon, and James.
     - We see that the movie or TV show release year and day of the month on movies or TV shows added to Netflix are slightly correlated with each other.
     - Based on the plot of release_year and year_added, we can conclude that Netflix is increasingly adding and releasing movies and TV shows over time.
     - We can conclude from plot release_year and month_added that Netflix releases movies and TV shows throughout the all months of the year.
#### <ins>Model Building</ins>
     We implemented the following unsupervised machine learning models:
     - K-Means Clustering
     - Hierarchical Clustering
     - DBSCAN Clustering
#### <ins>Models Evaluation</ins>
     - Model K-Means Clustering has a silhouette_score of 0.004634, which is close to 1 compared to models Hierarchical Clustering (-0.004158) and DBSCAN Clustering (-0.003757).
     - Model K-Means Clustering has the highest calinski_harabasz_score of 9.039247 compared to models Hierarchical Clustering (3.931202) and DBSCAN Clustering (3.003227).
     - Models Hierarchical Clustering (10.419206) and DBSCAN Clustering (1.000067) have lower davies bouldin scores than model K-Means Clustering, which has the maximum score of 11.844054.
     - Among all models, the K-Means Clustering model has the highest Calinski-Harabasz score (9.039247). Also, K-Means Clustering  model has a silhouette_score of 0.004634, which is close to 1 than other models, which means the K-Means Clustering model is capable of perfectly clustering items.
     - Due to its high Calinski-Harabasz score (9.039247) and silhouette_score (0.004634), which are close to 1, the K-Means Clustering model is the ideal model and well-trained for clustering movies and TV shows based on the content.
#### <ins>Conclusion</ins>
     - The K-Means Clustering model has the highest Calinski-Harabasz score out of all the models (9.039247). Also, the silhouette score for the K-Means Clustering model is 0.004634, which is close to one compared to other models, indicating that it can cluster Movies and TV shows perfectly based on the content.
     - The K-Means Clustering model is the optimal model and well-trained for clustering TV shows and movies based on the content due to its high Calinski-Harabasz score (9.039247) and silhouette score (0.004634), which are close to 1 than other builded models.
