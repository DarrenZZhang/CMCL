# Contrastive Multi-bit Collaborative Learning for Deep Cross-modal Hashing


### 1. Introduction

This is the source code of the paper "Contrastive Multi-bit Collaborative Learning for Deep Cross-modal Hashing" published in TKDE 2024.


### 2. Requirements

- python 3.7.6
- pytorch 1.8.0
- torchvision 0.9.0
- numpy
- scipy
- tqdm
- pillow
- einops
- ftfy
- regex
- ...




### 3. Preparation

#### 3.1 Download pre-trained CLIP

The pretrained CLIP model could be found in the 30 lines of [CLIP/clip/clip.py](https://github.com/openai/CLIP/blob/main/clip/clip.py). 
This code is based on the "ViT-B/32". 
You should download "ViT-B/32" and put it in `./cache`, or you can find it from the following link:

link: https://pan.baidu.com/s/1ZyDTR2IEHlY4xIdLgxtaVA 
password: kdq7


#### 3.2 Generate dataset

You should generate the following `*.mat` file for each dataset. The structure of directory `./dataset` should be:
```
    dataset
    ├── coco
    │   ├── caption.mat 
    │   ├── index.mat
    │   └── label.mat 
    ├── flickr25k
    │   ├── caption.mat
    │   ├── index.mat
    │   └── label.mat
    └── nuswide
        ├── caption.mat
        ├── index.mat 
        └── label.mat
```

Please preprocess the dataset to the appropriate input format.

More details about the generation, meaning, and format of each mat file can be found in `./dataset/README.md`.

Additionally, cleaned datasets (MIRFLICKR25K & MSCOCO & NUSWIDE) used in our experiments are available at `pan.baidu.com`:

link: https://pan.baidu.com/s/1ZyDTR2IEHlY4xIdLgxtaVA 
password: kdq7


### 4. Train

After preparing the Python environment, pretrained CLIP model, and dataset, we can train the CMCL model.

See `CMCL_$DATASET$.sh`.

### 5. Test
See `CMCL_$DATASET$_TEST.sh`.

### 6. Citation
If you find our approach useful in your research, please consider citing:

Qingpeng Wu, Zheng Zhang, Yishu Liu, Jingyi Zhang, Liqiang Nie, Contrastive Multi-bit Collaborative Learning for Deep Cross-modal Hashing, IEEE Transactions on Knowledge and Data Engineering (TKDE), 2024.

### 7. Any question

If you have any questions, please feel free to contact Zheng Zhang (darrenzz219@gmail.com) or Qingpeng Wu (wqp0033@gmail.com).
