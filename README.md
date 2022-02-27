# Fine Grained Sentiment Analysis (Emotion Detection)

## Background

Sentiment analysis aims to uncover opinions and sentiment in unstructured data such as text, audio, and images. Most studies mainly focus on extracting two sentiments (or polarity), Positive or Negative, from these materials, though some include an additional sentiment of Neutral. This makes most sentiment analysis a supervised binary classification task.

While numerous studies have trained models which excel at this binary classification of sentiment, there are few studies which look into classifying text into more fine-grained classes, such as the emotions a text holds (eg. whether the text contains happiness). Current studies also examine this from a document level, where the entire text is fed into the model for classification, instead of at a sentence level, where the document is broken into individual sentences and each sentence will receive its own classification.

As such, our experiments break new ground by 1) training models which can detect and classify emotions 2) at a sentence level. We also hope to go beyond binary classification and use more than two classes/emotions with each text input being classified as belonging to one emotion. This makes our experiments a multi-class classification task.

## Methodology and Results

The classes we used were Ekman’s 6 primary emotions of **happiness, sadness, anger, disgust, surprise, and fear.**

We then performed our multi-class classification on the **ISEAR, DailyDialog, and Multimodal EmotionLines datasets** with 3 different strategies:

1. Lexicon

2. Problem Transformation

3. Transfer Learning

To evaluate our models, we used **Recall** as our primary metric as we conceived a secondary goal of creating models that can predict negative emotions better than positive emotions; The presence of such emotions imply the need for urgent remediation/attention. For example, misclassifying an angry customer review as a happy one would cause the customer’s case to go unnoticed and unresolved, leading to even greater anger and dissatisfaction from the customer. It would have been better if a happy customer review had been misclassified as an angry one as in the worst scenario, it would have been a false alarm. However, we examined three other metrics (Accuracy, Precision, F1-score) for reference and to get a complete picture of our models’ performance.

A summary of our data cleaning, vectorisation, training, and results are as below:

![image](https://user-images.githubusercontent.com/81354022/155878385-a4d03249-883d-4e5d-9b26-92493b045b42.png) 
