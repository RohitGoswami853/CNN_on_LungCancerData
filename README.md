![](media/Banner.jpg)
#
# [Link of the Dataset-> Click Here](https://www.kaggle.com/datasets/adityamahimkar/iqothnccd-lung-cancer-dataset)


# About the dataset

The Iraq-Oncology Teaching Hospital/National Center for Cancer Diseases (IQ-OTH/NCCD) lung cancer dataset was collected in the above-mentioned specialist hospitals over a period of three months in fall 2019. 

It includes CT scans of patients diagnosed with lung cancer in different stages, as well as healthy subjects. 

IQ-OTH/NCCD slides were marked by oncologists and radiologists in these two centers. 

The dataset contains a total of 1190 images representing CT scan slices of 110 cases. 
These cases are grouped into three classes: normal, benign, and malignant. 
40 cases are diagnosed as malignant; 15 cases diagnosed with benign; and 55 cases classified as normal cases.

The CT scans were originally collected in DICOM format. The scanner used is SOMATOM from Siemens. CT protocol includes: 120 kV, slice thickness of 1 mm, with window width ranging from 350 to 1200 HU and window center from 50 to 600 were used for reading. with breath hold at full inspiration. 

All images were de-identified before performing analysis. Written consent was waived by the oversight review board. The study was approved by the institutional review board of participating medical centers. Each scan contains several slices. The number of these slices range from 80 to 200 slices, each of them represents an image of the human chest with different sides and angles. The 110 cases vary in gender, age, educational attainment, area of residence and living status. Some of them are employees of the Iraqi ministries of Transport and Oil, others are farmers and gainers. Most of them come from places in the middle region of Iraq, particularly, the provinces of Baghdad, Wasit, Diyala, Salahuddin, and Babylon.

# Approach

- Firstly the number fo image data was very low for a CNN model to work. So with data augmentation techinque (Keras prepocessing ImageDataGenerator) increase the data size (from 1500 to almost 4000.)

- Next change the image data to array with labels from the folder name (normal, benign, and malignant).
- Shuffle the data.
- Create a CNN model from tf.keras.Sequential().
- Add optimizer,loss function.
- Train and Evaluate the model.
- Predict.

# Libraries Used
![](media/Libraries.png)

![](media/data.png)

# CNN Model
![](media/model.png)

### After training the accuracy rate of the model is 86%, which means it can predict the data quite well.

![](media/Evaluate.png)

# Prediction

#### So the dataset contains a folder "Test" with no labels for actually verifing how good the model works.

![](media/prediction.png)

