## Introduction: 
This project aims to demonstrate how to directly load the saved model weights that have been trained on a set of household garbage image data[1], for use in any same type of image classification applications. Inside, **AlexNet, GoogLeNet, ResNet50** with various activation funtions (**GeLU, ReLU, Leaky_ReLU**) models have been trained and saved weights. Directly calling saved weights saves the process (usually more than 1 hour per model) of model training and allows predictions to be made right after building the model. The purpose of the high level is to expect that the model can correctly categorize garbage photographs, so as to correctly dispose of the garbage, and to alleviate the global environmental pressure.

[1] Pre-trained Dataset: https://www.kaggle.com/datasets/mostafaabla/garbage-classification

## Saved model weights storage
### All pre-trained weights have been uploaded to AWS S3, they can be accessed through the following links:

AlexNet model: https://danlee.s3.us-east-2.amazonaws.com/alex_weights.pth  
GoogLeNet model: https://danlee.s3.us-east-2.amazonaws.com/google_weights.pth  
ResNet50-GeLU: https://danlee.s3.us-east-2.amazonaws.com/g50clr_weights.pth  
ResNet50-ReLU: https://danlee.s3.us-east-2.amazonaws.com/r_weights.pth  
ResNet50-Leaky_ReLU: https://danlee.s3.us-east-2.amazonaws.com/lr_weights.pth  
ResNet50-GeLU(Step Learning rate & Epoch 50): https://danlee.s3.us-east-2.amazonaws.com/g50_weights.pth  
ResNet50-GeLU(Step Learning rate & Epoch 80): https://danlee.s3.us-east-2.amazonaws.com/g80_weights.pth  

### As well, aims for simple deployment, the project provides a small data with 120 images inside which can be imported from:
   https://danlee.s3.us-east-2.amazonaws.com/subsetdata/Subset.zip

## The steps to run pre-trained models in [Deployment.ipynb](https://github.com/danleezhu/CSCIDeep-Learning-Deployment/blob/main/Deployment.ipynb):

1. Import packages
2. Load a small data for deployment from AWS S3
3. Define test data prediction analysis (load saved model weights)
4. Define models, load weights, make prediction in order:  
   A. AlexNet  
   B. GoogLeNet  
   C. ResNet50-GeLU  
   D. ResNet50-ReLU  
   E. ResNet50-Leaky_ReLU  
   F. ResNet50-GeLU-Step Learning Rate(Epoch50)  
   G. ResNet50-GeLU-Step Learning Rate(Epoch80)  
5. Overall Comparison  

After finish these steps, the pre-trained models are loaded and used for predictions successfully.

## Any user can clone and run the project end-to-end through git clone command:
```
git clone https://github.com/danleezhu/CSCIDeep-Learning-Deployment.git
```
   

