# Universal Deepfake Image Detector using CLIP-based Method

**CVPR 2024 Deepfake Analysis and Detection Challenge** <br>


[[Workshop Page](https://dfad.unimore.it/)] [[Challenge Page](https://dfad.unimore.it/challenge/)]


## Contents

- [TODO](#todo)
- [Setup](#setup)
- [Dataset Preparation](#dataset-preparation)
- [Evaluation](#evaluation)
- [Training](#training)
- [Pretrained model](#pretrained-model)
- [Acknowledgments](#acknowledgments)


## TODO
- Train/evaluation code.
- Dataset download and processing code.
- Code to replicate challenge results.
- Pre-trained models.


## Setup 

1. Clone this repository 
```bash
git clone https://github.com/RaghadKhaled/DFAD_2024.git
```

2. Install the necessary libraries
```bash
pip install -r requirements.txt
```


## Dataset Preparation
- Prepare the training/testing list file through `data/preprocessing.py`.
- You can find the image path lists of first 800K records (for two classes) [[here](https://drive.google.com/file/d/1xT-3v5CmSs6Hqs2Lbn5_I39qOS1G1K3e/view?usp=sharing)]
- You can find the image lists of first 800K records (for five classes) [[here](https://drive.google.com/file/d/1kcFZOTR02iImBT2yhH_BBh5vPMOBHDLF/view?usp=sharing)]

## Evaluation
- You can evaluate the model by running the following command:
```bash
sh evaluate.sh
```

The parameters values in `evaluate.sh` file are as following:

- `data_root`: root path of testing list file.
- `model`: 'LASTED'.
- `num_class`: the class number of training dataset (default: 2).
- `test_file`: full path of testing list file.
- `batch_size`: the training batch size over all gpus. (default: 48)
- `isTrain`: 0.
- `ckps`: the full path for the pre-trained model weights.
- `data_size`: the image size for training (default: 448). 
- `out_dir`: the output folder path to save the results.


## Training
- You can train the model by running the following command:
```bash
sh train.sh
```

The parameters values in `train.sh` file are as following:

- `data_root`: root path of testing list file.
- `model`: 'LASTED'.
- `num_class`: the class number of training dataset (default: 2).
- `train_file`: full path of train list file.
- `test_file`: full path of validation list file.
- `isTrain`: 1.
- `lr`: the initial learning rate (default: 0.0001).
- `batch_size`: the training batch size over all gpus. (default: 48)
- `data_size`: the image size for training (default: 448). 
- `out_dir`: the output folder path to save the checkpoint.



## Pretrained model

- Download all pretrained weight files from [[here](https://drive.google.com/drive/folders/1DgiN4aeTbEdHt9Pre_iQxfVn_KOEhXlJ?usp=drive_link)].

## Acknowledgments
This repository borrows partially from the [[LASTED](https://github.com/HighwayWu/LASTED)]
