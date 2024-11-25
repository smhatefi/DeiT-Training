# DeiT-Training

## Dataset
```
mkdir Datasets
```
```
wget https://www.cs.toronto.edu/~kriz/cifar-100-python.tar.gz -P ./Datasets
```
```
tar -xf ./Datasets/cifar-100-python.tar.gz -C ./Datasets
```

## Clone Repository
```
git clone https://github.com/smhatefi/DeiT-Training
```
```
cd DeiT-Training
```

## Normal Training
```
python -W ignore main.py --model MODEL --input-size InputSize --batch-size BatchSize --output ./outputs --data-set CIFAR --data-path ../Datasets/
```

### Resume Training
```
python -W ignore main.py --model MODEL --input-size InputSize --batch-size BatchSize --output ./outputs --resume ./outputs/checkpoint.pth --data-set CIFAR --data-path ../Datasets/
```

## Extra Augment
```
python -W ignore main.py --model MODEL --input-size InputSize --batch-size BatchSize --ThreeAugment --src --output ./outputs --data-set CIFAR --data-path ../Datasets/
```

### Resume Training
```
python -W ignore main.py --model MODEL --input-size InputSize --batch-size BatchSize --ThreeAugment --src --output ./outputs --resume ./outputs/checkpoint.pth --data-set CIFAR --data-path ../Datasets/
```

## Evaluating
```
python -W ignore main.py --model MODEL --input-size InputSize --batch-size BatchSize --resume ./outputs/best_checkpoint.pth --data-set CIFAR --data-path ../Datasets/ --eval
```