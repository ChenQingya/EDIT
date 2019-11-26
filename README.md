# The code for EDIT: Exemplar-Domain Aware Image-to-Image Translation

## Introduction
This is the code for paper "EDIT: Exemplar-Domain Aware Image-to-Image Translation" （https://arxiv.org/abs/1911.10520）, which is based on pyTorch implementation of meta network for style transfer (from https://ypw.io/style-transfer/) and cycleGAN (from https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix). We design a novel generative adversarial network, namely exemplar-domain aware image-to-image translator (EDIT for short). The principle behind is that, for images from multiple domains, the content features can be obtained by a uniform extractor, while (re-)stylization is achieved by mapping the extracted features specifically to different purposes (domains and exemplars). The generator of our EDIT comprises of a part of blocks configured by shared parameters, and the rest by varied parameters exported by an exemplar-domain aware parameter network. In addition, a discriminator is equipped during the training phase to guarantee the output satisfying the distribution of the target domain. Our EDIT can flexibly and effectively work on multiple domains and arbitrary exemplars in a unified neat model.

## Network Architecture
![Reesuly](img/archf.png)

## Dependnecy
python 3.5, pyTorch >= 1.4.0 (from https://pytorch.org/), numpy, Pillow.
## Usage

### Training
1. Download the dataset you want to use and change the dataset directory. More datatsets can be found https://people.eecs.berkeley.edu/~taesung_park/CycleGAN/datasets/

2. Starting training using the following command

```python train.py```
 
### Testing
1. Put the pre-trained model in your own path and change the checkpoint path of the code
2. Starting testing using the following command

```python test.py```

## Results
![Reesuly](img/exp.png)
More Results can be found in our website: https://forawardstar.github.io/EDIT-Project-Page/
