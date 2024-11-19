# Amharic NLP Project

Welcome to the **Amharic NLP Project**, where we explore the fascinating world of Amharic text analysis using a combination of traditional linguistic principles and modern Python libraries. This project aims to uncover patterns, frequencies, and semantic nuances of Amharic text, providing valuable insights and tools for researchers and developers.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Features](#project-features)
   - [Remove Tags](#1-remove-tags)
   - [Tokenization](#2-tokenization)
   - [Statistical Properties](#3-statistical-properties)
   - [Analysis of Words Based on Luhn's Idea](#4-analysis-of-words-based-on-luhns-idea)
   - [Normalization](#5-normalization)
   - [Stopword Removal](#6-stopword-removal)
   - [Stemming](#7-stemming)
   - [Inverted Index](#8-inverted-index)
   - [Cosine Similarity](#9-cosine-similarity)
6. [Visualization](#visualization)
7. [Conclusion](#conclusion)
8. [Acknowledgments](#acknowledgments)

---

## Introduction

Amharic is a unique and rich language with its own challenges and opportunities in the field of Natural Language Processing (NLP). This project bridges linguistic tradition with technology by leveraging Python libraries such as:

- **NLTK** for natural language processing tasks,
- **NumPy** for efficient numerical operations,
- **BeautifulSoup** for HTML/XML parsing,
- **Matplotlib** for data visualization.

This toolkit enables detailed analysis of Amharic text, from preprocessing to similarity analysis and visualization.

---

## Features

- **HTML/XML Tag Removal:** Clean up raw text from web pages.
- **Tokenization:** Break text into individual words while retaining Amharic structure.
- **Normalization:** Standardize characters to reduce text variations.
- **Stopword Removal:** Remove common Amharic stopwords.
- **Stemming:** Reduce words to their root forms.
- **Frequency Analysis:** Visualize word frequencies using Zipf's Law and Luhn's Idea.
- **Inverted Index:** Map terms to document locations for efficient retrieval.
- **Cosine Similarity:** Quantify similarity between documents.

---

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/amharic-nlp.git
   cd amharic-nlp
   ```

2. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

   The dependencies include:

   - `nltk`
   - `beautifulsoup4`
   - `requests`
   - `matplotlib`
   - `numpy`

---

## Usage

1. **Prepare Your Dataset:**

   - Use Amharic text files or scrape content using the `remove_tags()` function.

2. **Run the Main Script:**

   - Start the preprocessing and analysis:
     ```bash
     python main.py
     ```

3. **Visualize Results:**
   - The word frequency graphs and tables are generated in the `output/` directory.

---

## Project Features

### 1. Remove Tags

Function to clean HTML/XML content:

```python
def remove_tags(url):
    ...
```

This ensures that only the text content is retained for analysis.

---

### 2. Tokenization

Tokenizes text into individual Amharic words using `nltk.tokenize`:

- Removes non-Amharic characters, symbols, and English words.
- Ensures clean and language-specific tokenization.

---

### 3. Statistical Properties

Analyzes word frequency distribution:

- Implements **Luhn's Idea**:
  - Ignores words with very high or very low frequencies.
  - Focuses on words with "middle range" frequencies for meaningful analysis.

---

### 4. Analysis of Words Based on Luhn's Idea

Significant words are determined by:

- Skipping words with frequency > 150.
- Ignoring words with frequency < 9.

---

### 5. Normalization

Standardizes Amharic characters to reduce text variations, e.g.:

- Replace "ሠ" with "ሰ".
- Replace "ሃ", "ሐ", "ሓ", and "ኅ" with "ሀ".

---

### 6. Stopword Removal

Filters out common Amharic stopwords to focus on significant words:

```python
def remove_stop_words(stemmed_words):
    ...
```

---

### 7. Stemming

Handles both special and general cases for reducing Amharic words to their root forms:

- **Special Cases:** Handles prefixes like "አስ" and suffixes like "ች".
- **General Cases:** Reduces plural forms to singular.

---

### 8. Inverted Index

Efficiently maps terms to their document locations for retrieval systems:

```python
def invert_index(preprocessed_data):
    ...
```

---

### 9. Cosine Similarity

Measures similarity between documents by:

- Converting documents to vectors.
- Calculating cosine similarity using vector dot products.

---

## Visualization

A "Function vs Rank" graph is generated to interpret word frequency patterns using Matplotlib:

```python
plt.plot(ranks, frequencies, marker='o', color='b', linestyle='-')
```

---

## Conclusion

This project is a comprehensive toolkit for analyzing Amharic text. It combines:

- Robust preprocessing techniques,
- Advanced analysis using linguistic principles, and
- Visualization for insightful interpretation.

With these tools, users can perform in-depth analysis and targeted investigations into Amharic text corpora.

---

## Acknowledgments

- **NLTK Library** for robust NLP functionalities.
- **BeautifulSoup** for parsing HTML/XML.
- **Matplotlib** for creating insightful visualizations.

For questions or suggestions, feel free to contact us at `hakensoabel@gmail.com`.

---

Thank you for exploring the **Amharic NLP Project**!
