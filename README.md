# Capstone_Sentiment_Analysis
# Video Game Review Sentiment Analysis

This capstone project uses **machine learning and natural language processing (NLP)** to analyze player reviews of video games.  
The goal is to help developers and marketing teams **understand player sentiment, identify key feedback themes**, and make **data-driven decisions** to improve the gaming experience.

---

## Business Goal

**Use sentiment analysis to extract meaningful insights from video game reviews, helping developers:**
- Prioritize updates and fixes
- Improve customer satisfaction
- Optimize marketing strategies

---

##  Project Objectives

- **Classify** player reviews as **Positive** or **Negative**
- **Identify key topics** and themes mentioned by players using BERTopic  
- **Track sentiment trends** over time to see how updates or patches affect perception  
- **Generate actionable insights** to inform development and marketing decisions  

---

## Machine Learning Models

Three models were trained and compared for performance:

| Model | Accuracy | Notes |
|--------|-----------|-------|
| **Logistic Regression** | ~88% | Best balance of accuracy and interpretability |
| **Random Forest** | ~84% | Good performance but slower and less interpretable |
| **XGBoost** | ~86% | Excellent at capturing nonlinear patterns; used for SHAP explainability |

All models used **TF-IDF vectorization** to convert text into numeric features for training.

---

## Key Techniques

| Technique | Purpose |
|------------|----------|
| **TF-IDF** | Text feature extraction |
| **SHAP (Shapley Additive Explanations)** | Explain model predictions and identify impactful words |
| **BERTopic** | Unsupervised topic modeling to cluster player feedback |
| **Streamlit + ngrok** | Interactive web app for real-time sentiment prediction |
| **Matplotlib / Seaborn** | Visualization of trends, sentiment distribution, and top words |

---

## Results & Insights

### Model Performance
- **Logistic Regression achieved the highest accuracy (~88%)** and provided consistent predictions.  
- **XGBoost was selected for SHAP explainability**, showing how specific words drive sentiment classifications.

### Top Positive Words
`fun`, `amazing`, `great`, `love`, `recommend`

### Top Negative Words
`bug`, `crash`, `boring`, `lag`, `bad`

---

## SHAP Summary (Explainable AI)

The SHAP summary plot reveals which words most strongly influence the sentiment prediction.  
- **Red dots (positive impact):** Push prediction toward *positive sentiment*  
- **Blue dots (negative impact):** Push prediction toward *negative sentiment*

This ensures our model is transparent and explainable for stakeholders.

![SHAP Plot](shap_summary.png)

---

## BERTopic – Key Themes in Reviews

Using BERTopic, the reviews were grouped into key discussion themes:

| Topic | Description |
|--------|--------------|
| **Gameplay Experience** | Fun, challenge, replay value |
| **Performance Issues** | Bugs, crashes, lag |
| **Graphics & Audio** | Visual quality, sound design |
| **Story & Content** | Narrative depth and creativity |

![Topic Words](topic_words.png)

---

## Tech Stack

| Category | Tools |
|-----------|-------|
| **Languages** | Python |
| **Libraries** | scikit-learn, XGBoost, Pandas, NumPy, Matplotlib, Seaborn, SHAP, BERTopic, Joblib |
| **Framework** | Streamlit |
| **Deployment** | ngrok (temporary tunnel) |
| **Notebook** | Kaggle |

---

##  How to Run Locally

1. Clone the repository  
   ```bash
   git clone https://github.com/YOURUSERNAME/video-game-sentiment-analysis.git
   cd video-game-sentiment-analysis

