# COH-PIAH Detector

## Overview
The COH-PIAH Detector is a Python program that analyzes text samples to identify potential cases of COH-PIAH infection based on linguistic patterns. It uses various text metrics to compare writing styles and determine similarities between texts.

## Features
The program analyzes texts using six main linguistic traits:
- Average word length
- Type-Token ratio (lexical diversity)
- Hapax Legomana ratio (proportion of words used only once)
- Average sentence length
- Sentence complexity
- Average phrase length

## How it Works
1. The program first collects a baseline signature of linguistic traits from a known infected text
2. Users can then submit multiple texts for analysis
3. Each text is broken down into its linguistic components (sentences, phrases, words)
4. The program calculates a similarity score between each submitted text and the baseline
5. The text with the closest match to the infected signature is identified as potentially infected

## Functions

### Main Components:
- `le_assinatura()`: Collects the baseline linguistic signature
- `le_textos()`: Reads multiple texts for comparison
- `calcula_assinatura()`: Calculates the linguistic signature of a given text
- `compara_assinatura()`: Compares two linguistic signatures
- `avalia_textos()`: Evaluates multiple texts and identifies the most likely infected one

### Text Processing Functions:
- `separa_sentencas()`: Splits text into sentences
- `separa_frases()`: Splits sentences into phrases
- `separa_palavras()`: Splits phrases into words
- `n_palavras_unicas()`: Counts words that appear only once
- `n_palavras_diferentes()`: Counts unique words

## Usage
1. Run the program
2. Enter the baseline linguistic traits when prompted
3. Input the texts you want to analyze
4. The program will output which text is most likely infected with COH-PIAH

Example:
```python
python coh_piah_detector.py
```

## Requirements
- Python 3.x
- re (Regular Expression) module

## Technical Details
The program uses regular expressions for text processing and implements various linguistic analysis algorithms. It calculates similarity scores using the average absolute difference between linguistic traits.

## Notes
- All text analysis is case-insensitive
- The program handles various punctuation marks (., !, ?, :, ;, ,) for sentence and phrase separation
- Empty strings and trailing spaces are properly handled

## Contributing
Feel free to submit issues and enhancement requests. The main area marked with comments ("Não mexer daqui para cima") should not be modified as it contains core functionality.
