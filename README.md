
This project implements a **hybrid log classification system**, combining three complementary approaches to handle varying levels of complexity in log patterns. This design ensures flexibility and effectiveness in processing **predictable**, **complex**, and **low-data** scenarios.

---

## 🧠 Classification Approaches

### 1. ✅ Regular Expression (Regex)
- Best for **simplified and predictable patterns**
- Fast and efficient using predefined rules
- Example: Detecting known error messages

### 2. 🤖 Sentence Transformer + Logistic Regression
- Suitable for **complex patterns** with enough training data
- Embeddings from `sentence-transformers` + classification using Logistic Regression
- Helps when regex isn’t expressive enough

### 3. 💡 LLM (Large Language Models)
- Ideal for **ambiguous patterns** or **low-data scenarios**
- Acts as a **fallback** or complementary classifier
- Great for generalization and nuanced understanding


![arch](https://github.com/user-attachments/assets/453a59ee-2218-43df-8066-596272dad6d1)

log-classification/
├── classify.py
├── main.py
├── processor_regex.py
├── processor_bert.py
├── processor_llm.py
├── server.py
├── requirements.txt
├── .gitignore
├── training/
│   ├── dataset/
│   └── training.ipynb
├── models/
├── resources/
│   ├── test.csv
│   └── output.csv
└── .env (not included in repo)


