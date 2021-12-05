# "Music Generation"
2020021461 Heejo Kong

2nd project for Applications and Practice in Neural Networks

This repository is based on third party implementation code of "Music Transformer"

Link: https://github.com/gwinndr/MusicTransformer-Pytorch

Paper: https://arxiv.org/pdf/1809.04281.pdf


## Installation

For install and data preparation, please refer to the guidelines as follows

This repository supports Pytorch >= 1.2.0 with Python >= 3.6

Donwload [dataset] https://drive.google.com/file/d/1Mq3C4flVX1OJElPSVIB8Cqmh2xPdZ1xk/view?usp=sharing \
Need to prepare the data root as below
```
NN_project2_kong
├── model
├── third_party
├── utilities
├── dataset
│   ├── e_piano.py
│   ├── e_piano
│   ├── midi_data
│   ├── preprocessed
│   │   
```


## Training
```
python train.py -output_dir <folder_name> --rpr
```


## Evaluation
Donwload [weights_Baseline] https://drive.google.com/file/d/1D2ih4l-yFhvBVqcu0F6TWuMng0x-4pqb/view?usp=sharing \
Donwload [weights_MTGAN] https://drive.google.com/file/d/1J_CSJY2gsi2gHmt2iVKoLUmSXtUHk7S2/view?usp=sharing \
Download [result_sample] https://drive.google.com/file/d/1dP-z-J9B6bj_qUJvGBle09kyrB2Icv3S/view?usp=sharing \
Need to prepare the data root as below
```
NN_project1_kong
├── model
├── third_party
├── utilities
├── dataset
├── mt_gan
│   ├── results
│   ├── tensorboard
│   │   
├── baseline
│   ├── results
│   ├── tensorboard
│   │   
```

```
python evaluate.py -model_weights <pretrained_weight_path> --rpr
```

## Generation
```
python generate.py -output_dir <folder_name> -model_weights <pretrained_weight_path> --rpr
```
