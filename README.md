# NLP Root Word Frequency Analyzer

## 1. Project Overview

This project is a Python script designed to analyze a piece of text and identify the frequency of its root words. It's a practical tool for basic Natural Language Processing (NLP) that helps users understand the core vocabulary of a document.

The script takes any text provided by the user, processes it, and outputs a list of unique word "stems" (the core part of a word) and how many times each stem appears in the text. This is useful for tasks like keyword extraction, text summarization, and sentiment analysis.

---

## 2. Features

-   **Interactive Input**: The script prompts the user to enter their own text for analysis.
-   **Text Cleaning**: Automatically removes punctuation and converts all text to lowercase to ensure consistent analysis.
-   **Tokenization**: Breaks down the input text into individual words (tokens).
-   **Stemming**: Aggressively reduces each word to its core root or "stem" by removing prefixes and suffixes. This is excellent for grouping related words (e.g., `hating`, `hater`, `hatred` all become `hate`).
-   **Frequency Counting**: Counts the occurrences of each unique stem.
-   **Sorted Output**: Displays the results in a clean, sorted list, from the most frequent stem to the least frequent.

---

## 3. How It Works: Key Concepts

This script uses two fundamental NLP techniques:

1.  **Tokenization**: The process of splitting a large block of text into smaller units, such as sentences or, in our case, individual words. This is the first step in almost any NLP task.

2.  **Stemming**: A process that chops off the ends (and sometimes beginnings) of words to get to a common base or "stem". The goal is to group related words. For example, `love`, `loving`, `lovable`, and `loves` all get reduced to the stem `love`.

    **Important Note**: A stemmer follows aggressive rules and does not care if the resulting stem is a real dictionary word. For instance, `unstructured` might become `unstructur`. This is expected behavior, as its only goal is to ensure all variations map to the same unique identifier.

---

## 4. Prerequisites & Setup

To run this script, you will need:

-   **Python 3.x** installed on your system.
-   **Jupyter Notebook** (recommended for interactive use) or any Python environment.
-   The **NLTK** (Natural Language Toolkit) library.

You can install NLTK using pip:
```bash
pip install nltk

5. How to Run the Script
Open Jupyter Notebook: Launch Jupyter Notebook on your computer.

Create a New Notebook: Create a new Python 3 notebook file.

Copy the Code: Copy the entire Python script from nlp_word_frequency_stemming.py and paste it into a single cell in your notebook.

Run the Cell: Execute the cell by pressing Shift + Enter.

Download Resources (First Time Only): The first time you run the script, it will automatically download the necessary NLTK data packages (punkt). You will see a message confirming the resources are ready.

Provide Input: An input box will appear below the cell with the prompt: Please paste the text you want to analyze below and press Enter.

Paste Your Text: Paste the text you wish to analyze into the box and press Enter.

View the Output: The script will immediately process the text and display the list of stemmed words and their frequencies directly below the input box.

6. Example Output
If you provide the input:
"The disagreeable hater's deep-seated hatred was not well understood..."

The output will look something like this, grouping related words under a common stem:

--- Stemmed Word Frequencies ---
Found 35 unique word stems.

- 'the': 4
- 'hate': 3
- 'love': 3
- 'understand': 3
- 'agreeabl': 2
...and so on.
