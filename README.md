# Multiple Granularity Network
Implement of paper:[Learning Discriminative Features with Multiple Granularities for Person Re-Identification](https://arxiv.org/abs/1804.01438v1)

## Dependencies

- Python >= 3.5
- PyTorch >= 0.4.0
- torchvision
- scipy
- numpy
- scikit_learn



## Current Result

### With Re-Ranking
| backbone |  mAP | rank1 | rank3 | rank5 | rank10 |  
| :------: |  :------: | :------: | :------: | :------: |  :------: |   
| resnet50 |  94.33 | 95.58 | 97.54 | 97.92 | 98.46 | 
| paper |  94.20 | 96.60 | - | - | - | 

### Without Re-Ranking
| backbone |  mAP | rank1 | rank3 | rank5 | rank10 |  
| :------: |  :------: | :------: | :------: | :------: |  :------: |   
| resnet50 |  86.15 | 94.95 | 97.42 | 98.07 | 98.93 | 
| paper |  86.90 | 95.70 | - | 98.30 | 99.00 | 

## Data

Market1501 data download from [here](http://www.liangzheng.org/Project/project_reid.html)

## Weights

Pretrained weight download from [here](https://drive.google.com/open?id=1TyM7J_UjLhvU8UUkxcKwLQq8VFHlEWCa)
## Train

You can specify more parameters in opt.py

```
python3 train_eval.py --mode train --data_path <path/to/Market-1501-v15.09.15> 
```

## Evaluate

Use pretrained weight or your trained weight

```
python3 train_eval.py --mode evaluate --data_path <path/to/Market-1501-v15.09.15> --weight <path/to/weight_name.pt> 
```


## Citation

```text
@ARTICLE{2018arXiv180401438W,
    author = {{Wang}, G. and {Yuan}, Y. and {Chen}, X. and {Li}, J. and {Zhou}, X.},
    title = "{Learning Discriminative Features with Multiple Granularities for Person Re-Identification}",
    journal = {ArXiv e-prints},
    year = 2018,
}
```
