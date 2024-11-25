# DeiT-Training

## Normal Training
```
python -W ignore main.py --model MODEL --input-size 224 --output ./outputs --data-set CIFAR --data-path ../Datasets/
```

### Resume Training
```
python -W ignore main.py --model MODEL --input-size 224 --output ./outputs --resume ./outputs/checkpoint.pth --data-set CIFAR --data-path ../Datasets/
```

## Extra Augment:
```
python -W ignore main.py --model MODEL --input-size 224 --ThreeAugment --src --output ./outputs --data-set CIFAR --data-path ../Datasets/
```

### Resume Training
```
python -W ignore main.py --model MODEL --input-size 224 --ThreeAugment --src --output ./outputs --resume ./outputs/checkpoint.pth --data-set CIFAR --data-path ../Datasets/
```

## Evaluating
```
python -W ignore main.py --model MODEL --resume ./outputs/best_checkpoint.pth --input-size 224 --data-set CIFAR --data-path . --eval
```