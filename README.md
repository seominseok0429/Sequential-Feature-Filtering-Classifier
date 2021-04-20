# Sequential Feature Filtering Classifier

Minseok Seo, Jaemin Lee, Jongchan Park, and Dong-Geol


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

| METHOD | DATASET | AUC | 
|:--------:|:--------:|:--------:|
| ResNet-50 | ImageNet-1K | 75.80 |
| [ResNet-50+FFC](https://github.com/seominseok0429/Sequential-Feature-Filtering-Classifier/edit/main/README.md) | ImageNet-1K | 77.01 |

## train-test script

### train

```
python main.py --ffc
```

### test

```
python main.py --ffc --path ./ffc.pth
```
