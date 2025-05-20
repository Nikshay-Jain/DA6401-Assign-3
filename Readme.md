# DA6401 Assignment 3: Sequence-to-Sequence Transliteration with Attention
## Nikshay Jain | MM21B044
## Overview

This project explores the task of character-level transliteration using sequence-to-sequence models. It is based on the Dakshina dataset by Google and aims to map romanized text (e.g., "ghar") to native Devanagari script (e.g., "घर"). We experiment with multiple RNN architectures including vanilla RNNs, GRUs, and LSTMs, and further enhance performance using attention mechanisms.

---

## Objectives

- Implement a flexible RNN-based encoder-decoder model.
- Tune hyperparameters using Weights & Biases (wandb) sweeps.
- Evaluate performance on validation and test sets.
- Integrate attention for improved decoding accuracy.
- Visualize attention maps and RNN connectivity.

---

## Dataset

We use the **Dakshina dataset** (v1.0), specifically `dakshina_dataset_v1.0/hi/lexicons/` for Hindi transliteration. The dataset consists of tuples in the format:  
`<romanized_input> <native_output>`

---

## Setup

```bash
git clone https://github.com/Nikshay-Jain/DA6401-Assign-3.git
pip install -r requirements.txt     # for local env exceution
````

Ensure your environment supports GPU acceleration (e.g., Google Colab, Kaggle).

---

## Files

* `dl-assign-3.ipynb`: Main implementation notebook.
* `requirements.txt`: Required packages.
* `predictions_vanilla/`: Outputs of vanilla seq2seq model on test data.
* `predictions_attention/`: Outputs of attention model on test data.
* `wandb/`: W\&B logs and sweep reports.

---

## Model Features

* Configurable character embeddings, RNN cell types (RNN, GRU, LSTM), hidden sizes, and layer counts.
* Beam search decoding.
* Dropout for regularization.
* Supports vanilla and attention-based decoding.
* Detailed wandb logging and visualizations.

---

## Training

```python
# Inside the notebook:
# Set parameters
# Run training cell
```
---

## Evaluation

Run final evaluation on the test set using the best model:

* Accuracy is computed based on exact sequence match.
* Predictions and attention maps are logged.
* Common errors and patterns are analyzed (e.g., more errors on long sequences or consonants).

---

## Visualization

* **Attention heatmaps** for selected test examples.
* **Connectivity visualizations** showing encoder-decoder alignment (inspired by Distill.pub).
* **W\&B plots**: accuracy vs time, parallel coordinates, and correlation tables.

---

## Reporting

* W\&B Report: [Assignment Report](https://wandb.ai/mm21b044-indian-institute-of-technology-madras/DA_seq2seq_transliteration/reports/DA6401-Assignment-3--VmlldzoxMjg2NTM4MA?accessToken=dhitf5spe0x83f8l1uinfylairt6l2p8q5uaizkfv24ihl9nf76xud14c35fw5xe)
* GitHub: [https://github.com/](https://github.com/Nikshay-Jain/DA6401-Assign-3.git)

---

## Notes

* Only training and validation sets were used for model selection.
* Test data was used strictly for final evaluation.
* All commits are spaced over time to reflect development progress.

---