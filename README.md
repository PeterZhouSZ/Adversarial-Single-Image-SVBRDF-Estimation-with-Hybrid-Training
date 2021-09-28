# Adversarial-Single-Image-SVBRDF-Estimation-with-Hybrid-Training
This is code of "Adversarial Single-Image SVBRDF Estimation with Hybrid Training"

<img src='./misc/representation.jpg'>

## Requirements
This codebase was developed and tested with PyTorch 1.2 and Python 3.6 in both windows and Linux system.
To install environments, please use this command:

```bash
conda env create -f environment.yml
```

## Dataset 

The synthetic dataset are provided by Deschaintre et al.2018, please download through this [link] (https://repo-sam.inria.fr/fungraph/deep-materials/)
The real images dataset can be downloaded from this link

## Inference

The pretrained checkpoint model can be downloaded from this link

To run the inference code, please use this command:

```
python test.py --name $exp --dataroot $data --resize_or_crop resize --MyTest ALL_4D --netG NewVA_Net_Light --which_epoch final --mode Real --savename $name
```
Please download the providede checkpoint and save it into 


Here are some instructions about the command:

```
--name: your experiment name
--dataroot: path of test dataset
--MyTest: [ALL_4D: output four feature maps || ALL_5D: output four feature maps + rerendered images using estimated feature maps and light position given single input images]
--which_epoch: the name of checkpoint to load
--mode: [Syn: show both ground truth and estimated results || Real: only show estimated results]
--savename: the folder name where results are saved


## Training