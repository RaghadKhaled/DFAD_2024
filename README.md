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
- Prepare the training/testing list file through `preprocess.py`.


## Evaluation
- You can evaluate the model by running the following command:
```bash
sh evaluate.sh
```

The parameters values in `evaluate.sh` file are as following:

- `data_root`: root path of testing list file.
- `model`:
- `num_class`: 2.
- `test_file`: full path of testing list file.
- `batch_size`: 48.
- `isTrain`: 0.
- `ckps`:
- `data_size`: 448 
- `out_dir`:


## Training
- You can train the model by running the following command:
```bash
sh train.sh
```

The parameters values in `train.sh` file are as following:

- `data_root`: root path of testing list file.
- `model`:
- `num_class`: 2.
- `train_file`: full path of train list file.
- `test_file`: full path of validation list file.
- `val_ratio`: 0.005.
- `isTrain`: 1.
- `lr`: 0.0001.
- `batch_size`: 48.
- `ckps`:
- `data_size`: 448 
- `out_dir`:
- `gpu`:
- `resume`:



## Pretrained model

Coming soon..
