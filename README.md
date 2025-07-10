# Image Captioning with ResNet50 and Hybrid LSTM–GRU using Beam Search

Course Project – Neural Networks and Deep Learning, MSc in Artificial Intelligence  
University of Tehran, July 2025  
Supervisor: Dr. Ahmad Kalhor

This project reproduces and extends a deep learning model for automatic image captioning based on a 2025 publication in *Automatika Journal*. The system combines a ResNet50 encoder for visual feature extraction with a hybrid LSTM–GRU decoder, and utilizes beam search to improve caption generation.

## 📚 Summary
- **Architecture**: ResNet50 encoder + Hybrid LSTM–GRU decoder
- **Dataset**: Flickr8k (from Kaggle), 8,000+ images with 5 human-generated captions each
- **Search Strategy**: Beam Search (beam width = 5) vs. Greedy Search
- **Evaluation**: BLEU scores, accuracy, and loss
- **Best Result**: BLEU-4 score of 0.6034, accuracy of 89.3%, and loss of 0.4013

## ⚙️ Techniques Used
- Transfer learning with ResNet50
- Hybrid decoder combining strengths of LSTM and GRU
- Caption generation using Beam Search for improved sequence quality
- Tokenization, padding, and preprocessing of both text and image data
- Comparative evaluation with alternative CNN encoders and RNN decoders

## 📊 Results
| Model               | Accuracy | Loss   | BLEU-4 |
|--------------------|----------|--------|--------|
| ResNet50 + LSTM    | 84.6%    | 0.596  | 0.45   |
| ResNet50 + GRU     | 85.2%    | 0.512  | 0.49   |
| **ResNet50 + Hybrid LSTM–GRU + Beam Search** | **89.3%** | **0.401** | **0.6034** |

## 💻 Tools & Libraries
- Python, TensorFlow, Keras
- NumPy, NLTK, Scikit-learn, Matplotlib
- Google Colab for GPU training

## 📁 Structure
- `ResNet50+LSTM.ipynb`: Full training, evaluation, and caption generation notebook
- `data/`: Dataset preprocessing and caption tokenization
- `utils/`: BLEU scoring and beam search functions

---

### 📜 Reference
Kavitha, P. V., & Karpagam, V. (2025). *Image captioning deep learning model using ResNet50 encoder and hybrid LSTM–GRU decoder optimized with beam search*. *Automatika*, 66(3), 394–410. DOI: [10.1080/00051144.2025.2485695](https://doi.org/10.1080/00051144.2025.2485695)
