# twitterNLP_Recommender

In this project, I use the Twitter's Python API, TweePy, in order to collected hundreds of thousands of tweets on the users I follow with the goal to develop a recommendation system based on the similarities between the content of the users I currently follow and other users I do not follow.  To do so, I use natural language processing techniques such as Latent Semantic Analysis as well as Latent Dirichlet Allocation to cluster each user's collection of tweets and recommend following a user based on their cosine similarity with cluster centroids.  

### Install

This project requires **Python** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [pyLDA](https://github.com/bmabey/pyLDAvis) 
- [plotly](https://plot.ly/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)


### Files

`Data Acqusition.ipynb` --> This notebook covers the data collecting methodology to get tweets from each follower.  Note, since there are rate-limiting constraints on accessing tweets using the Twitter API, this was done using several iterations.   

`Data_Cleaning.ipynb` --> This notebook contains the process to clean and preprocess the data.  Preprocessing stems included lemmatization, removing emojis, punctuations, and other extraneous symbols that would dirty the modeling methods. 

`Sentiment Analysis.ipynb` --> Contains some interesting sentiment analysis for all of the users that I follow using both textblob and VaderSentiment.  Interaction visualizations were done using Plotly. 

`Topic Modeling.ipynb` --> Covers the topic modeling of the content of my users' tweets using both LDA and LSA.  Unsurprisingly, popular topics included politics, data science, machine learning, and sports. 

`Clustering.ipynb` --> Train a Doc2Vec model on the corpus of the Twitter users that I follow. Compared the cosine similarity of the vectors generated by this model by a truncated SVD and got similar results. Used KMeans++ clustering projected onto two principal components to visualize the clusters. 

`tweets.csv` --> The raw tweet data. 

`cleaned_tweets.csv` --> The tweets after running `Data_Cleaning.ipynb`.

`twitter_users.csv` --> The users combined with their document of tweets. 

`tweets_with_sentiment.csv` --> The tweets combined with sentiment analysis per user. 

`user_with_sentiment.csv` --> The users combined with their document of tweets and sentiment analysis. 

`d2v.model` --> The trained doc2vec model (note that the hyperparameters extensively were not tuned). 





### Run

In a terminal or command window, navigate to the top-level project directory and run the following command:


```bash
jupyter notebook
```

This will open the Jupyter Notebook software and project file in your browser.

#### Data:

 * [twitter](twitter.com) 
 


 
 
