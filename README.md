# 🤖 Spam SMS Detection with spaCy

This repository provides a pre-trained [spaCy](https://spacy.io/) NLP model to classify SMS messages as **spam** or **ham** (not spam). The trained model is stored in the `model-best/` directory and ready to use out of the box — no training required!


## 📦 Requirements

To run the model, install the dependencies according to spaCy's installation guide.

Most likely you would be running :

```bash
pip install spacy
```


## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/BMDarkLight/SMS-Spam-Detector.git
cd SMS-Spam-Detector
```

### 2. Load the Model in Python

You can use the model directly with `spaCy` in a python script:

```python
import spacy

# Load the trained model
nlp = spacy.load("model")

# Test it on a sample message
text = "Congratulations! You've won a free cruise. Reply WIN to claim now!"
doc = nlp(text)

# Print classification results
print("Text:", text)
print("Predictions:", doc.cats)
```

## 🧠 Model Details

- **Framework**: spaCy v3+
- **Language**: English
- **Type**: Text Classification
- **Labels**: `spam`, `ham`
- **Location**: [`model/`](model/)


## 📁 Project Structure

```
SMS-Spam-Detector/
├── model-best/       # ✅ Trained spaCy model directory
├── README.md           
```

## 🙌 Acknowledgments

- Dataset used: [UCI SMS Spam Collection Dataset](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection)
- NLP framework: [spaCy](https://spacy.io/)