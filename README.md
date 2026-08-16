# 📊 Social Media Analytics — Capstone Project

A Python data-analysis project that parses and analyzes social media messages, including tweets and Facebook posts, made by United States politicians in 2013. The project extracts poster information such as name, position, state, and region, along with hashtags and message sentiment. The enriched dataset is then used to analyze politicians, hashtags, and sentiment patterns.

## ✨ Features

### Phase 1 — Data Organization

* Parse poster labels into structured **name, position, and state** fields
* Map each state to its corresponding US region
* Extract hashtags from social media messages
* Perform **VADER sentiment analysis** on each message
* Classify messages as **positive, negative, or neutral**
* Add the extracted information and sentiment results as new columns to the dataset

### Phase 2 — Deeper Analysis

* Calculate sentiment score quantiles such as **minimum, 25%, 50%, 75%, and maximum**
* Get hashtags used by a filtered group such as a state or politician
* Count the frequency of hashtags across the dataset
* Find the most commonly used hashtags
* Calculate the average sentiment associated with a specific hashtag

## 🗂️ Project Structure

```text
.
├── social.py
├── social_tests.py
└── data/
    ├── politicaldata.csv
    └── statemappings.csv
```

### File Description

* `social.py` — Main implementation containing the project functions
* `social_tests.py` — Test suite used to validate the functions
* `data/politicaldata.csv` — Raw social media dataset
* `data/statemappings.csv` — State-to-region lookup table

## 🛠️ Technologies Used

* Python
* Pandas
* NLTK
* VADER Sentiment Analysis

## 🛠️ Requirements

* Python 3.x
* pandas
* nltk

### Install Dependencies

```bash
pip install pandas nltk
```

The VADER sentiment lexicon is downloaded automatically when the script runs:

```python
nltk.download('vader_lexicon', quiet=True)
```

## ▶️ Usage

Run the main Python file:

```bash
python social.py
```

The project runs the test cases and executes the implemented analysis functions.

## 🧩 Key Functions

| Function                                             | Description                                                                |
| ---------------------------------------------------- | -------------------------------------------------------------------------- |
| `parse_label(label)`                                 | Extracts name, position, and state from a poster label                     |
| `get_region_from_state(state_df, state)`             | Maps a state to its US region                                              |
| `find_hashtags(message)`                             | Extracts hashtags from a message                                           |
| `find_sentiment(classifier, message)`                | Returns sentiment score and category                                       |
| `add_columns(data, state_df)`                        | Adds name, position, state, region, hashtags, score, and sentiment columns |
| `get_sentiment_quantiles(data, col_name, col_value)` | Calculates sentiment score distribution                                    |
| `get_hashtag_subset(data, col_name, col_value)`      | Gets hashtags used by a filtered group                                     |
| `get_hashtag_rates(data)`                            | Counts hashtag usage across the dataset                                    |
| `most_common_hashtags(hashtags, count)`              | Finds the top N most-used hashtags                                         |
| `get_hashtag_sentiment(data, hashtag)`               | Calculates sentiment associated with a hashtag                             |

These functions are implemented in the project code.

## 📊 Example Insights

The project can identify frequently used hashtags and analyze their sentiment.

Example results:

```text
Top Hashtags:

#Obamacare  - 61 uses, avg sentiment: negative
#IRS        - 26 uses, avg sentiment: negative
#jobs       - 20 uses, avg sentiment: positive
#SOTU       - 20 uses, avg sentiment: neutral
```

These results demonstrate how hashtag frequency and sentiment can be used to understand topics discussed in social media posts.

## 📚 Skills Gained

Through this project, I developed practical skills in:

* **Data Analysis** — Analyzing and filtering data using Pandas
* **Sentiment Analysis** — Using NLTK VADER to classify social media posts
* **Text Processing** — Extracting hashtags from social media messages
* **Data Transformation** — Converting raw data into structured information
* **Data Filtering** — Analyzing data based on politicians, states, regions, and hashtags
* **Python Programming** — Working with functions, strings, lists, dictionaries, and sets
* **Problem Solving** — Building functions to process data and generate useful insights
* **Testing and Debugging** — Using test cases to validate project functions

This project helped me improve my **Python, Data Analysis, Sentiment Analysis, Text Processing, and Problem-Solving skills** through practical experience.

## 📌 Data Source

The dataset contains social media posts made by US politicians in 2013 and was sourced from Kaggle for this capstone project.

## 📝 Conclusion

This project demonstrates how **Python, Pandas, and NLTK VADER** can be used to process and analyze social media data.

By extracting politician information, hashtags, regions, and sentiment, the project provides useful insights into social media content and hashtag trends.

It was a valuable hands-on project for developing practical skills in **Data Analysis, Python Programming, Sentiment Analysis, Text Processing, and Problem Solving**.
