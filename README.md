# 🧠 Next Word Prediction using LSTM

This project demonstrates how to build a deep learning model that predicts the next word in a sentence using a Long Short-Term Memory (LSTM) network. The training text is taken from the classic literary novel *War and Peace* by Leo Tolstoy.

---

## 📚 Objective

To train a neural network to understand and predict the next word in a given sequence of words using natural language processing techniques and sequence modeling.

---

## 🗂️ Dataset

- **Source**: A manually defined text excerpt (from *War and Peace*) stored as a string variable.
- **Size**: Small-scale dataset containing about 1600+ sequences.
- **Processing**: Tokenized using `Tokenizer()` from Keras and padded to ensure uniform input length.

---

## 🔑 Key Features

### ✅ Text Preprocessing
- Word tokenization using Keras `Tokenizer`
- Word-to-index dictionary creation
- Input sequences generated as n-gram chains
- Zero-padding applied to standardize sequence lengths

### ✅ Model Architecture
- **Embedding Layer**: Converts words to dense vector representations
- **LSTM Layer**: Captures sequence dependencies and context
- **Dense Output Layer**: Uses softmax activation to classify the next word

```python
model = Sequential()
model.add(Embedding(vocab_size, 100, input_length=X.shape[1]))
model.add(LSTM(150))
model.add(Dense(vocab_size, activation='softmax'))
