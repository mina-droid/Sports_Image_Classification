# Sports_Image_Classification Model

## Competition link (You must use this link to be able to join the competition): https://www.kaggle.com/t/f3e7c2ff1eff448c94b0f7753ddff60d

## Description:
In today’s world of internet, a massive amount of data is getting generated every day and content-based classification of images is becoming an essential aspect for efficient retrieval of images and have attracted application in several fields and one of such field is sports. Building a model that is able to classify different sports activities into different categories could be useful for automated sports analysis tasks.

## Evaluation:
The evaluation metric for this competition is Categorical Accuracy

## Submission Format:
The submission file should be a .csv file which contains two columns: image_name,label. The image_name is the imagename.jpg, the label is the predicted class and should be one of the following values: 0,1,2,3,4,5

Where Basketball --> 0 Football-->1 Rowing-->2 Swimming-->3 Tennis-->4 Yoga-->5
The submission should contain exactly 688 lines (for the 688 images in the test set). The image names don't have to be in a particular order but each image in the test set must have exactly one row in your submission file. The file should contain a header and have the following format:

image_name,label
0.jpg,4

1.jpg,0

## Dataset Description:
The full dataset can be found in this link: https://drive.google.com/file/d/1s07aL-7nvhO8ESJy_uTCZJMF5lw5LAGK/view?usp=share_link

The dataset is also uploaded to this Kaggle competition and can be used directly in Kaggle notebooks [Make sure the notebooks are private until the competition ends]

This folder consists of two main subfolders:

Train : contains 1681 images. The label is in the image name. Image format is a mix between .png and jpg

Test: 688 images without labels all jpg

## Report
Note: training accuracy always between 98%– 100%, in all models our goal was to solve overfitting.
## Trial 1: CNN Model
At first, we tried to implement the architecture found in LAB 7 in many ways as of changing the hyperparameters (filter size, number of filters, stride size, activation functions) as well as the number of layers (fully connected, convolution, maximum pooling), also adding regularization methods to prevent overfitting (batch normalization, dropout)

![Picture1](https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/8b2bbf1b-acb1-4910-9e14-4b5be9333571)


## Conclusion:

![Picture2](https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/3b637878-659e-454b-bda2-ffd38f6b0a16)

Public accuracy: 80%
Private accuracy: 78%
We began to understand what to do in case of overfitting, underfitting, understanding the process for hyperparameter tuning and how to deal with insufficient data.

## Trial 2: VGG16 Model (without weights)
We then tried to look online for models used to solve similar classification problems and found the VGG16 model, so we tried to implement its architecture but without weights

![Picture3](https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/624d4226-4298-4f6e-9764-9d973460dcc6)

## Conclusion:

![Picture4](https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/d5128f7d-9d82-4ab7-99e9-f755e54ec243)

Public accuracy: 76%
Private accuracy: 77%
We noticed that using the model without its weight achieved similar accuracy to trial 1 accuracy, so we tried to use transfer learning

## Trial 3: VGG16 Model (with weights)
We then saw that using the model’s pretrained weights that was trained on a dataset called ImageNet achieved higher accuracy

## Conclusion:

![Picture5](https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/dafc9648-a305-4cb8-a448-9eddc2cbfda7)

Public accuracy: 83%
Private accuracy: 82%
Using the model pre-trained weights achieved higher accuracy so we decided to always use the weights

## Trial 4: Xception Model (with weights) (Best Results)

We then decided to use the Xception Model and implement its architecture which achieved the highest accuracy in the ImageNet problem hoping to achieve higher accuracy in our problem

<img width="447" alt="Picture6" src="https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/f5e4750e-aba7-4812-9231-fce45ab81939">

## Conclusion:

![Picture7](https://github.com/mina-droid/Sports_Image_Classification/assets/62221411/d49938b4-5ed8-42a0-9662-2c210513d55d)

Public accuracy: 95%
Private accuracy: 93%
As expected, when we used the xception model with its pre-trained weights we achieved even higher accuracy than the VGG16 and that was the best accuracy we could achieve.
