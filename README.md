# Real-Time-Sign-Language-Detection
Created a Sign Language Detector using Tensorflow, which uses pretrained model SSD MobileNet to detect different sign language words in real time.

## The whole process of developing the application consisted of the following phases:

### 1. Image Collection

In this phase, images were collected for training. Images captured from the webcam of laptop are purely of the developer
gesturing in sign language. After capturing the images, they were resized, cropped, and labelled using an annotation tool 
called LabelImg.

Below is a visual example of the developer gesturing the sign 'Wrong':

![wrong 8a04e089-68ed-11ed-bd2f-8038fb2f0103](https://user-images.githubusercontent.com/83728289/209449679-9557a09c-6603-4287-a921-aee81f386f51.jpg)


### 2. Data Labelling

For the process of Data Labelling, a graphical image annotation tool called LabelImg was used.
LabelImg is a free, open-source tool for graphically labelling images. It’s written in Python and uses QT 
for its graphical interface. It’s an easy, free way to label a few hundred images to try out your next object 
detection project.
Labels are used to segment out the Regions of Interest (ROIs), so that the model is able to identify the 
same, before the training process begins.


### 3. Setting up Object Detection Configuration

For every specific class, a label map was created which is used to generate training as well as testing record files. 
These are then used while configuring the TrainEvalPipeline.

The library used for creating this pipeline was TensorFlow Object Detection API. It is an open source framework 
built on top of TensorFlow that makes it easy to construct, train and deploy object detection models.

### 4. Training the Deep Learning Model

The model used in for this project is Single Shot Detector Model which is a pre-trained model (SSD) obtained through 
TensorFlow Model Zoo.

The model was configured to fit the dataset and to solve the problem at hand. The SSD model was trained for 10k training 
steps so as to ensure that the model performs with good accuracy score.


## Results:

Below are some visual examples of the results obtained:

![image](https://user-images.githubusercontent.com/83728289/209449733-f7bf4cf2-4b37-40a4-b580-d687fa0186f7.png)

![image](https://user-images.githubusercontent.com/83728289/209449734-9cb1b75d-3dae-4167-b36d-ff2f112ad260.png)

![image](https://user-images.githubusercontent.com/83728289/209449737-867c1404-2e42-4941-8c0b-c1c67f526e59.png)


