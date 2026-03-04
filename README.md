# Automated Terminology Extractor for Localization (v2.0)

**Project Overview:**
In large-scale localization projects, manually extracting terms to build a glossary is highly time-consuming. This Python script automates the initial phase of terminology extraction using Natural Language Processing (NLP).

**Version 2.0 Updates:**
* **POS Tagging:** Integrates NLTK's `averaged_perceptron_tagger` to identify the grammatical category of each word in context.
* **Lemmatization:** Uses WordNet to reduce words to their dictionary roots (e.g., successfully merging "know" and "knows" into "know").

**How it works:**
1. Takes raw text (e.g., technical documents).
2. Uses `NLTK`'s `word_tokenize` for smart tokenization.
3. Tags each token with its Part-of-Speech (POS) to preserve grammatical context.
4. Filters out punctuation and numbers using `.isalpha()`.
5. Removes standard English stop words using the `NLTK` corpus.
6. Lemmatizes the remaining words based on their POS tags.
7. Outputs a frequency dictionary of base terms to be reviewed by the linguist.

**Linguistic Insights & Next Steps:** While effective, the basic POS tagger sometimes struggles with structural ambiguity (e.g., mistakenly tagging the noun "meaning" as a verb in certain contexts, reducing it to "mean"). Future versions will explore Transformer-based models (like spaCy or Hugging Face) for better contextual accuracy and bilingual mapping.
