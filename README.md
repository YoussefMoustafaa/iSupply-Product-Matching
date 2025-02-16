# Product Matching System for Pharmaceutical Marketplace Overview

This project develops an advanced product matching system for a pharmaceutical marketplace. The system is designed to accurately match product names by leveraging both textual features and additional product attributes such as price. By combining robust text preprocessing, domain-specific normalization, and a deep learning model, our solution aims to deliver high accuracy and fast inference without the need for a GPU.
Features

### Text Normalization & Preprocessing:
Removal of Arabic diacritics and standardization of characters.
Custom normalization for pharmaceutical terms (e.g., converting various dosage forms to a standard form).
Tokenization and lemmatization using the Qalsadi library.

### Deep Learning Model:
An improved RNN model leveraging Bidirectional LSTM and GRU layers.
Use of embedding layers to learn text representations.
Integration of price as an additional feature (after scaling).

## Dataset

The dataset is provided as an Excel file with two main sheets:

Master File: Contains the official product names and related details.
Dataset: Contains seller item names along with pricing and SKU details.

## Installation
### Prerequisites

Python 3.7+
Required libraries:
    pandas
    numpy
    re
    sklearn
    tensorflow
    qalsadi

Install the required packages using pip:

```
pip install pandas numpy nltk scikit-learn tensorflow qalsadi
```

## Usage

### Data Preprocessing:

The script reads the Excel file, applies extensive text normalization (including handling of Arabic text and pharmaceutical-specific terms), and prepares the dataset for model training. It also scales the price feature.

### Tokenization and Sequence Padding:

The text from the seller item names is tokenized and padded to prepare input for the RNN model.

### Model Training:

An improved RNN model is built using Bidirectional LSTM and GRU layers. The model is trained with early stopping to prevent overfitting.

### Evaluation:

The model is evaluated on a hold-out test set, and accuracy is printed as the performance metric.

Open the notebook and press Run All

## Code Structure

### Data Preprocessing:
Functions for text normalization and lemmatization are defined, including removal of diacritics, standardization of terms, and tokenization.

### Model Definition and Training:
The RNN model is defined using TensorFlow/Keras, with an embedding layer, Bidirectional LSTM, GRU, and Dense layers. Training is performed with early stopping.

### Evaluation:
Model performance is evaluated on the test set, and key metrics are printed.
