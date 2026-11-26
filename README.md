[Decoding Emotions in Literature - NLP and Deep Learning Approaches.pptx](https://github.com/user-attachments/files/35466227/Decoding.Emotions.in.Literature.-.NLP.and.Deep.Learning.Approaches.pptx)
# Decoding Emotions in Literature: NLP and Deep Learning Approaches

An NLP framework that detects nuanced, overlapping emotions in literary text using **DistilBERT** and **sliding window segmentation**, and visualizes how emotions change across a text.

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" />
  <img src="https://img.shields.io/badge/NLP-FECC00?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Deep%20Learning-FF6F00?style=for-the-badge" />
</p>

## 📖 Overview

Literary emotion detection aims to capture and analyze emotional expression in novels, poems and other literary text. Literature relies on figurative language, metaphors and symbolism, which makes this hard. This project uses DistilBERT's contextual embeddings to interpret those cues, and a sliding window to track emotional transitions across consecutive segments of text.

**Application areas:** literary analysis, AI-driven storytelling and digital humanities.

## ❗ Problem Statement

- **Challenge:** Traditional models struggle with contextual and figurative language in literature.
- **Limitation:** Existing systems fail to detect subtle and overlapping emotions.
- **Need:** An improved deep learning approach for accurate emotion classification in complex texts.

## 🎯 Aim

- Develop an NLP framework for detecting nuanced emotions in literature.
- Implement DistilBERT for **multi-label** emotion classification.
- Use **sliding window segmentation** for dynamic emotion tracking.
- Compare lexicon-based and transformer-based approaches.

## ✨ Key Features

- **DistilBERT model**, pre-trained on GoEmotions, generating contextual embeddings
- **Sliding window segmentation** over overlapping text segments to track emotional transitions
- **Multi-label classification** that predicts several emotions per segment, with probability scores
- **Visualizations**: heatmaps and line graphs of emotional intensity across the text

## 🔍 Existing vs Proposed System

| Method (existing) | Description | Limitation |
|---|---|---|
| Lexicon-based | Predefined word-emotion mappings (NRC Emotion Lexicon) | Relies on fixed word lists |
| Traditional ML | Naive Bayes, SVM with handcrafted features | Ineffective for complex literary texts |
| Deep learning | BERT, DistilBERT contextual embeddings | Struggles with sarcasm and ambiguity |

| Feature | Existing systems | Proposed (DistilBERT + sliding window) |
|---|---|---|
| Model | BERT: accurate but large, slow and resource-heavy | DistilBERT: smaller and faster, with 97% of BERT's performance |
| Inference speed | Slower, high memory usage, needs GPUs | Faster, lower memory, suited to real-time analysis |
| Emotion detection | Whole-text (static) analysis | Overlapping windows capture emotion shifts |
| Granularity | Whole document or sentence, misses subtle shifts | Fine-grained, chunk-level emotion dynamics |
| Visualization | Typically static | Line plots and heatmaps showing emotional evolution |
| Target use case | Social media, reviews, customer feedback | Literary texts such as poetry, where emotions evolve |

## ⚙️ Methodology

| Stage | Process |
|---|---|
| 1. Text preprocessing | Tokenization and stopword removal |
| 2. Feature extraction | DistilBERT contextual embeddings |
| 3. Sliding window | Overlapping windows to track emotion shifts |
| 4. Emotion classification | Multi-label detection with probability scores |
| 5. Visualization | Heatmaps and line graphs of emotional intensity |

### Model Architecture

![Model Architecture](images/model-architecture.png)

### Workflow

![Workflow Diagram](images/workflow.png)

## 🧠 Model Selection

The project uses `joeddav/distilbert-base-uncased-go-emotions-student` from Hugging Face, a DistilBERT model pre-trained for emotion classification on GoEmotions.

| Feature | BERT | DistilBERT |
|---|---|---|
| Size | 110M parameters (base) | 60% smaller (66M parameters) |
| Speed | Slower | Faster inference and training |
| Performance | State-of-the-art on many tasks | 97% of BERT's performance |
| Memory | High | Lower |
| Use case | Large-scale, high-resource settings | Real-time applications (mobile, web) |

## 📊 Experimental Results

A sample poem was processed end to end: preprocessing, sliding windows (4 overlapping windows), then classification.

- **Lexicon-based result:** positive
- **Transformer-based result (top emotions):**

| Emotion | Score |
|---|---|
| Remorse | 0.19 |
| Amusement | 0.17 |
| Excitement | 0.17 |
| Joy | 0.16 |
| Love | 0.11 |
| Grief | 0.10 |
| Pride | 0.08 |
| Caring | 0.08 |
| Relief | 0.07 |

The lexicon method returns one label, while the transformer shows a mix of overlapping emotions, which matches the bittersweet tone of the text.

![Emotion visualization](images/results-1.png)
![Emotion trend](images/results-2.png)

## 🚀 Future Enhancements

| Enhancement | Description |
|---|---|
| Multi-modal data integration | Incorporate audiobooks for richer insights |
| Model fine-tuning | Train on larger literary datasets for better accuracy |
| Sarcasm and irony detection | Improve interpretation of figurative language |
| Interactive visualization | Dynamic visualizations for real-time analysis |

## ✅ Conclusion

DistilBERT with sliding window segmentation detects emotional transitions in literary text. Contextual embeddings improve accuracy over lexicon-based methods, multi-label classification captures overlapping emotions, and the visualizations give interpretable insight for literary analysis.

## 💻 How to Run

```bash
git clone https://github.com/Ramyaanbazhagan/Decoding-Emotions-in-Literature.git
cd Decoding-Emotions-in-Literature
# [Add your install command, e.g. pip install -r requirements.txt]
# [Add your run command, e.g. python main.py or the notebook name]
```

## 📚 References

1. A. Koufakou, J. Garciga, A. Paul, J. Morelli and C. Frank, "Automatically Classifying Emotions based on Text: A Comparative Exploration of Different Datasets," arXiv, 2023. doi: 10.48550/ARXIV.2302.14727
2. P. Patel, D. Patel, D. Patel and M. Bera, "Emotion Detection in Text: A Deep Learning Approach for Sentiment Analysis," vol. 8, no. 10, 2023.
3. F. Safari and A. Chalechale, "Emotion and personality analysis and detection using natural language processing, advances, challenges and future scope," *Artif. Intell. Rev.*, vol. 56, no. S3, pp. 3273–3297, Dec. 2023. doi: 10.1007/s10462-023-10603-3
4. K. Machová, M. Szabóova, J. Paralič and J. Mičko, "Detection of emotion by text analysis using machine learning," *Front. Psychol.*, vol. 14, p. 1190326, Sep. 2023. doi: 10.3389/fpsyg.2023.1190326

## 👩‍💻 Author

**A.K. Ramya** · [LinkedIn](https://linkedin.com/in/ramya-anbu) · [Portfolio](https://ramyaanbazhagan.github.io/portfolio/)
