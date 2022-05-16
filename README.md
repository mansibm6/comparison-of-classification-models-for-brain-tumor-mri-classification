
# Classification of Brain Tumor MRI Scans using Deep Learning Models

In this project, we used images of brain MRI scans from human subjects to predict whether they had brain tumor and if so what kind of brain tumor.


## Authors

- [@mansibm6](https://www.github.com/mansibm6)


## Dataset

Dataset Link - [Brain Tumor MRI Scan Dataset](https://www.kaggle.com/sartajbhuvaji/brain-tumor-classification-mri)

The dataset was created by Sartaj Bhuvaji, Ankita Kadam, Prajakta Bhumkar, and Sameer Dedge to create an automated system in the Cloud that can detect tumors.
The dataset contains training and testing folders each of which has 4 classes of brain MRI scan images of jpeg format. The classes are:
- Glioma Tumor
- Meningioma Tumor
- No Tumor 
- Pituitary Tumor
The number of training and test images in each are:
- Glioma Tumor (train - 826, test - 100)
- Meningioma Tumor (train - 822, test -	115)
- No Tumor	(train - 395, test - 105)
- Pituitary Tumor	(train - 827, test - 74)


## Methodology

In our project, we applied transfer learning. We took two prebuilt models from the Keras Applications library and fine-tuned the models making all the layers fully trainable. We took the models EfficientNetB0 and MobileNetV3Small. EfficientNetB0 has 236 layers, all of which were made trainable. MobileNetV3Small has 234 layers, all of which were made trainable same as EfficientNetB0. EfficientNetB0 has almost 4 million parameters and MobileNetV3Small has around 1.5 million parameters. What this means is that the network architectures will remain the same but the weights and biases of the neurons of each layer will change based on the training it will go through on our dataset. 

We found that the EfficientNetB0 model got an overall accuracy of 76.14% on the test dataset. On the other hand, the MobileNetV3Small model got an overall accuracy of 73.35% on the test dataset.
## Conclusion

From the confusion matrix, we came to know that the EfficientNetB0 model had greater True Positives for 3 of the 4 classes. However, the F_1 scores for No Tumor and Pituitary Tumor classes are higher for the MobileNetV3Small model and the F_1 scores for Glioma Tumor and Meningioma Tumor classes are higher for the EfficientNetB0 model. The model size for the EfficientNetB0 model came to 47 MB while the model size for MobileNetV3Small came to only 18.1 MB. The EfficientNetB0 model got an overall accuracy of 76.14% on the test dataset. On the other hand, the MobileNetV3Small model got an overall accuracy of 73.35% on the test dataset. Although the EfficientNetB0 model got a greater accuracy, it is by a very small margin. Less than 3% better. We can take this as a tradeoff and conclude that MobileNetV3Small is a better model to use in real-world applications due its smaller size but very little trade-off in accuracy to EfficientNetB0. 
We got a brief overview of the evaluation metrics, our results and lastly, we concluded which network will work better in real life.
