# Automated Terminology Extractor for Localization (v2.0)

**Project Overview:**
In large-scale localization projects, manually extracting terms to build a glossary is highly time-consuming. This Python script automates the initial phase of terminology extraction using Natural Language Processing (NLP).

**Version 2.0 Updates:**
* **POS Tagging:** Integrates NLTK's `averaged_perceptron_tagger` to identify the grammatical category of each word in context.
* **Lemmatization:** Uses WordNet to reduce words to their dictionary roots (e.g., successfully merging "know" and "knows" into the lemma "know").

**How it works:**
1. Takes raw text (e.g., technical or medical documents).
2. Uses `NLTK`'s `word_tokenize` for smart tokenization.
3. Tags each token with its Part-of-Speech (POS) to preserve grammatical context.
4. Filters out punctuation and numbers using `.isalpha()`.
5. Removes standard English stop words using the `NLTK` corpus.
6. Lemmatizes the remaining words based on their POS tags.
7. Outputs a frequency dictionary of base terms to be reviewed by the linguist.

## How to Run
1. Clone the repo: `git clone https://github.com/tumut-k/nlp-glossary-extractor`
2. Install dependency: `pip install nltk`
3. Open `term_extractor.ipynb` in Google Colab or Jupyter
4. Paste your source text into the `source_text` variable
5. Run all cells

**Linguistic Insights & Next Steps:**
While effective, the rule-based POS tagger occasionally struggles with structural ambiguity. For example, it mistakenly tagged the noun "meaning" (in "is about meaning") as a verb due to the "-ing" suffix, reducing it to "mean". Future versions will explore Transformer-based models (like spaCy or Hugging Face) to resolve these contextual ambiguities and implement bilingual mapping.

## About
Built by Talha Umut Kulu, a professional translator (500,000+ words across 
medical, legal and technical domains) currently transitioning into NLP. 
This tool grew out of real localization workflows at node101 and freelance 
projects where manual glossary building was a bottleneck.

GitHub: https://github.com/tumut-k  
LinkedIn: https://linkedin.com/in/tumutk
