# Disaster Tweet Classification: Leveraging NLP for Crisis Detection

This project aims to build an effective machine learning model to predict whether a tweet is about a real disaster or not. The task was part of a Kaggle competition, and the goal was to leverage Natural Language Processing (NLP) techniques—especially transformer-based models—to classify tweets accurately during crises.

## Project Overview

In this project, you will find:
- **Project Code:** The main implementation is available in the Jupyter Notebook `nlp-ensemble(4).ipynb`
- **Project Presentation Slides:** A detailed slide deck (`ML Presentation.pdf`) walks through the methodology, analysis, and key insights.
- **Kaggle Competition:** This project is based on the [NLP Getting Started Disaster Tweets Competition](https://www.kaggle.com/competitions/nlp-getting-started/overview)

The central challenge is to build a robust machine learning pipeline that can distinguish between tweets related to real disasters and those that are not, using a dataset of 10,000 hand-classified tweets.

## Key Objectives

- **Accurate Classification:** Develop a model to reliably predict disaster-related tweets.
- **Efficient Preprocessing:** Clean and preprocess noisy text data by removing redundant elements (hyperlinks, emojis, etc.).
- **Transformer-based Approaches:** Utilize state-of-the-art NLP models (BERT, roBERTa, deBERTa, and distilBERT) to capture contextual nuances and improve performance.
- **Ensemble Modeling:** Combine predictions from multiple models to achieve higher accuracy (final Kaggle score of 84.2%).

## Data Description

The dataset used for this project contains 10,000 tweets that have been manually classified into two categories:
- **Disaster-related tweets**
- **Non-disaster tweets**

This balanced dataset allowed for effective training and validation of the classification models.

## Methodology

### Exploratory Data Analysis (EDA)
- **Data Insights:** Analysis confirmed that tweet metadata such as word count and tweet length were not reliable predictors of the target variable.
- **Class Balance:** Ensured that the classes were balanced to avoid biased learning.

### Preprocessing
- **Text Cleaning:** 
  - Removed hyperlinks and emojis.
  - Cleaned abbreviations and redundant elements.
- **Tokenization:** Handled informal language and typos using robust transformer tokenizers.

### Model Selection
Several transformer-based models were evaluated:
- **BERT:** Provided a strong baseline with bidirectional context.
- **roBERTa:** Improved performance by using advanced training techniques.
- **deBERTa:** Enhanced contextual understanding via disentangled attention.
- **distilBERT:** Offered a lighter, faster alternative with minimal loss in accuracy.

### Ensemble Approach
- **Final Model:** An ensemble method was implemented to combine the strengths of the individual models, leading to improved predictive performance.
- **Performance Metrics:** The ensemble approach achieved a Kaggle score of 84.2%, demonstrating high sensitivity and specificity in classification.

## Results & Insights

- **Performance:** The ensemble model outperformed individual models by reducing false negatives and false positives.
- **Lessons Learned:** 
  - Proper text cleaning (removing noise like hyperlinks and emojis) significantly improved model accuracy.
  - Combining multiple models through ensembling can yield better results than any single model alone.
  - Transformer models are highly effective for processing short, noisy texts typical of tweets.

## How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/disaster-tweet-classification.git
   cd disaster-tweet-classification
   ```

2. **Install Dependencies:**
   Ensure you have Python 3.7+ installed. Then, install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook:**
   Launch Jupyter Notebook and open `nlp-ensemble(4).ipynb`:
   ```bash
   jupyter notebook nlp-ensemble(4).ipynb
   ```

4. **Review the Presentation:**
   Open the `ML Presentation.pdf` to follow the project workflow and analysis.

## Acknowledgements

- **Kaggle Competition:** [NLP Getting Started Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/overview)
