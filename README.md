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

![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/ResNetRegCurve.png?raw=true)

## Regression Models Training Results with Artificial Urine
![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/CNNRegTrainModCompare.png?raw=true)

The best regression model performance was obtained using CNN-ResNet50. Coefficient of Determination on single test strip was 0.991, multiple test strip was 0.997, and all test strip was 0.999 on testing dataset. 

![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/ResNetConfMatrix.png?raw=true)

## Testing Results with Real Urine
After building and training the optimum CNN models, the models then testing into new dataset consists of urine test strip image that had been dipped into real urine sample. ResNet50 successfully achieve the optimum performance.

![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/TestingModelVGG16Class.png?raw=true)

In classification models, ResNet50 achieved an Accuracy score of 91.3% on single test strip images, 87.8% on multiple test strip images, and 93.5% on all test strip images. 

![alt text](https://github.com/fadindashafira/CNN_Smartphone_Urinalysis_VitaminC/blob/master/Images/TestingModelResNet50Reg.png?raw=true)

In regression models, ResNet50 achieved a Coefficient of Determination score of 0.956 on single test strip images, 0.919 on multiple test strip images, and 0.803 on all test strip images. 

## Conclusion
After building and testing the optimum CNN ResNet50 and VGG16 models, the results show that ResNet50 have a better architecture and deeper layer, therefore the models can learn feature much more than VGG16 models. 

These results indicate that the urinalysis colorimetry system based on smartphone cameras with ResNet50 is the optimum CNN model and can be used to measure urine Vitamin C with urine strip test images.

## Notes

Folders:

Classification Models: Python code

ClassificationReports: Report after train and build classification model

ClassificationTestingReports: Report of Testing on the best model

Datasets: images dataset in .hdf5 file

Images: images used in README.md file

Regression Models: Python code

RegressionReports: Report after train and build regression model

RegressionTestingReports: Report of Testing on the best model
