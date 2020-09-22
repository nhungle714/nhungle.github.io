---
layout: post
title: Embedding Layer
subtitle: Basic Understanding
image: /img/embedding/EmbeddingCover.svg
---

When I worked on many Natural Language Processing (NLP) projects using deep neural net models, it became a muscle memory to include an embedding layer, knowing vaguely the important role of an embedding layer. I followed this [tutorial](https://developers.google.com/machine-learning/crash-course/embeddings/programming-exercise) provided by TensorFlow team to understand what neural network embeddings are, why we want to use them, and how they are learned.

## One Hot Encoding

Deep neural network operates on numbers (e.g., float), so in traditional machinel learning model, we apply one-hot-encoding to represent categorical data as a vector of 0 and 1. 
![alt text](/img/embedding/one_hot_enc.png)

When the categories get large (e.g., 20,000), then having extra 20,000 columnes to present these 20,000 categories would result in a high number of features, potentially leading to overfitting. In addition, if we want to measure similarity between vectors using cosin distance using dot product, the one-hot-encoding vector of 0 and 1 will only give us 0 for every distance between categories. Given the challenges of one-hot-encoding, when the number of categories is large, it becomes infeasible to train a neural network using one-hot encodings. To overcome this challenge, we use embedding to obtain a low-dimension, dense vector of sparse data, in which each cell can contain any number, not just 0 or 1. 


## Embedding


**How model is learned to provide an embedding layer?**

When we train a deep neural net DNN classifier, our model learns a low-dimensional representation for the features, where the dot product defines a similarity metric tailored to the desired task. In this example, terms that are used similarly in the context of movie reviews (e.g., `"great"` and `"excellent"`) will be closer to each other the embedding space (i.e., have a large dot product), and terms that are dissimilar (e.g., `"great"` and `"bad"`) will be farther away from each other in the embedding space (i.e., have a small dot product).

When we train the model with fewer steps (e.g., 10), the model performs terribly and fails to group similar words together. As a result, we observe a sparse representation of words. 

![alt text](/img/embedding/embedding_10steps.png)

When we train the model with more steps (e.g., 10,000), the model does a good job in predicting sentiment of movie reviews with an accuracy of 0.76. Clusters of similar words partly demonstrates the model's capabillity to learn and group similar words to successfully classify sentiment of movie reviews. 

![alt text](/img/embedding/embedding_10000steps.png)

**Applications** 

In the NLP world, relationship between words (e.g., distance between words in a d-dimensional space) helps significanly when solving problems including sentiment analysis, next word prediction. The embedding layer is a weight matrix of d by n, for d being the d-dimensional space to project our words into a lower-dimensional d space, and n being the number of words (i.e., size of corpus). For example, the GloVe (Global Vectors for Word Representation) Twitter 27B provides pretrained word vectors for 2 billion tweets, 27 billion tokens from 1.2 million vocab, uncased in a weights matrix of 200 (d) x 27B (tokens). This matrix gives you the presentation of each token when projected onto a 200 dimensional space, and the sum of each row is 1. 

If we think about embedding simply as mapping discrete categorical variables to a lower-dimensional dense vector of continuous numbers, we can apply the same technique and concepts in predicting some unknown outcomes of a specific target given the outcomes of its neighbors. For example, if you like to predict Jon's rating of Game of Thrones season 8, we can look at his rating of similar series, or look at rating of Game of Thrones season 8 from other viewers similar to him. 

## Conclusion

Embedding is an intuiative and super powerful tool in the machine learning / deep learning world. I added more explanation and key takeaways [here.](https://github.com/nhungle714/Data-Science-Projects/blob/master/NLP/SentimentAnalysis/intro_to_sparse_data_and_embeddings.ipynb) 

 
Merry Christmas, everyone!

Nhung Le