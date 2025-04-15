# 📄 What Does It Do?

This is a simple text classification model based on the **Multinomial Distribution** and **Bayes' Theorem**. It estimates the probability that a given article was written by **Author A** or **Author B**.

---

# ⚙️ How It Works

### 🧾 Inputs

The model takes **three inputs**:

- `text_A.txt`: Sample text(s) known to be written by Author A  
- `text_B.txt`: Sample text(s) known to be written by Author B  
- `text.txt`: The unknown article to classify

You will also be asked to input your **prior belief** \( P(A) \) — i.e., how likely you think the article is written by A (enter `0.5` if you're unsure).

---

### 🎲 Random Variables

- **A**: The author is A  
- **B**: The author is B  
- **T**: The text is the one we want to classify

---

### 📐 Core Equation

We compute the posterior odds ratio:

$$
\frac{P(A \mid T)}{P(B \mid T)} = \frac{P(T \mid A)}{P(T \mid B)} \cdot \frac{P(A)}{P(B)}
$$

Assuming a multinomial distribution for the text, we approximate:

$$
\frac{P(T \mid A)}{P(T \mid B)} =
\frac{{p_1}^{c_1} \cdot {p_2}^{c_2} \cdots {p_m}^{c_m}}{{q_1}^{c_1} \cdot {q_2}^{c_2} \cdots {q_m}^{c_m}}
$$

Where:
$p_i$: probability of word $i$ in Author A’s texts  
$q_i$: probability of word $i$ in Author B’s texts  
$c_i$: count of word $$ in the unknown text

---

### 🛡️ Handling Zero Probabilities

If any $p_i$ or $q_i$ equals zero, the ratio breaks (division by zero or log of zero).  
To avoid this, we apply **Laplace smoothing** — replacing zeros with a small constant $\epsilon$.

