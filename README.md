# ABOSD: Autoencoder-Based Open-Set Detection of Zero-Day Network Intrusion

**Course:** Advanced Deep Learning (CS-601), Bahria University  
**Author:** Rameen Sohail

## Overview
This project implements the ABOSD framework for network intrusion detection. Standard deep learning classifiers fail on zero-day attacks because their SoftMax layer forces 100% confidence across known classes, so unknown attacks get silently labeled as normal traffic. ABOSD solves this by pairing an LSTM classifier with an autoencoder trained on CICIDS2017. When the autoencoder sees unfamiliar traffic, reconstruction error increases significantly and that error is used to flag the flow as suspicious. The baseline LSTM detected 0% of unknown attacks while ABOSD detected 99.85% from UNSW-NB15 and 90.20% from NSL-KDD with only a 2% false alarm rate, and no retraining was needed.

## Datasets Used
- CICIDS2017 (training)
- UNSW-NB15 (unknown test set 1)
- NSL-KDD (unknown test set 2)

## Requirements
- Python 3.x
- TensorFlow / Keras
- scikit-learn
- pandas, numpy, matplotlib, seaborn

## How to Run
Open `Research_competition.ipynb` in Jupyter Notebook or VS Code and run cells in order. Make sure dataset paths are set correctly.
