# Chatbot: Your Personal Book Companion 📚🤖

<img src="https://github.com/AnasElbattra/Book-Recommendation-ChatBot/assets/75434006/2914dbe4-3824-4e91-a19a-97555d2945a8" alt="Bias" width="200"/>

## 🚀 Introduction

Welcome to Chatbook, your go-to content-based book recommender system! 🌟 Using the magic of natural language processing and machine learning, Chatbook offers personalized book suggestions based on insightful book summaries. Dive into a world of tailored recommendations, connecting readers with books that align with their unique interests. Let's embark on a literary adventure in the digital age!

## 💻 Tech Stack

Our chatbot is powered by a dynamic tech stack, featuring Dialogflow for the front end and Flask for the back end. This ensures a seamless and interactive experience. Discover two distinct recommendation options:

1️⃣ **Recommendation by Book Name:** Share your favorite book, and let the chatbot fetch related suggestions. Perfect for those with a specific book in mind.

2️⃣ **Recommendation by Genre:** Immerse yourself in recommendations based on your preferred genre. Ideal for readers seeking fresh perspectives.

## 📊 Data Source

We've harnessed the power of the CMU Book Summary Dataset on Kaggle, comprising summaries for a whopping 16,559 books. This dataset, enriched with vital metadata such as author, title, and genre, fuels Chatbook's intelligent recommendations.

## 🙌 Acknowledgments

A heartfelt shoutout to our incredible team members:

- [Anas Elbattra](https://github.com/AnasElbattra)
- [Ahmed Badawy](https://github.com/ahmedbadawy11)
- [Esmael Ezz](https://github.com/EsmaelEzz74)


## 🏃 Running the Code

1. We run our code locally on our machines.
2. For the notebook, we preprocess, clean, and transform the data into Word2Vec form.
3. Save this representation into a CSV file for later use:

```python
train_data.to_csv("Embeddings.csv", sep=";")
```

## 🗂️ Clustering

1. We cluster our data and get 5 labels.
2. For each label, we manually assign the most frequent genre.
3. Use the following code to check for the most frequent genre in each cluster:

```python
# Code snippet here
```

4. After classifying our data, save the dataframe with all the new features:

```python
random_sample.to_csv("Final_output.csv", index=False, sep=';')
```

Please note that the final accuracies may vary due to data randomization.

## 🤖 Chatbot

1. After finishing the notebook, install the ngrok application.
2. Start our server using the command:

```bash
ngrok http 5000
```

3. Take the provided https link and paste it in the Dialogflow fulfillment:

```
https://1889-41-33-218-52.ngrok-free.app/webhook
```

4. To use our work in the chatbot and Dialogflow, load the pre-saved dataframes:

```python
train_data = pd.read_csv("Embeddings.csv", sep=";")
random_sample = pd.read_csv("Final_output.csv", index=False, sep=';')
```

5. Run our .py file to connect the model to the chatbot.

## 📷 Chatbot Screenshots

<img src="https://github.com/AnasElbattra/Book-Recommendation-ChatBot/assets/75434006/10ce96f1-ab2d-417b-a597-f22d762d9b7f" alt="Bias" width="330"/>
<img src="https://github.com/AnasElbattra/Book-Recommendation-ChatBot/assets/75434006/d260ad41-d32a-48d5-b011-59a86e64d66a" alt="Bias" width="330"/>
<img src="https://github.com/AnasElbattra/Book-Recommendation-ChatBot/assets/75434006/f6d5d6cf-8608-44c5-ab4f-4b55c12806e7" alt="Bias" width="330"/>
