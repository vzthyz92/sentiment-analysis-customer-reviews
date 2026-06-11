# Amazon Product Review Sentiment Analysis

## Overview

This project applies Natural Language Processing (NLP) techniques to analyze customer sentiment in Amazon product reviews. Using spaCy and SpaCyTextBlob, the project cleans review text, classifies sentiment, measures review similarity, and visualizes sentiment trends within the dataset.

The goal is to gain actionable insights from customer feedback by identifying positive and negative sentiment patterns that can help improve products and customer experience.

---

## Project Objectives

- Clean and preprocess customer review text
- Perform sentiment analysis using NLP techniques
- Classify reviews into sentiment categories
- Compare review similarity using semantic embeddings
- Visualize sentiment distributions and polarity scores
- Extract business insights from customer feedback

---

## Dataset

### Amazon Consumer Reviews Dataset

The project uses the following dataset:

```text
Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv
```

The dataset contains Amazon customer reviews, ratings, product information, and review text.

### Key Feature Used

| Feature | Description |
|----------|------------|
| reviews.text | Customer review text |

Missing review entries are removed before analysis.

---

## Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Programming Language |
| Pandas | Data Analysis |
| spaCy | Natural Language Processing |
| SpaCyTextBlob | Sentiment Analysis |
| Matplotlib | Data Visualization |
| Collections (Counter) | Word Frequency Analysis |
| Jupyter Notebook | Development Environment |

---

## NLP Pipeline

### 1. Data Loading

The Amazon reviews dataset is loaded into a Pandas DataFrame for analysis.

### 2. Text Cleaning

Review text is preprocessed using spaCy:

- Convert text to lowercase
- Remove punctuation
- Remove stop words
- Remove extra whitespace
- Generate cleaned review text

Example:

```text
Original:
"This product is AMAZING and works perfectly!"

Cleaned:
"product amazing works perfectly"
```

---

## Sentiment Analysis

Sentiment is calculated using **SpaCyTextBlob**, which assigns a polarity score to each review.

### Sentiment Categories

| Polarity Score | Classification |
|---------------|---------------|
| Very High Positive | Very Positive |
| Positive | Positive |
| Around Zero | Neutral |
| Negative | Negative |
| Very Low Negative | Very Negative |

Each review receives:

- A numerical polarity score
- A sentiment label

Example:

```text
Review:
"This product exceeded my expectations."

Polarity:
0.75

Sentiment:
Very Positive
```

---

## Review Similarity Analysis

The project compares customer reviews using spaCy's semantic similarity capabilities.

### Purpose

Determine how closely related two reviews are in meaning.

Example:

```python
review_1.similarity(review_2)
```

The similarity score ranges between:

```text
0 → Completely Different
1 → Nearly Identical
```

This can be useful for:

- Duplicate review detection
- Customer feedback clustering
- Recommendation systems

---

## Visualizations

Several visualizations were created to explore sentiment patterns.

### Sentiment Distribution

Bar chart showing the number of reviews in each sentiment category.

Insights include:

- Overall customer satisfaction levels
- Positive vs negative review balance

### Polarity Score Distribution

Histogram showing the spread of sentiment polarity scores.

Helps identify:

- Overall sentiment trends
- Review concentration around positive or negative values

### Most Common Words

Word frequency analysis highlighting the top 15 most frequently used terms in customer reviews.

Provides insight into:

- Common product discussions
- Frequently mentioned features
- Customer concerns and praise points

---

## Project Workflow

```text
Load Amazon Reviews Dataset
            ↓
Clean Review Text
            ↓
Preprocess with spaCy
            ↓
Sentiment Analysis
            ↓
Review Similarity Analysis
            ↓
Generate Visualizations
            ↓
Business Insights
```

---

## Key Findings

### Positive Reviews

Customers frequently praised:

- Product value
- Ease of use
- Affordability
- Convenience

### Negative Reviews

Common complaints included:

- Product quality issues
- Missing components
- Delivery-related problems

### General Trend

The dataset contains a strong concentration of positive reviews, indicating generally favorable customer experiences.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/amazon-review-sentiment-analysis.git
cd amazon-review-sentiment-analysis
```

### Install Dependencies

```bash
pip install pandas matplotlib spacy spacytextblob
```

### Download spaCy Model

```bash
python -m spacy download en_core_web_md
```

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
sentiment_analysis.ipynb
```

Run all cells sequentially.

---

## Repository Structure

```text
project/
│
├── sentiment_analysis.ipynb
├── Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv
├── README.md
│
├── Visualizations
│   ├── Sentiment Distribution
│   ├── Polarity Histogram
│   └── Word Frequency Analysis
│
└── NLP Components
    ├── Text Cleaning
    ├── Sentiment Analysis
    └── Review Similarity
```

---

## Skills Demonstrated

- Natural Language Processing (NLP)
- Text Preprocessing
- Sentiment Analysis
- Semantic Similarity Analysis
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Visualization
- Business Insight Generation
- Python Programming
- spaCy NLP Framework

---

## Future Improvements

- Implement machine learning sentiment classifiers
- Add aspect-based sentiment analysis
- Create interactive dashboards
- Generate word clouds
- Perform topic modeling
- Deploy as a web application
- Compare multiple sentiment analysis techniques

---

## Business Applications

This type of sentiment analysis can be used to:

- Monitor customer satisfaction
- Identify product issues early
- Improve customer support
- Track brand reputation
- Analyze customer feedback at scale
- Support product development decisions

---

## Author

**Thys van Zyl**

---

## License

This project was developed for educational and portfolio purposes.
