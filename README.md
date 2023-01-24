# Zindi-Challenge--Sentiment-Analysis

# ZINDI NLP CHALLENGE : [To Vaccinate or Not to Vaccinate](https://zindi.africa/competitions/zindiweekendz-learning-to-vaccinate-or-not-to-vaccinate/)

## Repository description
This repository contains the basic files to start the NLP Live Project based on the Zindi's challenge [To Vaccinate or Not to Vaccinate: It’s not a Question by #ZindiWeekendz](https://zindi.africa/competitions/zindiweekendz-learning-to-vaccinate-or-not-to-vaccinate/).

- The folder `data` contains the dataset.
- The folder `notebooks` contains sample notebooks to get started.


## Instructions
1. Solve this challenge by applying your DS knowledge to finetune a pretrain Hugging Face model. [Read more](https://medium.com/mlearning-ai/fine-tuning-bert-for-tweets-classification-ft-hugging-face-8afebadd5dbf)
1. Create a Gradio app based on your trained model. [Read more](https://huggingface.co/course/chapter9/1)
1. Upload your Hugging Face model (and pipeline), and Deploy your Gradio app on the HuggingFace platform. [Read more](https://huggingface.co/docs/hub/models-uploading)
1. Dockerize your Gradio app to get it ready to be deployed to any cloud hub. [Watch this](https://www.youtube.com/watch?v=f6zJwK-pCJo)

Introduction

This is my third project in turning ML models into actual applications other people can use. In this project, I create  an AI-Sentiment analysis web application using Gradio and Hugging face.

Challenge Description

This challenge was designed specifically as a #ZindiWeekendz hackathon (To Vaccinate or Not to Vaccinate: It’s not a Question). We are re-opening the hackathon as a Knowledge Challenge, to allow the Zindi community to learn and test their skills. To help you all out, we’ve created a new Tutorials tab with helpful resources from the community. We encourage Zindians to share their code on the discussion board so that everyone in our community can learn from and support one another.

Work has already begun towards developing a COVID-19 vaccine. From measles to the common flu, vaccines have lowered the risk of illness and death, and have saved countless lives around the world. Unfortunately in some countries, the 'anti-vaxxer' movement has led to lower rates of vaccination and new outbreaks of old diseases.

Although it may be many months before we see COVID-19 vaccines available on a global scale, it is important to monitor public sentiment towards vaccinations now and especially in the future when COVID-19 vaccines are offered to the public. The anti-vaccination sentiment could pose a serious threat to the global efforts to get COVID-19 under control in the long term.

**The objective of this challenge is to develop a machine learning model to assess if a Twitter post related to vaccinations is positive, neutral, or negative. This solution could help governments and other public health actors monitor public sentiment towards COVID-19 vaccinations and help improve public health policy, vaccine communication strategies, and vaccination programs across the world.**

## About
The data comes from tweets collected and classified through Crowdbreaks.org [Muller, Martin M., and Marcel Salathe. "Crowdbreaks: Tracking Health Trends Using Public Social Media Data and Crowdsourcing." Frontiers in public health 7 (2019).]. Tweets have been classified as pro-vaccine (1), neutral (0) or anti-vaccine (-1). The tweets have had usernames and web addresses removed.

The objective of this challenge is to develop a machine learning model to assess if a twitter post that is related to vaccinations is positive, neutral, or negative.

**Variable definition:**

**tweet_id:** Unique identifier of the tweet

**safe_tweet:** Text contained in the tweet. Some sensitive information has been removed like usernames and urls

**label:** Sentiment of the tweet (-1 for negative, 0 for neutral, 1 for positive)

**agreement:** The tweets were labeled by three people. Agreement indicates the percentage of the three reviewers that agreed on the given label. You may use this column in your training, but agreement data will not be shared for the test set.


Files available for download are:

**Train.csv** - Labelled tweets on which to train your model

**Test.csv** - Tweets that you must classify using your trained model

**SampleSubmission.csv** - is an example of what your submission file should look like. The order of the rows does not matter, but the names of the ID must be correct. Values in the 'label' column should range between -1 and 1.

**NLP_Primer_twitter_challenge.ipynb** - is a starter notebook to help you make your first submission on this challenge.

**Process**

1.This challenge is solved by applying my Data science knowledge to fine-tune a pretrained Hugging face model:
First import data (test and train CSV from Zindi into Colab)
2.Code to eliminate rows containing NaN values
3. Load datasets into pretrained model
4. Select model under sentiment analysis for fine-tuning

Fine-Tuning Steps
1. Prepare the dataset
2. Load pretrained Tokenizer, call it with dataset(encoding)
3. Build pytorch dataset with encodings
4. Load pretrained model
5.Load trainer and train into native pytorch training loop

After fine-tuning on pretrained model,
a. Embed into Grado App
b. Host on Hugging Face


Steps to upload on Hugging Face
1. Create a Hugging face account
2. Download test- trainer folder from google Colab and save model on Hugging Face
3. Host your fine-tuned model and app on the Hugging Face Platform

You can find my Hugging face model at:https://huggingface.co/Mawulom/Fine-Tuned-Bert_Base_Cased_Sentiment_Analysis/blob/main/README.md

Results

Final Evaluation Metrics
{'eval_loss': 0.6129302978515625,
 'eval_accuracy': 0.7615,
 'eval_runtime': 59.1046,
 'eval_samples_per_second': 33.838,
 'eval_steps_per_second': 4.23}
 'eval_samples_per_second': 29.272,
 'eval_steps_per_second': 3.659}

