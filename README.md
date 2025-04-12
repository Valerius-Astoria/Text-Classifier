# Text-Classifier

### ❓ What is this?

This is a simple Python-based authorship classifier that estimates the probability that a given piece of text was written by **Author A** or **Author B**.

It uses a Naive Bayes-inspired approach based on **word frequency analysis**. You provide:
- Two known writing samples (`text_A.txt` and `text_B.txt`)
- One unknown text sample (`text.txt`)
- Your prior belief (e.g., 0.5 if unsure)

The script then calculates the likelihood of the text under each author's word distribution and uses **Bayes’ Theorem** to return a probability score.

It’s lightweight, educational, and perfect for exploring basic natural language processing concepts like tokenization, smoothing, and probabilistic inference.

---

### ❓ How to use it ?

1.	Replace the contents of text_A.txt with a sample written by Author A
2.	Replace the contents of text_B.txt with a sample written by Author B
3.	Replace the contents of text.txt with the unknown text you want to classify

Then simply run test.ipynb. The notebook will ask you to enter your prior belief (e.g., how likely you think the text is written by A — enter 0.5 if you’re unsure).
📊 The model will then return the probabilities that the text was written by Author A and Author B, respectively.

