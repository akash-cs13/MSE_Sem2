## Image Classification 

This project involves image classification using deep learning models trained to classify images into two categories: "stop" and "priority". The models were trained using the ResNet18 and MobileNetV3 architectures. The dataset used for training and testing is contained in the `data.zip` file.

### Dataset

The dataset `data.zip` consists of images classified into two categories:

- **Stop**
- **Priority**


### Models and Training

The python notebook containing the code for training the models in Google Colab can be found in `classification_modeltraining1.pynb`.

| Model                      | Architecture  | Training Environment | Best Accuracy | Epochs |
|----------------------------|---------------|----------------------|---------------|--------|
| `my_flower.pth`            | ResNet18      | Jetson Car           | 1.000000      | 10     |
| `my_flower_resnet18.pth`   | ResNet18      | Google Colab         | 1.000000      | 10     |
| `my_flower_mobilenet_v3.pth`| MobileNetV3   | Google Colab         | 0.946667      | 10     |

