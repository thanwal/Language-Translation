# English-to-Hindi Neural Machine Translation (Seq2Seq)

A deep learning project implementing a Sequence-to-Sequence (Seq2Seq) architecture for English-to-Hindi language translation. This repository tracks the evolution of an NMT model from basic RNNs to sophisticated Transformers.

## 🚀 Project Overview
Translating between English (SVO) and Hindi (SOV) requires a model capable of handling long-range dependencies and structural reordering. This project explores the transition from simple recurrent units to gated architectures and attention mechanisms.

### Key Features
* **Architecture:** Encoder-Decoder framework with LSTM and Attention support.
* **Data Engineering:** Custom punctuation-safe regex cleaning and length-based outlier filtering (max_threshold=28).
* **Embeddings:** Domain-specific pre-trained embeddings (Word2Vec for English, FastText for Hindi).
* **Infrastructure:** Trained on AWS EC2/SageMaker using NVIDIA Tesla T4 (G4dn) instances.
* **Experiment Tracking:** Integrated with **MLflow** and **DagsHub** for metric logging and model versioning.

---

## 🏗️ Version History

### v1.1: Long Short-Term Memory (LSTM) - [Current Main]
* **Upgrade:** Replaced `nn.RNN` with `nn.LSTM` to mitigate vanishing gradients.
* **Architecture:** - `hidden_dim`: 512
  - `num_layers`: 2
  - `dropout`: 0.4
* **Performance:** - **Val Acc:** ~38%
* **Key Learning:** Implementing **Teacher Forcing Decay (TRF=0.5)** significantly improved the model's ability to generate independent Hindi syntax.

### v1.0: Vanilla RNN Baseline
* **Accuracy:** ~15%
* **Limitation:** Significant semantic loss in sequences >15 tokens due to vanishing gradient issues.


## 👨‍💻 Author
**Abhishek Meena**
B.Tech in Artificial Intelligence and Data Engineering  
Malaviya National Institute of Technology (MNIT), Jaipur  
[LinkedIn](https://www.linkedin.com/in/thanwal/) | [GitHub](https://github.com/thanwal)