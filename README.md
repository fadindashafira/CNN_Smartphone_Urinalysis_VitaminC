# CNN_Smartphone_Urinalysis_VitaminC

## Introduction
Stunting is a condition of impaired growth and development that children experience caused by low nutrional intake, starting from fetus until the first 1,000 days of life.  One indicator that cause malnutrition is a lack of Vitamin C. Vitamin C is a water-soluble vitamin and excreted in the urine. A urine Vitamin C level less than 1.12 mmol/L, indicates that the patient is deficient in Vitamin C intake. Therefore, early detection is needed to monitor adequate intake of Vitamin C in pregnant women. 

![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/UrinalysisSystem.png?raw=true)

## Urinalysis System
In this study, a Vitamin C urinalysis colorimetric system based on test strip images was developed using CNN (Convolutional Neural Network). Two CNN models, ResNet-50 and VGG16, were build and compared. The image input was captured using the Samsung Galaxy A72, Samsung Galaxy A31, Huawei Nova 5T, and Vivo Y12 smartphone cameras. The image acquisition process uses an image housing box consisting of a LED, reference color board, and a test barcode (the test strip is cut into two equal parts). The image is color corrected using the Polynomial Color Correction (PCC) model using MATLAB. Then, the image is used to train the CNN models in python.

![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/ImageInputForm.png?raw=true)

The input image forms are varied into single analyte images, multiple analytes, all analytes. 

## Build the Models
![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/BuildModelCNN.png?raw=true)

The system output is 5 classes and urine Vitamin C contents (0-5.6 mmol/L). The artificial urine strip test image dataset used for building the model and split into three parts: Testing, Training, and Validation. The optimal models were tested using real urine strip test image dataset. The metrics used for evaluation are Accuracy, Coefficient of Determination (R^2), and RMSE (Root Mean Squared Error).

## Classification Models Training Results with Artificial Urine
![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/CNNClassTrainModCompare.png?raw=true)

The best classification model performance was obtained using CNN-ResNet50. Accuracy of single test strip was 97.7%, multiple test strip was 99.5%, and all test strip was 99.9% on testing dataset. 

(https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/ResNetRegCurve.png?raw=true)

## Regression Models Training Results with Artificial Urine
![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/CNNRegTrainModCompare.png?raw=true)

The best regression model performance was obtained using CNN-ResNet50. Coefficient of Determination on single test strip was 0.991, multiple test strip was 0.997, and all test strip was 0.999 on testing dataset. 

(https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/ResNetConfMatrix.png?raw=true)

## Testing Results with Real Urine

(https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/TestingModelVGG16Class.png?raw=true)
(https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/TestingModelResNet50Reg.png?raw=true)

These results indicate that the urinalysis colorimetry system based on smartphone cameras and VGG16 can be used to measure urine Vitamin C with urinalysis barcode images.
