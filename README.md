# Seq2Seq Response Generation for Emotion-Aware Chatbot

This project focuses on developing an emotion-aware chatbot: generating empathetic and contextually relevant responses using a Seq2Seq model with an LSTM-based encoder-decoder architecture. The aim is to create a conversational agent capable of producing emotionally aligned replies.

---

## **Project Overview**

The Seq2Seq model generates responses based on dialog input and optional emotion labels. By integrating emotion labels, the model improves the quality and empathy of the generated responses, making the chatbot emotionally intelligent.

---

## **Objective**

- Generate meaningful, contextually relevant responses to user input.
- Enhance response quality using emotion labels as additional context.
- Evaluate performance using advanced metrics like **BERTScore**.

---

## **Dataset**

### **Empathetic Dialogues Dataset**
- **Source**: [Kaggle Empathetic Dialogues](https://www.kaggle.com/datasets/atharvjairath/empathetic-dialogues-facebook-ai)
- **Description**: Contains over 25,000 conversation pairs designed to simulate empathetic conversations.
- **Format**:
  | **Input (Context)**            | **Output (Response)**                   | **Emotion** |
  |--------------------------------|------------------------------------------|-------------|
  | "I lost my job today."         | "I’m so sorry to hear that. Are you okay?" | Sadness     |
  | "I just got a promotion!"      | "Congratulations! You must be thrilled."  | Joy         |

### **Dataset Preprocessing**
1. **Tokenization**:
   - Splits text into words for input and output sequences.
2. **Padding**:
   - Ensures all sequences have the same length for batch processing.
3. **Emotion Labels**:
   - Emotion labels are appended to the input text for emotion-guided response generation.

---

## **Model Architecture**

### **Seq2Seq Model with LSTM**
- **Encoder**:
  - Encodes the input text into a fixed-length context vector.
- **Decoder**:
  - Generates the output response word by word using the context vector and prior predictions.

### **Features**
1. **Teacher Forcing**:
   - Speeds up training by providing the ground truth token during decoder training.
2. **Emotion Label Integration**:
   - Emotion labels guide the decoder in generating emotionally aligned responses.

---

## **Setup and Installation**

### **Prerequisites**
- **Python** (3.8 or later)
- **Libraries**:
  - PyTorch
  - NumPy
  - Pandas
  - NLTK

### **Installation**
Install the required libraries using:
```bash
pip install torch numpy pandas nltk
