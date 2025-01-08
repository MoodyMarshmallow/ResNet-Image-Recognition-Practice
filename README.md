# ResNet-Weather-Image-Recognition
In an effort to put the knowledge I had learned from the [fast.ai course](https://course.fast.ai/) into practical use. I decided to build a Residual Neural Network to classify images of different weather phenomena.

## Features

- Base model is a pre-activation ResNet52 (as detailed in [this](https://doi.org/10.48550/arXiv.1603.05027) paper)
- Dropout layers added to the bottleneck residual blocks according to [this](https://doi.org/10.48550/arXiv.2302.06112) paper.
- RAdam optimizer used, along with decoupled weight decay regularization found in the AdamW optimizer.
- Learning rate scheduled using 2 cycles of the CosineAnnealingLR scheduler described in [this](https://doi.org/10.48550/arXiv.1608.03983) paper
- Max Norm weight constraint on convolutions attempted but resulted in underfitting. Used l2 regularization with a large lambda instead.
- Final accuracy of 79.74%
