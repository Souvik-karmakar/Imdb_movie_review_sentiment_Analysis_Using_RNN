# 🎬 IMDb Movie Review Sentiment Analysis using Simple RNN

This project performs **sentiment analysis on IMDb movie reviews**, classifying them as **Positive** or **Negative** using **Natural Language Processing (NLP)** and a **Simple Recurrent Neural Network (RNN)**.  
The trained model is deployed as an **interactive Streamlit web application** for real-time predictions.

🌐 **Live App**  
👉 https://imdbmoviereviewsentimentanalysisusingrnn-n8zjsbkpnukjfkamapfdm.streamlit.app/

---

## 📌 Problem Statement
Understanding audience sentiment from movie reviews is crucial for the film industry.  
This project aims to automatically analyze IMDb reviews and predict whether the sentiment expressed is **positive or negative**.

---

## 📊 Dataset
- **IMDb Movie Reviews Dataset**
- 50,000 total reviews  
  - 25,000 training samples  
  - 25,000 testing samples
- Labels:
  - `1` → Positive  
  - `0` → Negative  

---

## ⚙️ Data Preprocessing
- Limited vocabulary to **10,000 most frequent words**
- Converted text reviews into integer sequences
- Applied **padding** to ensure uniform length (`max_len = 500`)
- Used IMDb word index for token mapping
- Preprocessed user input with the same pipeline for prediction

---

## 🧠 Model Architecture (Simple RNN)
- **Embedding Layer** (128 dimensions)
- **Simple RNN Layer** (128 units, ReLU activation)
- **Dense Output Layer** (1 neuron, Sigmoid activation)

### Model Configuration
- Optimizer: Adam  
- Loss Function: Binary Crossentropy  
- Metric: Accuracy  
- Early Stopping applied to prevent overfitting  

---

## 🚀 Model Training
- Batch Size: 32  
- Epochs: Up to 10  
- Validation Split: 20%  
- EarlyStopping monitored on validation loss (patience = 5)

---

## 🔍 Prediction Workflow
1. User enters a movie review
2. Review is tokenized and padded
3. Processed text is passed to the trained RNN model
4. Model outputs:
   - **Sentiment**: Positive / Negative  
   - **Confidence Score**

---

## 🌐 Streamlit Web Application
The application allows users to:
- Enter custom IMDb movie reviews
- Get instant sentiment predictions
- View prediction confidence in real time

🔗 **App Glimpse**  
👉 https://imdbmoviereviewsentimentanalysisusingrnn-n8zjsbkpnukjfkamapfdm.streamlit.app/

---

## 🛠️ Tech Stack
- Python  
- TensorFlow / Keras  
- NumPy  
- NLP  
- Streamlit  

---

## ▶️ Run Locally
```bash
git clone https://github.com/your-username/imdb-movie-review-sentiment-analysis-rnn.git
cd imdb-movie-review-sentiment-analysis-rnn
pip install -r requirements.txt
streamlit run main.py
