# BreastCancerDetection

This project was done for my Bachelor Thesis named "Detecting breast cancer using deep neural networks techniques" for the University of Macedonia in Greece under superisvor Ioannis Refanidis. 

Dataset that was used : https://www.kaggle.com/paultimothymooney/breast-histopathology-images.

The original dataset consisted of 162 whole mount slide images of Breast Cancer (BCa) specimens scanned at 40x. From that, 277,524 patches of size 50 x 50 were extracted (198,738 IDC negative and 78,786 IDC positive). Each patch’s file name is of the format: uxXyYclassC.png — > example 10253idx5x1351y1101class0.png . Where u is the patient ID (10253idx5), X is the x-coordinate of where this patch was cropped from, Y is the y-coordinate of where this patch was cropped from, and C indicates the class where 0 is non-IDC and 1 is IDC.

Metholodogy/Implementation : In order to try to classify the image as best, Convolutional Neural Networks were used to reduce the size of image while keeping the important features, and after using a fully-connected network to classify the patches. The metric that should be taken into account for this type of problems for unbalanced data is the F1-Score. The model that achieved the best score F1-Score was using 4 layers of CNN's with 32,64,128,256 kernels each following by max pooling after each layer but the last, to reduce it to 6x6 pixels eventually and apply the FC network on thi s image instead. Best F1-Score achieved after 39 epochs of training.

