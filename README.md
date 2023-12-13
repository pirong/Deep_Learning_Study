# Deep_Learning_Study
A comparison study for deep learning models using the CIFAR-10 dataset.

Exponential Linear Unit (ELU) is an activation function defined as -
$$ f(x)=   \left\{
\begin{array}{ll}
      x & x>0_{krit} \\
      e^x-1 & x<=0_{krit} \\
\end{array} 
\right.  $$

Compared to the commonly used Rectified Linear Unit (ReLU) activation function, ELU produces negative outputs.
ELU is claimed to decrease loss faster and produce more accurate results.

I tested these claims by comparing the performance of neural networks using ELU and ReLU on these 4 network architectures - LeNet-5, AlexNet, VGG-16 and ResNet-50

### LeNet-5
For LeNet-5, while the ELU activation function performs marginally slower, accuracy is slightly higher compared to ReLU.
|                    |Test Accuracy|Time Elapsed|
|--------------------|-------------|------------|
|LeNet-5 with ReLU   |63.98%       |2 min 23.19s|
|LeNet-5 with ELU    |65.56%       |2 min 23.56s|

### AlexNet
For AlexNet, the ELU activation function performs marginally faster, but its accuracy is slightly higher compared to ReLU.
|                    |Test Accuracy|Time Elapsed |
|--------------------|-------------|-------------|
|AlexNet with ReLU   |84.50%       |32 min 24.64s|
|AlexNet with ELU    |83.36%       |32 min 15.08s|

### VGG16
For VGG16, although the ELU function takes slightly longer, the accuracy is higher.
|                   |Test Accuracy|Time Elapsed |
|-------------------|-------------|-------------|
|VGG-16 with ReLU   |85.24%       |61 min 28.50s|
|VGG-16 with ELU    |86.36%       |62 min 50.60s|

### ResNet-50
For ResNet-50, the ELU activation function performs marginally slower, and with lower accuracy compared to ReLU.
|                    |Test Accuracy|Time Elapsed |
|--------------------|-------------|-------------|
|AlexNet with ReLU   |82.98%       |36 min 43.61s|
|AlexNet with ELU    |81.76%       |37 min 32.61s|

### *The Best Model?*
As CIFAR-10 is a relatively simple dataset, more layers bring about diminishing returns.
The best model evaluated was ResNet-18, a model with only 18 layers, which was faster and provided similar results.
|                    |Test Accuracy|Time Elapsed |
|--------------------|-------------|-------------|
|ResNet-50 with ReLU |82.98%       |36 min 43.61s|
|ResNet-18 with ReLU |83.10%       |22 min 23.95s|

## Conclusion
The claim that the ELU activation function is faster and more accurate is only true for simpler CNNs. For more complex CNNs, ReLU is still preferred.
However, there are other ways which can improve CNNs -
1. Data augmentation
2. Tuning optimisers and learning rates
3. Weight decay and regulators

