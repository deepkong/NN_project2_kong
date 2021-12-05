# "Music Generation"
2020021461 Heejo Kong

2nd project for Applications and Practice in Neural Networks

This repository is based on third party implementation code of "Music Transformer"

https://github.com/gwinndr/MusicTransformer-Pytorch

https://arxiv.org/pdf/1809.04281.pdf


## Installation

For install and data preparation, please refer to the guidelines as follows

This repository supports Pytorch >= 1.2.0 with Python >= 3.6

Donwload [dataset] https://drive.google.com/file/d/1TTFloQwNdg95h-IJceUtVs1WQl_Bu1Ev/view?usp=sharing \
Need to prepare the data root as below
```
NN_project1_kong
├── mmseg
├── tools
├── local_configs
├── data
│   ├── semantic_drone_dataset
│   │   ├── images
│   │   ├── labels
│   │   ├── split
│   │   │   ├── train.txt
│   │   │   ├── val.txt
│   │   │   ├── test.txt
```


## Training
Donwload [pretrained weights] https://drive.google.com/file/d/1VuhtdeQSGl2gxndg_-98HPFJ1qEl3KiH/view?usp=sharing
```
# Single-gpu training
python tools/train.py local_configs/segformer_drone/segformer.b2.512x512.drone.20k.py

# Multi-gpu training
./tools/dist_train.sh local_configs/segformer_drone/segformer.b2.512x512.drone.20k.py <GPU_NUM>
```


## Evaluation
Donwload [weights] https://drive.google.com/file/d/15X00UIMRd3cmFC7sgKiHu5DCRQhM5zik/view?usp=sharing
```
# Single-gpu testing
python tools/test.py local_configs/segformer_drone/segformer.b2.512x512.drone.20k.py /path/to/checkpoint_file --show-dir /path/to/save_file

# Multi-gpu testing
./tools/dist_test.sh local_configs/segformer_drone/segformer.b2.512x512.drone.20k.py /path/to/checkpoint_file <GPU_NUM> --show-dir /path/to/save_file
```
