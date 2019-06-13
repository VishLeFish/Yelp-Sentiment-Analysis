# Yelp-Sentiment-Analysis
Sentiment Analysis on Yelp Reviews to Forecast Restaurant Closure

VIDEO: https://www.youtube.com/watch?time_continue=2&v=Lsv_7Cj42zo  

For classification with SVM, we will subset the data into bad reviews (1 star), neutral reviews (3 stars), and good reviews (5 stars). 
The first step is to clean the data by removing stop-words, punctuation, and word stems as defined by conventional NLP practices and the standard NLTK package in Python. 
We will be using a bag-of-words approach with vectorized unigrams (single words) to train our SVM model. 
After vectorizing the reviews, we obtained a sparse matrix with a shape of (5000, 14432) and density of 0.368. We split our word vectors into a training set of 80% of the data and a testing set of 20% of the data. 
After fitting the SVM algorithm on our training data and grid searching for optimal hyperparameters, we obtained impressive benchmark results when predicting restaurant closure from testing data. 
For comparison with our SVM model, we decided to train classic Naive Bayes variants used in text classification (Multinomial, Complement, Bernoulli) and obtained similar results. 
However, our SVM model outperformed these variants in accuracy and f1-score.
