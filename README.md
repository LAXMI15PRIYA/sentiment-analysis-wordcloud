# 📊 Sentiment Analysis & Word Cloud Project

![Python](https://img.shields.io/badge/Python-3.x-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A sentiment analysis pipeline that classifies customer reviews as **Positive**, **Negative**, or **Neutral** using **TextBlob**, then visualizes the results with a sentiment distribution chart and a word cloud of the most common terms in negative reviews — surfacing what actually drives customer dissatisfaction.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [Workflow](#workflow)
- [Results](#results)
- [Sample Output](#sample-output)
- [How to Run](#how-to-run)
- [Project Structure](#project-structure)
- [Key Insights](#key-insights)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## Overview
Customer feedback is one of the richest sources of insight a business has — but reading through hundreds of reviews manually doesn't scale. This project automates that process: it scores review sentences by sentiment polarity, classifies them, and visualizes the results so patterns in customer dissatisfaction become immediately visible.

## Tech Stack
| Category | Tools |
|---|---|
| Language | Python |
| Data Handling | pandas, numpy |
| Sentiment Analysis | TextBlob |
| Visualization | matplotlib, seaborn |
| Text Visualization | wordcloud |

## Dataset
A collection of customer review sentences covering product quality and service experience, stored in `Sentiment_Analysis.csv`.

## Workflow
1. **Load data** — import review sentences from CSV
2. **Score sentiment** — apply TextBlob polarity scoring to each sentence
3. **Classify** — label each review as Positive (`polarity > 0`), Negative (`polarity < 0`), or Neutral (`polarity = 0`)
4. **Export** — save labeled results to `Sentiment_Labeled.xlsx`
5. **Visualize distribution** — pie chart of sentiment breakdown
6. **Isolate negative feedback** — filter negative reviews
7. **Generate word cloud** — highlight the most frequent terms driving negative sentiment

## Results

| Sentiment | Count | Percentage |
|---|---|---|
| Positive | 12 | 54.55% |
| Negative | 9 | 40.91% |
| Neutral | 1 | 4.55% |

## Sample Output

**Sentiment Distribution**
![Sentiment Pie Chart](piechart.png)

**Word Cloud — Negative Reviews**
![Negative Word Cloud](wordcloud.png)

## How to Run
```bash
# Clone the repository
git clone https://github.com/LAXMI15PRIYA/sentiment-analysis-wordcloud.git
cd sentiment-analysis-wordcloud

# Install dependencies
pip install pandas numpy matplotlib seaborn textblob wordcloud

# Download TextBlob corpora (first-time setup)
python -m textblob.download_corpora

# Launch the notebook
jupyter notebook Sentiment_Analysis_&_Word_Cloud_Project.ipynb
```

## Project Structure


