## Sentiment Analysis on IMDB Movie Reviews

### Overview

This project focuses on building a sentiment analysis model to classify movie reviews from the IMDB dataset as either positive or negative. The IMDB dataset contains 50,000 movie reviews that are labeled either positive (1) or negative (0). Our goal is to train a model that can predict the sentiment of a given review accurately.

### Dataset

The dataset is provided by the `keras` library and consists of 25,000 training reviews and 25,000 testing reviews. Each review in the dataset is tokenized, and words are replaced with integers representing their relative frequency of occurrence. For instance, the integer "3" might represent the third most frequent word in the dataset.

### Data Preprocessing

Given the varying lengths of movie reviews, data preprocessing involved padding sequences to ensure each review had a uniform length. This step ensures that the model receives input data of consistent shape.

### Model Architecture

The neural network model is built using Keras and consists of the following layers:

1. **Embedding Layer**: This layer converts the integer sequences into dense vectors of fixed size. It helps in reducing dimensionality and capturing semantic meaning of words.
2. **LSTM Layer**: LSTM (Long Short-Term Memory) is a type of Recurrent Neural Network (RNN) layer. It's particularly suited for sequence data, like our movie reviews, as it can capture long-term dependencies and patterns in the data.
3. **Dense Layer**: A fully connected layer with a sigmoid activation function. It outputs a value between 0 and 1, representing the predicted sentiment of the review (0 for negative and 1 for positive).

### Results

After training the model for 10 epochs, it achieved an accuracy of 85.48% on the test set. Sample predictions on test data showcased the model's ability to categorize movie reviews effectively.

### Conclusion and Future Work

This project serves as an introduction to sentiment analysis using deep learning. While the achieved accuracy is promising, there's always room for improvement. Future work could involve experimenting with more complex model architectures, fine-tuning hyperparameters, or using pre-trained word embeddings like Word2Vec or GloVe.
