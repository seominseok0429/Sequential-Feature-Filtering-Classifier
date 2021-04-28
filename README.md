# Sequential Feature Filtering Classifier


Minseok Seo, Jaemin Lee, Jongchan Park, and Dong-Geol

<img width="1376" alt="Screen Shot 2021-04-22 at 8 59 05 PM" src="https://user-images.githubusercontent.com/33244972/115710771-ac47fa00-a3ad-11eb-8c3f-ed4dd5c9ed84.png">

## Abstract

In this study, we propose Sequential Feature Filtering Classifier (FFC), a simple but effective classifier for convolutional neural networks (CNNs). Using sequential LayerNorm and ReLU, FFC zeroes out low-activation units and preserves high-activation units. The sequential feature filtering process generates multiple features, which are transmitted to a shared classifier, yielding multiple outputs. FFC can be applied to any CNN with a classifier and it significantly improves the performance with negligible overhead.  In this study, the efficacy of FFC is validated extensively on various tasks—ImageNet-1K classification, MS COCO detection, Cityscapes segmentation, and HMDB51 action recognition. Moreover, it is empirically established that FFC can further improve performances using additional techniques, including attention modules.


## Datasets

* The datsets can be downloaded from 

    [ImageNet-1K](https://www.kaggle.com/c/imagenet-object-localization-challenge/data)

/IMAGENET/ILSVRC/Data/CLS-LOC/
* Directory tree
 ```
    DATA/
        ILSVRC/ 
              /Data
                    /CLS-LOC
                            /train
                            /val
        
    Sequential-Feature-Filtering-Classifier/
        (main.py)

```

## Models

Note that our top performance was **76.97** as a result of multiple runs, but the average of the results of multiple runs was **76.84** on the paper.

| METHOD | DATASET | ACC | 
|:--------:|:--------:|:--------:|
| ResNet-50 | ImageNet-1K | 75.80 |
| ResNet-50+FFC | ImageNet-1K | **76.97** |

## train-test script

### train

```
python main.py --ffc
```

### test

```
python main.py --ffc --r
```
