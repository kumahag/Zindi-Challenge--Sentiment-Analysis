# Zindi-Challenge--Sentiment-Analysis
Natural Language Processing -Sentiment Analysis

Introduction

This is my third project in turning ML models into actual applications other people can use. In this project, I create  an AI-Sentiment analysis web application using Gradio and Hugging face.

Setup

Install the required packages to be able to run the evaluation locally.

You need to have Python3 on your system. Then you can clone this repo and being at the repo's root (root :: repo_name> ...) follow the steps below:

Windows:

  python -m venv venv; venv\Scripts\activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt  
Linux & MacOs:

  python3 -m venv venv; source venv/bin/activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt  
The both long command-lines have a same structure, they pipe multiple commands using the symbol ; but you may manually execute them one after another.

Create the Python's virtual environment that isolates the required libraries of the project to avoid conflicts;
Activate the Python's virtual environment so that the Python kernel & libraries will be those of the isolated environment;
Upgrade Pip, the installed libraries/packages manager to have the up-to-date version that will work correctly;
Install the required libraries/packages listed in the requirements.txt file so that it will be allow to import them into the python's scripts and notebooks without any issue.
NB: For MacOs users, please install Xcode if you have an issue.

Process

1.This challenge is solved by applying my Data science knowledge to fine-tune a pretrained Hugging face model:
First import data (test and train CSV from Zindi into Colab)
2.Code to eliminate rows containing NaN values
df=df[~df.isna(). any(axis=1)]
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

Results
