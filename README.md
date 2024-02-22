# NLP Predictions of User Ratings

The Data for this Hobby-Project contains product reviews and a rating for each product. A product can be rated from one to five. The dataset contains 10K samples. I analyze the dataset and build a model that is able to predict from a given review its score. 

It has been found that the most frequent words in all categories are the same except in the case of category 5, where the words great and love appear frequently. Therefore, it has been decided not to use mod-els that model the reviews as unrelated sets of words (BOG, TF-IDF). In these models, the similarity between the reviews would be calculated by means of the distance (for example, Euclidean distance) between the vectors in each review. From there it could be clustered into 5 different classes, for example with K-Means. Another alternative would be to use LSI which decomposes the TF-IDF matrix using SVD, or PLSI which uses the Expectation Maximization al-gorithm.

As previously argued, I am not going to use pure word statistics models. In this project, it is proposed to use the BERT model, which is a Bidirectional Transformer that can take advantage of the information from left to right and vice versa simultaneously. In addition, the attention layers provide the flexibility to pay attention to certain parts of the sentence. This model has a pretrained model of large volumes of text in an unsupervised way, predicting the next sentence or the next word. In this task, it is proposed to use the pretrained model and execute fineunning for our classification task. The model has been implemented in the Pytorch library.



