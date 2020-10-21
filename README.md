# Session 10 

The model reaches a maximum accuracy of **91.11%** on CIFAR-10 dataset using **ResNet-18** model.

**LR Finder and Reduce LR on Plateau** was implemented for model training.


### Parameters and Hyperparameters

- Loss Function: Cross Entropy Loss (combination of `nn.LogSoftmax` and `nn.NLLLoss`)
- LR Finder
  - Start LR: 1e-7
  - End LR: 5
  - Number of iterations: 400
- Optimizer: SGD
  - Momentum: 0.9
  - Learning Rate: 0.012 (Obtained from LR Finder)
- Reduce LR on Plateau
  - Decay factor: 0.1
  - Patience: 2
  - Min LR: 1e-4
- Batch Size: 64
- Epochs: 50

### Data Augmentation

The following data augmentation techniques were applied to the dataset during training:

- Horizontal Flip
- Rotation
- CutOut
