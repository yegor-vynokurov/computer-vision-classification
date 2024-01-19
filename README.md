# Computer vision classification

## And experiments with preprocessing of data

Task: Select what gives the best results for classification from the given architectural solutions. Check how class imbalance affects accuracy. Test the accuracy of the best model on balanced classes. Check the dataset for outliers and compare the training accuracy. Check how much the accuracy of the model changes if you use only the contours in the image instead of the original images.

Used Kaggle dataset: https://www.kaggle.com/datasets/gpiosenka/sports-classification 

# Conclusions

Best pretrain model: ResNet50.

On imbalanced dataset: Average accuracy on test dataset: 89.4 %

On balanced dataset: Average accuracy on test dataset: 89.6 %

With outliers deletion: Average accuracy on test dataset: 87.2 %

With edge detection: Average accuracy on test dataset: 57.4 %

We see that edge detecion as alone give bad results. 

Accuracy on balanced dataset is littlebit bigger. 

For balancing we used the same pictures. There was no increase in information, the frequency of classes in the batch was simply equalized. 

Excluding outliers from the dataset was supposed to increase accuracy, since among the outliers there were pictures with text instead of pictures, and most of the text, etc. But this did not happen with the pretrained model, since the amount of new information also decreased.

I tested the assumption that highlighting extreme contours can increase the accuracy of calibration. The results are negative. Even visually, most of the pictures are impossible to recognize. The neural network can't handle it either.
