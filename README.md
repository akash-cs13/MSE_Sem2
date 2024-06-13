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

## Image Regression

This project involves image regression using deep learning models to predict coordinates, specifically trained for driving applications. The models were trained using the ResNet18 and MobileNetV3 architectures. 

### Models and Training

The original dataset collected is in `xyz.zip` (1,714 images), and the processed dataset used for training is in `xyz_processed.zip` (1,003 images). The Google Colab notebook containing the code for model training and testing can be found in `Pytorch.ipynb`. The models were evaluated using `eval.zip`, which consists of 200 images. Based on the evaluation, ResNet18 exhibited a lower mean error, indicating better performance for the regression task.

| Model                | Architecture | Training Environment | Mean Error | Epochs | Loss   |
|----------------------|--------------|----------------------|------------|--------|--------|
| `model_resnet18.pth` | ResNet18     | Google Colab         | 14.4967    | 10     | 72.0884|
| `model_mobilenetv3.pth`| MobileNetV3 | Google Colab         | 14.8934    | 10     | 99.2242|

### Model Deployment

Since ResNet18 showed superior performance in terms of mean error during evaluation, it was chosen for deployment. The deployment model `road_honeybee.pth` was trained on the Jeston car and the `road_honeybee_trt.pth` is the optimized model used in deployment.


