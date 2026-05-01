# Text Mining on ChatGPT Discourse — Sentiment & Topic Analysis

**Course:** CIS 3252 — Business Intelligence  
**Institution:** Cal Poly Pomona  
**Term:** Spring 2026  

## Overview

This project applies **text mining techniques** to analyze public discourse about ChatGPT on the **Bluesky** social platform. Using sentiment analysis and LDA topic modeling, it identifies patterns in public perception and translates them into actionable business intelligence insights.

## Research Questions

1. What is the overall public sentiment toward ChatGPT on Bluesky?
2. What drives negative sentiment?
3. What are the dominant topics in ChatGPT-related discussions?
4. How can a technology company use these insights strategically?

## Dataset

- **Source:** Bluesky social platform (collected via [Communalytic](https://communalytic.org/))
- **Content:** User-generated posts related to ChatGPT
- **Scope:** Posts classified as opinion vs. fact using subjectivity scoring
  - Sentiment analysis used **opinion posts only** (158 posts)
  - Topic modeling used **both fact and opinion posts**

## Methodology

### Part 1 — Data Preprocessing
- Lowercased all text
- Removed URLs, mentions (`@`), hashtags (`#`), punctuation, and non-ASCII characters
- Removed stopwords
- Tokenized and lemmatized words to base forms
- Removed duplicates and empty entries
- Classified posts as **fact vs. opinion** using subjectivity scores

### Part 2 — Sentiment Analysis
Applied polarity scoring to opinion posts to classify each post as positive, negative, or neutral.

| Sentiment | Percentage |
|---|---|
| Positive | 73.42% |
| Negative | 20.89% |
| Neutral | 5.70% |

**Key finding:** Sentiment is strongly positive overall. Negative sentiment is driven by concerns about misinformation, AI advertising backlash, social/cultural anxiety about job displacement, and reliability issues.

### Part 3 — Topic Modeling (LDA)
Selected **k = 3 topics** based on coherence, exclusivity, and perplexity metrics.

| Topic | Label | Top Keywords | Share |
|---|---|---|---|
| Topic 1 | News Sharing & Content Dissemination | chatgpt, use, work, like, ai, get, free | ~30% |
| Topic 2 | User Opinions & Everyday Usage | chatgpt, search, google, think, make, answer | ~40% |
| Topic 3 | Global & Multilingual Discussions | chatgpt, de, en, la, que, el, ai | ~30% |

**Key finding:** Topic 2 (personal experience, ChatGPT vs. Google comparisons) dominates, indicating the discourse is socially driven rather than purely technical.

## Business Insights

1. **Leverage positive momentum** — The 73.42% positive sentiment shows users respond well to capability-focused messaging (e.g., reasoning features). Continue highlighting productivity and practical value.

2. **Address the information trust gap** — Users compare ChatGPT to Google. Improving factual accuracy and adding source transparency features could reduce negative sentiment.

3. **Optimize for global utility** — Topic 3's multilingual content reflects a strong international user base. Localizing features and marketing for non-English regions is a high-impact opportunity.

4. **Strategic recommendation** — Strengthen trust through transparency: clearly communicate model limitations, avoid overpromising, and develop API/workflow integrations that make ChatGPT indispensable for daily work.

## Tools & Techniques

- **Communalytic** — Social media data collection
- **Text Preprocessing** — Lowercasing, stopword removal, lemmatization, tokenization
- **Sentiment Analysis** — Polarity and subjectivity scoring (TextBlob/VADER)
- **Topic Modeling** — Latent Dirichlet Allocation (LDA)
- **Visualization** — Bar charts for sentiment distribution and topic prevalence

## Limitations

The sentiment analysis subset (158 opinion posts) is relatively small and may not fully represent all perspectives on Bluesky or the broader internet.
