# Manifold_mixup Supervised

### Requirements
This code has been tested with
python 3.6.8
torch 1.0.0
torchvision 0.2.1

### Additional packages required

```
matplotlib==3.0.2
numpy==1.15.4
pandas==0.23.4
Pillow==5.4.1
scipy==1.1.0
seaborn==0.9.0
six==1.12.0
```

### Important :Running each of the following commands will automatically create a subdirectory containing the output of that particular experiment in the manifold_mixup/supervised/experiments directory

### How to run experiments for CIFAR10

#### No mixup Preactresnet18
```
python pgd-visualize.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 500 --schedule 500 --gammas 0.1 --train vanilla
```

#### Mixup Preactresnet18

```
python pgd-visualize.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 500 --schedule 500 --gammas 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup Preactresnet18
```
python pgd-visualize.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 500 --schedule 500 --gammas 0.1 --train mixup_hidden --mixup_alpha 2.0
```

#### No mixup Preactresnet34
```
python main.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train vanilla 
```

#### Mixup Preactresnet34

```
python main.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup Preactresnet34
```
python main.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0 
```

#### No mixup WRN-28-10
```
python main.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train vanilla
```

#### Mixup WRN-28-10

```
python main.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup WRN-28-10
```
python main.py --dataset cifar10 --data_dir data/cifar10/ --root_dir experiments/ --labels_per_class 5000 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```

### How to run experiments for MNIST

#### No mixup LeNet5
```
python pgd-visualize.py --dataset mnist --data_dir data/mnist/ --root_dir experiments/ --labels_per_class 5000 --arch lenet5 --learning_rate 0.0002 --momentum 0.9 --decay 0 --epochs 800 --schedule 400 600 --gammas 0.5 0.5 --train vanilla --pgd_eps 0.3 --pgd_alpha 0.01 --pgd_step_size 40
```

#### Mixup LeNet5

```
python pgd-visualize.py --dataset mnist --data_dir data/mnist/ --root_dir experiments/ --labels_per_class 5000 --arch lenet5 --learning_rate 0.0002 --momentum 0.9 --decay 0 --epochs 800 --schedule 400 600 --gammas 0.5 0.5 --train mixup --mixup_alpha 1 --pgd_eps 0.3 --pgd_alpha 0.01 --pgd_step_size 40
```

#### Manifold mixup LeNet5

```
python pgd-visualize.py --dataset mnist --data_dir data/mnist/ --root_dir experiments/ --labels_per_class 5000 --arch lenet5 --learning_rate 0.0002 --momentum 0.9 --decay 0 --epochs 800 --schedule 400 600 --gammas 0.5 0.5 --train mixup_hidden --mixup_alpha 2.0 --pgd_eps 0.3 --pgd_alpha 0.01 --pgd_step_size 40
```



### How to run experiments for CIFAR100

#### No mixup Preactresnet18
```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train vanilla 
```

#### Mixup Preactresnet18

```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup Preactresnet18
```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```

#### No mixup Preactresnet34
```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train vanilla
```

#### Mixup Preactresnet34

```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup Preactresnet34
```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```

#### No mixup WRN-28-10
```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train vanilla
```

#### Mixup WRN-28-10

```
python main.py --dataset cifar100 --data_dir data/cifar100/ --root_dir experiments/ --labels_per_class 500 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup WRN-28-10
```
python main.py --dataset cifar100 --data_dir data/cifar109/ --root_dir experiments/ --labels_per_class 500 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```


### How to run experiments for SVHN

#### No mixup Preactresnet18
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train vanilla
```

#### Mixup Preactresnet18

```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup Preactresnet18
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```

#### No mixup Preactresnet34
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train vanilla
```

#### Mixup Preactresnet34
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup Preactresnet34
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch preactresnet34 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 500 1000 1500 --gammas 0.1 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```

#### No mixup WRN-28-10
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train vanilla
```

#### Mixup WRN-28-10

```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train mixup --mixup_alpha 1.0
```

#### Manifold mixup WRN-28-10
```
python main.py --dataset svhn --data_dir data/svhn/ --root_dir experiments/ --labels_per_class 7325 --arch wrn28_10 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 400 --schedule 200 300 --gammas 0.1 0.1 --train mixup_hidden --mixup_alpha 2.0
```

### How to run experiments for Tiny-Imagenet-200

1.Download the zipped data from https://tiny-imagenet.herokuapp.com/
2.If not already existing, create a subfolder "data" in root folder "manifold_mixup"
3.Extract the zipped data in folder manifold_mixup/data
4.Run the following script (This will arange the validation data in the format required by the pytorch loader)
```
python utils.py
```

5. Run the following commands
#### No mixup Preactresnet18
```
python main.py --dataset tiny-imagenet-200 --data_dir data/tiny-imagenet-200/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 1000 1500 --gammas 0.1 0.1 --train vanilla 
```

#### Mixup Preactresnet18

```
python main.py --dataset tiny-imagenet-200 --data_dir data/tiny-imagenet-200/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 1000 1500 --gammas 0.1 0.1 --train mixup --mixup_alpha 0.2
```

#### Manifold mixup Preactresnet18
```
python main.py --dataset tiny-imagenet-200 --data_dir data/tiny-imagenet-200/ --root_dir experiments/ --labels_per_class 500 --arch preactresnet18 --learning_rate 0.1 --momentum 0.9 --decay 0.0001 --epochs 2000 --schedule 1000 1500 --gammas 0.1 0.1 --train mixup_hidden --mixup_alpha 0.2
```





