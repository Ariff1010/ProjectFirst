# CSC649 Setup & Word Count Tool

## Description
This program is a simple text analysis tool written in Python. It accepts an input sentence from the user, validates whether the input is empty, and calculates both the total word count and total character count (including spaces).

## How to Run
1. Open the project in **PyCharm**.
2. Ensure the project interpreter is set to **Python 3.12** inside the `.venv` virtual environment.
3. Open `main.py`.
4. Right-click inside `main.py` and select **Run 'main'** (or run `python main.py` in the terminal).
5. Enter a sentence when prompted and press Enter.

## Test Results

| Test Case | Input | Expected Output | Actual Output | Status |
| :--- | :--- | :--- | :--- | :--- |
| **1. Normal Sentence** | `Hello world this is CSC649.` | Words: 5<br>Characters: 26 | Word count: 5<br>Character count (including spaces): 26 | Pass |
| **2. Empty Input** | *(Pressed Enter directly)* | `You did not enter a sentence.` | `You did not enter a sentence.` | Pass |
| **3. Extra Spaces** | `  Python   3.12   is   great!  ` | Words: 4<br>Characters: 31 | Word count: 4<br>Character count (including spaces): 31 | Pass |

## Limitations
* **Punctuation Handling**: The `len(sentence.split())` method splits words based on whitespace alone. As a result, attached punctuation (e.g., `"world!"` or `"end."`) is treated as part of the word rather than being stripped out or counted separately.