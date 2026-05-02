# Real Bias News Detector
## By: Lauren Crawford () & Maria Martin-Barbera (10955852)

## Introduction
In this day and age media can be used for anything. Therefore, this project aims to determine whether an article is real or fake. In addition, media can be used to influence individuals' perspective, hence it also detects whether the article is right leaning or left learning. 

## Program Language
This issue has been addressed using python for all of the steps (preprocessing, EDA, model training/ testsing and UI integration).

## Datasets
For the real news aspect of this project the following dataset was used this [LINK](https://www.kaggle.com/datasets/emineyetm/fake-news-detection-datasets/data). A quick summary of the data is that there are 2 seperate datasets one contaitning real news (indicated by the source of the article being Reuters) and a fake dataset which was flagged unreliable by Politifact (fact checking org). Both dataset contains similar amount of observations and have the same features.




## Navigation of this Repo/ Folder
These are all the files within this repo. 

### Code Files:
- `real_news.ipynb`: This file will showcase all the preprocessing and EDA for determining whether the article is real or not.
- `real_news_mlds.ipynb`: This file will showcase all the models tested for determining whether the article is real or fake.
- `INSERT FILE NAME`: This file will showcase all the preprocessing and EDA for determining whether the article is left leaning or right leaning.
- `INSERT FILE NAME_2`: This file will showcase all the models tested for determining whether the article is real or fake.
- `INSERT FILE NAME_3`: This file utilizes the clean datasets generated from `real_news.ipynb` and `INSERT FILE NAME` and utilizes one of the models [per section (i.e. real news or bias detection)] to be integrated with the UI.

Due that the datesets used are big we were not able to insert the data directly here. Hence, we have used KaggleHub to be able to read it and for the convinience of the user after preprocessing the cleaned data will be generate. Therfore, the following section.

### Dataset Files Generated:
- `clean_real_news`: This file contains the preprocessed data for the real news model.

### Non-Code File:
- `Real Neutral News - Lauren & Maria.pdf`: This is the presentation of this project

## How to run this code?
- First, please make a virtual environment by using the following command in terminal:
  `python3 -m venv venv`
- Then activate it
  - If you are a Windows user then: `.\venv\Scripts\activate`
  - If you are a Mac/Linux user then: `source venv/bin/activate`
- Then run the following command to ensure you have all the neccesary libraries installed:
  `pip install -r requirements.txt`
- Now run this command: `jupyter notebook`

Now that you have the setup you will need to run the following files in order (descriptions for each file provided above):

- You run 1 and 2 in order to get the cleaned data.
1. `real_news.ipynb`
2. `INSERT FILE NAME`
- Then run 3 to get the UI
3. `INSERT FILE NAME_3`




