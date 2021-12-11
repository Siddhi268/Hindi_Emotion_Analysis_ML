# Hindi Text Emotions Classification (ML Approach)


## Goal: 

Build an application (end to end) that predicts emotions(i.e. angry,sad,neutral,happy) behind the hindi text.

## Project Introduction

This Hindi Emotion Analysis project classifies the Hindi text sentence into the set of classes such as Angry, Happy, Sad and Neutral.The project plots word cloud for all the respective emotions. Implemented and trained the Multinomial Naive Bayes model with both Count Vectorizer and Tf-idf Vectorizer. The project allows user to predict the emotion on new text in hindi.

## Steps followed to built the model:

* Data has been read into lists and have been finally converted into a Pandas DataFrame.

* Input to the model (X) and output (y) has been separated.

* Randomly split the X and Y into train and test data.

* Using CountVectorizer and TF-IDF Vectorizer text has been converted into numerics as model needs numbers not String or tokens. Here we are giving it some stop words so that they can be removed as they do not contribute to the model building. Also a tokenizer defined manually has been passed as the built-in tokenizer will split everything into characters which we don’t want so the manually built tokenizer (my_tokenizer) splits about white spaces only.

* A Multinomial Naive Bayes classifier has been trained with both vectorization technique(Count Vectorizer & Tf-idf Vectorizer).

* Accuracy has been evaluated.

## Text Vectorization:

Vectorization is the general process of turning a collection of text documents into numerical feature vectors.

1. COUNT VECTORIZER:

CountVectorizer converts a collection of text documents to a matrix of token counts: the occurrences of tokens in each document. This implementation produces a sparse representation of the counts.

2. TF-IDF(Term Frequency-Inverse Document Frequency) VECTORIZER:

TF-IDF stands for Term Frequency-Inverse Document Frequency which basically tells the importance of the word in the corpus or dataset. TF-IDF contain two concept Term Frequency(TF) and Inverse Document Frequency(IDF).Term Frequency is defined as how frequently the word appears in the document or corpus. As each sentence is not the same length so it may be possible a word appearing in a long sentence occurs more time as compared to word appearing in a shorter sentence.Inverse Document Frequency (IDF) is a scoring of how rare the word is across documents. IDF is a measure of how rare a term is. Rarer the term, more is the IDF score. 


## Model

1.Multinomial Naive Bayes Classifier(Count Vectorizer):

![cv](https://user-images.githubusercontent.com/73767113/145659777-3e155847-e784-4135-ad50-3b0699ce916c.jpg)


2.Multinomial Naive Bayes Classifier(TF-IDF Vectorizer):

![tf](https://user-images.githubusercontent.com/73767113/145659787-959c29ca-aac9-4b4e-a420-05164e9f8fc4.jpg)


#### Link to Jupyter Notebook in Repository
[Notebook](https://github.com/Siddhi268/Hindi_Emotion_Analysis_ML/blob/main/Hindi_Emotion_Analysis_ML.ipynb)



## Deploying model

<p> Saved the model in a file using the <b>pickle library</b> </p>

1.Landing Page

![landing](https://user-images.githubusercontent.com/73767113/145659796-08b85920-d255-4b52-a567-96bcacf30778.jpg)


2.Emotion Detection Page

![emotion_detection](https://user-images.githubusercontent.com/73767113/145659808-945b5164-8060-4ae7-bc0e-1191518a3899.jpg)



Developed app using Streamlit in VSCode

Deployed app on Heroku : https://hindi-emotion-analysis-app1.herokuapp.com/


