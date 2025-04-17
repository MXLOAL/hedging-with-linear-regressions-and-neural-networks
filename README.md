# hedging-with-linear-regressions-and-neural-networks

This repository contains an implementation of the models and experiments described in the paper:  
Johannes Ruf & Weiguan Wang (2021): **Hedging With Linear Regressions and Neural Networks, Journal of Business & Economic Statistics**, DOI:10.1080/07350015.2021.1931241 (https://doi.org/10.1080/07350015.2021.193124)

The goal is to reproduce the results from the paper using PyTorch.

Date: 18 April 2025

---

## About

The original paper investigates how machine learning models — specifically linear regressions and neural networks — can be used for hedging a simple portfolio in financial markets. This repository provides:
- PyTorch implementations of the proposed models  
- Notebooks for running training, evaluation, and benchmark comparisons   
- Integration with [Weights & Biases (WandB)](https://wandb.ai/) for experiment tracking (optional)

---

## Getting Started

Clone the repository and install the required dependencies

There are two workflows:

1. **Standard PyTorch Execution**  
   Run: `Model-PYTORCH-V2.ipynb`

2. **PyTorch Lightning + WandB Execution**  
   Run: `Model-LIGHTNING-V2.ipynb`  
   > Make sure you have a WandB account and API key set up if you want to log experiments.

Once training is completed, you can visualize and compare results by running: `BENCHMARK-V1.ipynb`

> Each notebook is self-contained and can be run independently.

---

## Structure

```bash
.
├── README.md
│
├── data
│   ├── df_train.parquet
│   ├── df_train_2d.parquet
│
├── notebooks <- Training/inference/benchmark notebooks
│
├── code <- Related code used by notebooks
│   ├── src
│       ├── nemo
│            ├── collections
│            ├── utils
│            ├── __init__.py
│            ├── constants.py
│            ├── package_info.py
│
├── .jpg and .png files

## Data folder structure

This repository contain ONLY the training datasets: `df_train.parquet` and `df_train_2d.parquet`.  
To recover all the simulated data (training and testing datasets), please the following procedure: https://github.com/weiguanwang/Hedging_Neural_Networks

## Package Information

| Package           | Version  |
|-------------------|----------|
| matplotlib        | 3.10.1   |
| numpy             | 2.1.3    |
| pandas            | 3.11.11  |
| python            | 0.24.2   |
| pytorch-lightning | 2.5.1    |
| scikit-learn      | 1.6.1    |
| scipy             | 1.15.2   |
| seaborn           | 0.13.2   |
| torch             | 2.6.0    |
| torchaudio        | 2.6.0    |
| torchmetrics      | 1.7.1    |
| torchvision       | 0.21.0   |

## License 

This project is licensed under the Apache-2.0 License.

## Reference

Johannes Ruf & Weiguan Wang (2021): Hedging With Linear Regressions and Neural Networks, Journal of Business & Economic Statistics, DOI:10.1080/07350015.2021.1931241 (https://doi.org/10.1080/07350015.2021.193124)