# **Sentiment Analysis on Product Reviews - Machine Learning**

## **Project Overview**
This project performs **sentiment analysis** on product reviews using **TextBlob**. It classifies customer feedback as **positive, neutral, or negative** based on the text's polarity. The analysis includes data preprocessing, sentiment classification, and interactive visualizations.

## **Features**
- **Preprocessing**: Cleans text by removing punctuation, converting to lowercase, and removing special characters.
- **Sentiment Classification**: Uses **TextBlob** to determine polarity and classify the sentiment.
- **Evaluation**: Compares model predictions with actual sentiment labels using accuracy and classification reports.
- **Visualization**:
  - Sentiment distribution
  - Word cloud for positive & negative reviews
  - Interactive sentiment trends using **Plotly**

## **Data Processing**
- The dataset is loaded and preprocessed.
- A `sentiment` column is created based on ratings:
  - **Positive (1)**: Ratings ≥ 4
  - **Neutral (0)**: Rating = 3
  - **Negative (-1)**: Ratings ≤ 2
- Each review is cleaned by:
  - Converting to lowercase
  - Removing non-alphabetic characters
  - Removing extra spaces

## **Sentiment Analysis Methodology**
1. **TextBlob Sentiment Analysis**
   - Calculates **polarity score** (-1 to 1).
   - Assigns sentiment labels based on polarity:
     - `> 0`: **Positive (1)**
     - `= 0`: **Neutral (0)**
     - `< 0`: **Negative (-1)**

2. **Model Evaluation**
   - **Accuracy Score**
   - **Classification Report** (Precision, Recall, F1-score)

## **Visualizations**
- **Sentiment Distribution**: Bar plot showing the distribution of positive, neutral, and negative reviews.
- **Word Clouds**:
  - **Positive Reviews**: Most common words in positive reviews.
  - **Negative Reviews**: Most common words in negative reviews.
- **Interactive Sentiment Trends**:
  - Uses **Plotly** to display sentiment changes over time.

## **Running Custom Input Sentiment Analysis**
You can analyze any custom review using:
```python
from sentiment_analysis import analyze_custom_review

review = "This product is amazing! I love it."
result = analyze_custom_review(review)

for key, value in result.items():
    print(f"{key}: {value}")
```

## **Output Example**
```
Original Review: This product is amazing! I love it.
Cleaned Review: this product is amazing i love it
Polarity Score: 0.75
Predicted Sentiment: Positive (1)
```

## **Future Enhancements**
- Use **Deep Learning models** for sentiment classification.
- Deploy as a **web application** with interactive user input.
- Support **multilingual sentiment analysis**.

## **Conclusion**
This project successfully performs sentiment analysis on textual data using Natural Language Processing (NLP) techniques. By leveraging TextBlob, we analyzed customer reviews, classified sentiments as Positive, Negative, or Neutral, and visualized trends using various interactive charts. The model provides valuable insights into customer opinions, helping businesses understand user feedback effectively.

For further improvements, advanced models like VADER, BERT, or custom-trained models can be explored to enhance accuracy.

