# 🐦 Twitter Sentiment Analysis using PyTorch (LSTM)

### 🔍 Project Overview
This project performs **Sentiment Analysis** on tweets — classifying them as **Positive 😀** or **Negative 😞**.  
It uses **Natural Language Processing (NLP)** techniques and a **PyTorch LSTM model** to understand the emotional tone of text.

---


1. **Data Cleaning**
   - Removed URLs, mentions (`@user`), numbers, and special characters  
   - Lowercased all text and removed English stopwords  


2. **Tokenization & Vocabulary**
   - Each word is converted into an integer (token)
   - Top 10,000 most frequent words were used
   - Added `<pad>` and `<unk>` tokens

3. **Dataset & DataLoader**
   - Tweets were grouped into mini-batches using PyTorch’s `DataLoader`
   - Balanced Positive and Negative samples

4. **Model Architecture**
   - Embedding layer → LSTM (2 layers) → Fully connected → Sigmoid  
   - Binary output: `0` = Negative, `1` = Positive  
   - Loss: `BCEWithLogitsLoss`  
   - Optimizer: `Adam`

5. **Training**
Epoch 1, Loss: 0.6349

Epoch 2, Loss: 0.4694

Epoch 3, Loss: 0.3639

Epoch 4, Loss: 0.2901

Epoch 5, Loss: 0.2498

Epoch 6, Loss: 0.1985

Epoch 7, Loss: 0.1732

Epoch 8, Loss: 0.1416

Epoch 9, Loss: 0.1279

Epoch 10, Loss: 0.1245

7. **Prediction**


predict("i really love it")

predict("it is ok")

predict("it is wonderful")

predict("i do not like because it is awful")

predict("it is bad")

# Results

Probability: 0.94, Label: positive 😀

Probability: 0.55, Label: positive 😀

Probability: 0.59, Label: positive 😀

Probability: 0.21, Label: negative 😞

Probability: 0.43, Label: negative 😞
