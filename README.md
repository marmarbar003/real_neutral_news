# Real Bias News Detector
## By: Lauren Crawford (10956355) & Maria Martin-Barbera (10955852)

## Introduction
In this day and age media can be used for anything. Therefore, this project aims to determine whether an article is real or fake. In addition, media can be used to influence individuals' perspective, hence it also detects whether the article is right leaning or left learning. 

## Program Language
This issue has been addressed using python for all of the steps (preprocessing, EDA, model training/ testsing and UI integration).

## Datasets
For the real news aspect of this project the following dataset was used this [LINK](https://www.kaggle.com/datasets/emineyetm/fake-news-detection-datasets/data). A quick summary of the data is that there are 2 seperate datasets one contaitning real news (indicated by the source of the article being Reuters) and a fake dataset which was flagged unreliable by Politifact (fact checking org). Both dataset contains similar amount of observations and have the same features.

For the new bias portion of this project, the following dataset was used [LINK](https://www.kaggle.com/datasets/emineyetm/fake-news-detection-datasets/data). This dataset contains over 10,000 articles obtained by webscraping allsides.com, a platform that presents news articles from differing political perspectives.  The articles were initially labeled "leaning-left", "left", "center", "right", and "leaning-right" but the formatting was changed to suit this project.  


## Navigation of this Repo/ Folder
These are all the files within this repo. 

### Code Files:
- `real_news.ipynb`: This file will showcase all the preprocessing and EDA for determining whether the article is real or not.
- `real_news_mlds.ipynb`: This file will showcase all the models tested for determining whether the article is real or fake.
- `bias_news.ipynb`: This file will showcase all the preprocessing and EDA for determining whether the article is left leaning or right leaning.
- `bias_news_modls.ipynb`: This file will showcase all the models tested for determining whether the article is real or fake.
- `UI.ipynb`: This file utilizes the model/ vecotrizers dumped in  `real_news_mlds.ipynb` and `bias_news_modls.ipynb` and utilizes one of the models [per section (i.e. real news or bias detection)] to be integrated with the UI. We have opted to chose the logistic regression for both as its the one that performed the best. However, if one wants to change the model used in this file just change the joblib model saved in the variable `bias_model` and `real_model`.

### Models/ Vectorizers Generated (saved with dump):
- `vectorizer_rn.joblib`: This is the trained text vectorizer (TF-IDF) for real news.
- `log_reg_rn.joblib`: This is the trained Logistic Regression for real news.
- `rand_for.joblib`: This is the trained Random Forest for real news.
- `svc_rn.joblib`: This is the trained SVM for real news.

- `vec_text.joblib`: This is the trained text vectorizer for bias detection.
- `model_decTree.joblib`: This is the trained Decision Tree for bias detection.
- `grid_best_estimator_svc.joblib`: This is the trained SVM for bias detection.
- `grid_best_estimator_logreg.joblib`: This is the trained Logistic Regression for bias detection.

Because the datesets used are big we were not able to insert the data directly here. Hence, we have used KaggleHub and HuggingFace to read in data. For the convenience of the user, after preprocessing, the cleaned data will be generated. Therfore, the following section...

### Dataset Files Generated:
- `clean_real_news.csv`: This file contains the preprocessed data for the real news model.
- `huggingFaceClean.json`: This file contains the preprocessed data for the bias news model, generated from the Hugging Face Dataset
- `KaggleClean.json`: This file contains the preprocessed data for the bias news model, generated from the Kaggle Dataset.

### Non-Code File:
- `Real Neutral News - Lauren & Maria.pdf`: This is the presentation of this project

## How to run this code?
- First, please make a virtual environment in the same directory as the files by using the following command in terminal:
`python3 -m venv venv`
- Then activate it
  - If you have a Windows user then: `.\venv\Scripts\activate`
  - If you have a Mac/Linux user then: `source venv/bin/activate`
- Then run the following command to ensure you have all the neccesary libraries installed:
  `pip install -r requirements.txt`
- Then run this so the venv will appear on jupyer notebook: `python -m ipykernel install --user --name=venv --display-name "Real Bias (venv)"`
- Now run this command: `jupyter notebook`

Now that you have the setup you will need to run the following files in order (descriptions for each file provided above):

**Before Running the code make sure you have selected the kernel named `Real Bias (venv)`**

- You run 1 and 2 in order to get the cleaned data, then run 3 and 4 in order to generate the models, and finally run 5 in order to run the user interface and test the application.
1. `real_news.ipynb`
2. `bias_news.ipynb`
- Then run 3 and 4 to generate the models.
3. `real_news_mlds.ipynb`
4. `bias_news_mdls.ipynb`
- Lastly, run 5 to interact with the user interface.
5. `UI.ipynb`




