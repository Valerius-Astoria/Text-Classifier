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

Replace the content of Text_A.txt to the artical written by author A, and Replace the content of Text_B.txt to the artical written by author B

Replace the content of Text.txt to the unknown text

Then you can run the code.

