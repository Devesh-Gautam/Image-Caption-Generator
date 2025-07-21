# 🖼️ Image Caption Generator

This project implements a **branchial neural network** for generating natural language captions for images. It combines **deep visual features** extracted from a pretrained **Xception CNN** and sequential **LSTM-based language modeling** to predict captions, trained on the **Flickr8k** dataset.

---

## 🔧 Features

- 🔍 **Branchial architecture** using image and text inputs
- 🧠 **Xception CNN** for image feature extraction via transfer learning
- ✍️ **LSTM** model for language modeling from partial captions
- 🔄 **Custom data generators** to handle large datasets efficiently
- 🔤 **NLP preprocessing** and **Keras Tokenizer** for text processing
- 📊 Evaluated using **BLEU score** for caption quality

---

## 📁 Dataset

- **Dataset used**: [Flickr8k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr8k)
- Contains **8000 images** with **5 captions each**
- Download and extract images and `Flickr8k.token.txt` file

---

## 🧠 Model Architecture

- **Image Input Branch**:  
  `2048-dim feature vector` from pretrained **Xception** → Dense layer (256 units)

- **Text Input Branch**:  
  `Text sequence` → Embedding layer → LSTM (256 units)

- **Fusion**:  
  Merged both branches → Dense layer → Softmax over vocabulary

- Implemented using **Keras Functional API**

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/image-caption-generator.git
cd image-caption-generator
pip install -r requirements.txt
