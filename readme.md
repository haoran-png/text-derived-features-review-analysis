


# Star Ratings vs Review Text  
**An Exploratory Analysis of Sentiment Disagreement in Online Reviews**

## Project Overview

This project investigates the relationship between numeric star ratings and sentiment expressed in review text, with a particular focus on **cases where these two signals disagree**. Rather than treating disagreement as noise or error, the analysis views it as a potentially informative phenomenon that reveals how users communicate evaluation in practice.

Using a large corpus of online reviews, the project combines **data wrangling, interpretable text feature engineering, exploratory visual analysis, and simple explanatory modelling** to examine how and why disagreement occurs between ratings and text sentiment.

The project adopts an **explanatory and exploratory data science approach**, prioritising transparency and interpretability over predictive optimisation.

---

## Research Questions

The analysis is guided by the following research questions:

1. How frequently do star ratings and text derived sentiment signals disagree withinYelp reviews?
2. Which observable textual characteristics are associated with larger rating-text mismatches?
3. Is disagreement symmetric, or do certain types of mismatch occur more frequently?

---

## Dataset

The project uses a large-scale public review dataset containing:

- Numeric star ratings  
- Free-text review content  
- Review metadata (e.g. usefulness votes, timestamps)

Due to the significant size of the original Yelp dataset, the raw JSON files are not included in this repository. To replicate the analysis, please download the dataset directly from https://business.yelp.com/data/resources/open-dataset/.

Once downloaded, extract the files and place them in the data/yelp/ directory. Note that the analysis notebook is designed to load a subset of this data to maintain computational efficiency.

---

## Structure

├── data
│   └── yelp
│       ├── yelp_academ...  (JSON file)
│       ├── yelp_academ...  (JSON file)
│       ├── yelp_academ...  (JSON file)
│       ├── yelp_academ...  (JSON file)
│       ├── yelp_academ...  (JSON file)
│       ├── Yelp Dataset D... (PDF file)
│       └── yelp_dataset.tar
├── submission
│   ├── code.pdf
│   └── report.pdf
├── .gitattributes
├── .gitignore
├── readme.md
└── work.ipynb

---

## Methodology

The analysis follows an iterative data science process:

### 1. Data Wrangling
- Parsing large JSON review files  
- Cleaning and normalising text  
- Handling missing and irrelevant fields  
- Constructing an analysis-ready tabular dataset  

### 2. Feature Engineering (Interpretable)
Text-derived features were designed to remain simple and explainable, including:
- Review length (number of words)  
- Expressive markers (e.g. questions, exclamation marks)  
- Sentiment scores extracted using a lexicon-based method  

A **binary indicator of strong disagreement** was constructed to support explanatory modelling.

### 3. Exploratory Data Analysis
- Distribution of star ratings  
- Sentiment distributions across rating levels  
- Visualisation of disagreement patterns  
- Comparison of review characteristics across agreement and disagreement groups  

### 4. Explanatory Modelling
- Simple, interpretable models were used to examine associations between review characteristics and disagreement  
- Emphasis was placed on **effect sizes and interpretability**, not prediction accuracy  

---

## Key Findings

- Disagreement between star ratings and review text is **common**, not exceptional  
- Disagreement is **asymmetric**, with positive ratings paired with negative text occurring more frequently  
- Longer and more expressive reviews are more likely to exhibit disagreement  
- Reviews marked as useful by other users often contain nuanced sentiment that increases mismatch  

These findings suggest that disagreement reflects **complex and qualified user expression**, rather than random inconsistency.

