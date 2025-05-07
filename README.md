CS-598 Final Project
Authors:

Daniel Valentine

Michael Quan

Date: May 6, 2025

Overview
This repository contains the code and resources for the CS-598 Final Project. The project implements and benchmarks deep learning models for time series classification using multiple sensor datasets. It is designed for ease of use in Python notebooks, with special optimization for Google Colab and TPU acceleration.

Features
- Plug-and-play setup for Google Colab (auto-detects and uses TPUs for faster training; falls back to CPU/GPU if unavailable)
- Automatic dataset download and extraction to the data/ directory
- Flexible model architectures: MLP, LSTM, FCN, ResNet, and Encoder
- Advanced metrics: accuracy, precision, recall, AUC, top-k categorical accuracy
- Custom logging: All results are saved to results_output.log for easy review
- Reproducibility: Hyperparameters and computational settings are clearly documented

Quick Start
The notebook file installs dependencies, downloads and organizes the dataset, and runs the model in the notebook. You can simply run all and the notebook and model should begin running. It uses the following steps: 

1. Install dependencies
  The notebook will auto-install required packages:
  !pip install numpy pandas matplotlib scikit-learn pyts torch tensorflow
2. Data Preparation
  The script automatically downloads and unzips the required datasets into the data/ directory.
3. Run the rest of the notebook
  Open the notebook in Google Colab for best performance. The code will:
    - Detect and use TPU if available
    - Parse the datasets
    - Train and evaluate models
    - Output all results to results_output.log

Logging & Output
All training progress and evaluation metrics are saved in results_output.log (INFO level and above, with warnings shown only on console).
Metrics reported include:
  - Accuracy
  - Precision
  - Recall
  - AUC
  - Top-K Categorical Accuracy
  - Loss

Customization
Models: You can easily switch between MLP, LSTM, FCN, ResNet, and Encoder architectures.
Metrics: The code supports multiple similarity metrics (DTW, BOSS, Wasserstein, etc.) for transfer learning experiments.
Hyperparameters: Learning rate, batch size, hidden layer size, dropout, and epochs are all configurable at the top of the script.

Partners
Daniel Valentine
Michael Quan

Citation
This code is based on and expands on code from Daily Physical Activity Monitoring: Adaptive Learning from Multi-source Motion Sensor Data (CHIL 2024)
https://github.com/Oceanjinghai/HealthTimeSerial

License
This project is for educational use in CS-598.
See individual files for license details if applicable.

For questions or collaboration, please contact Daniel Valentine or Michael Quan.
