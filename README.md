# README: Task-04 - Data Science Internship at Prodigy InfoTech

## Project Overview

Excited to announce the completion of Task-04 during my data science internship at Prodigy InfoTech 🚀. This project involved analyzing and visualizing sentiment patterns in social media data to understand public opinions and attitudes towards various topics or brands using Python in Jupyter Notebook.

## Table of Contents

1. [Project Description](#project-description)
2. [Technologies Used](#technologies-used)
3. [Setup and Installation](#setup-and-installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [License](#license)
7. [Contributors](#contributors)

## Project Description

Task-04 focused on sentiment analysis of social media data to uncover public opinions and attitudes. The project included data collection, preprocessing, sentiment analysis, and visualization of the results.

### Objectives

- Collect and preprocess social media data.
- Perform sentiment analysis to classify the sentiment of the data.
- Visualize sentiment patterns and trends.
- Interpret the results to gain insights into public opinions.

## Technologies Used

- **Python**: Programming language used for data manipulation, analysis, and visualization.
- **Jupyter Notebook**: Interactive computing environment for writing and running code.
- **Pandas**: Data manipulation library.
- **NumPy**: Numerical computing library.
- **NLTK**: Natural language processing library for text analysis.
- **TextBlob**: Simple library for processing textual data.
- **Matplotlib**: Visualization library for creating static plots.
- **Seaborn**: Statistical data visualization library based on Matplotlib.
- **WordCloud**: Library for generating word clouds from text data.

## Setup and Installation

### Prerequisites

Ensure you have the following software installed:

- Python (version 3.6 or higher)
- Jupyter Notebook


### Running the Notebook

1. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

2. Open the notebook file `Task-04-Sentiment-Analysis.ipynb` and run the cells sequentially.

## Usage

### Example Usage

The notebook provides a step-by-step guide on how to:

1. Load and preprocess social media data.
2. Perform sentiment analysis using TextBlob.
3. Visualize the distribution of sentiments.
4. Generate word clouds for positive and negative sentiments.
5. Interpret the results.

#### Data Collection and Preprocessing

```python
import pandas as pd

# Load dataset
data = pd.read_csv('twitter_training.csv')

# Display the first few rows of the dataset
data.head()
```

#### Sentiment Analysis

```python
from textblob import TextBlob

# Function to classify sentiment
def get_sentiment(text):
    analysis = TextBlob(text)
    if analysis.sentiment.polarity > 0:
        return 'Positive'
    elif analysis.sentiment.polarity == 0:
        return 'Neutral'
    else:
        return 'Negative'

# Apply sentiment analysis
data['sentiment'] = data['text'].apply(get_sentiment)
```

#### Visualizing Sentiment Distribution

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Plot sentiment distribution
sns.countplot(x='sentiment', data=data)
plt.title('Sentiment Distribution')
plt.xlabel('Sentiment')
plt.ylabel('Count')
plt.show()
```

## Project Structure

```
prodigy_ds_04/
├── data/
│   └── twitter_training.csv  # Sample dataset
├── images/
│   └── prodigy_ds_04.png  # Example of generated sentiment distribution plot
├── prodigy_ds_04.ipynb  # Jupyter Notebook file
└── README.md  # Project documentation
```

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contributors

**Saumya Poojari** - [saumya.poojarii7@gmail.com]
LinkedIn - https://www.linkedin.com/in/ssaumz/

Feel free to reach out with any questions or feedback!

---

Thank you for your interest in this project. Happy coding! 🚀
