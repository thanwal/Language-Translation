# English-to-Hindi Neural Machine Translation (Seq2Seq)

A deep learning project implementing a Sequence-to-Sequence (Seq2Seq) architecture for English-to-Hindi language translation. This repository tracks the development of an Encoder-Decoder neural network built from scratch using PyTorch.

## 🚀 Project Overview
Translating between English (Subject-Verb-Object) and Hindi (Subject-Object-Verb) requires a model capable of understanding deep structural syntax. 

### Key Features
* **Architecture:** Vanilla Recurrent Neural Network (RNN) baseline.
* **Custom Data Pipeline:** Dynamic tokenization, padding, and batching using PyTorch `DataLoader`.
* **Pre-trained Embeddings:** Integrates Google News Word2Vec (300d) for English and Wiki News FastText (300d) for Hindi.
* **Experiment Tracking:** Fully integrated with **DagsHub** and **MLflow** to track hyperparameters and metrics.

## 🧠 Current State: v1.0 Vanilla RNN
The current architecture utilizes standard `nn.RNN` layers. 
* **Observation:** The model currently achieves an accuracy baseline of ~15%.
* **Diagnosis:** For sequence lengths of 30 tokens, the Vanilla RNN suffers from the Vanishing Gradient problem, causing it to lose the semantic meaning of early English words and default to high-frequency Hindi tokens. 

## 👨‍💻 Author
**Abhishek Meena**
B.Tech in Artificial Intelligence and Data Engineering  
Malaviya National Institute of Technology (MNIT), Jaipur  
[LinkedIn](https://www.linkedin.com/in/thanwal/) | [GitHub](https://github.com/thanwal)