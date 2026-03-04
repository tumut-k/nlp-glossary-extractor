Automated Terminology Extractor for Localization
Project Overview:
In large-scale localization projects, manually extracting terms to build a glossary is highly time-consuming. This Python script automates the initial phase of terminology extraction using Natural Language Processing (NLP).

How it works:

Takes raw text (e.g., technical or medical documents).

Uses NLTK's word_tokenize for smart tokenization.

Filters out punctuation and numbers using .isalpha().

Removes standard English stop words using the NLTK corpus.

Outputs a frequency dictionary of meaningful terms to be reviewed by the linguist.

Next Steps: Future versions will include Lemmatization (grouping "know" and "knows") and bilingual mapping.
