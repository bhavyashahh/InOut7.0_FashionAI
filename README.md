# SieveNet #
This is the unofficial implementation of 'SieveNet: A Unified Framework for Robust Image-Based Virtual Try-On' </br>
Paper can be found from [here](https://arxiv.org/pdf/2001.06265.pdf)

# Dataset downloading and processing #
Dataset download instructions and link of dataset can be found from official repo of [CP-VTON](https://github.com/sergeywong/cp-vton) and [VITON](https://github.com/xthan/VITON) </br>
Put dataset in `data` folder

# Usage #
Clone the repo and install requirements through ```pip install -r requirements.txt``` 

# Traning #
#### Coarse-to-Fine Warping module ####
&nbsp;&nbsp;&nbsp;&nbsp; In `config.py` set ```self.datamode='train'``` and ```self.stage='GMM'```
</br> &nbsp;&nbsp;&nbsp;&nbsp; then run ```python train.py```
</br> You can observe results while traning in tensorboard as below
</br>
![SS from tensorboard while training gmm](https://github.com/levindabhi/SieveNet/blob/master/images/train_gmm.png)

####  Conditional Segmentation Mask generation module ####
&nbsp;&nbsp;&nbsp;&nbsp; In `config.py` set ```self.datamode='Train'``` and ```self.stage='SEG'```
</br> &nbsp;&nbsp;&nbsp;&nbsp; then run ```python train.py```
</br>
![SS from tensorboard while training segm](https://github.com/levindabhi/SieveNet/blob/master/images/train_seg.jpeg)

####  Segmentation Assisted Texture Translation module ####
&nbsp;&nbsp;&nbsp;&nbsp; In `config.py` set ```self.datamode='Train'``` and ```self.stage='TOM'```
</br> &nbsp;&nbsp;&nbsp;&nbsp; then run ```python train.py```
</br>
![SS from tensorboard while training tom](https://github.com/levindabhi/SieveNet/blob/master/images/train_tom.png)



