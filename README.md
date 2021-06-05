# Garbage Classification

Using deep learning to classify garbage.  
Classification:
- Recycle
  - Plastic
  - Paper
  - Metal
  - Glass
- Trash   

Data used in this project is taken by ourselves.

## Installation

To clone this repo, use git command:

```bash
git clone https://github.com/BenedictusKent/GarbageClassification.git
```

## Training
1. Load all images under ```img/own``` with size (224x224) and color.
2. Label images with the respective label by using integer.
3. Take 10% of the images of every classes as test images and the rest for training and validation ```(TRAINVAL)```.
4. Every image is augmented using the function provided by TensorFlow and added to ```(TRAINVAL)```.
5. 10% of ```(TRAINVAL)``` is taken as validation data and the rest as training data.
6. Train data using selected pre-trained model + fully connected layer.

## Result
### Accuracy
| Model         | Average of 3 runs | 5-fold Cross Validation |
| ------------- |:-----------------:| :----------------------:|
| MobileNetV2   | 93.13%            | 92.63%                  |
| MobileNetV1   | 92.88%            | 92.85%                  |
| Resnet50      | 93.64%            | 95.09%                  |  

### Model size
| Model         | Size    |
| ------------- |:-------:|
| MobileNetV2   | 41 MB   |
| MobileNetV1   | 49 MB   |
| Resnet50      | 294 MB  |  

### Time
Time to send image, predict, and receive answer from server:
| Model         | Time    |
| ------------- |:-------:|
| MobileNetV2   | 4 s     |
| MobileNetV1   | 4 s     |
| Resnet50      | 4 s     |  

## Future Update
1. 