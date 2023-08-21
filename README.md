# GestureDetection

## Video Input
![Picture 1](https://github.com/Akshat5349/GestureDetection/assets/64729967/9345fd87-2ba5-4c57-8a48-b86afdfe66e4)

Video Stream is passed to the program via web camara using
VideoCapture module of OpenCV, then it is read using read
function of the module.

The reading of input is repeated by while loop with isOpened().

## Detection and Tracking

Detection and tracking of key points is performed with the help of mediapipe library.


## FILE SET-UP

In this part, the folder is set up for data collection for model training using makedirs() and path join function of os module.

<img width="97" alt="image" src="https://github.com/Akshat5349/GestureDetection/assets/64729967/47b06e21-b877-48b1-9199-7f2cfd5fce0f">

## DATA COLLECTION AND TRAINING 

![image](https://github.com/Akshat5349/GestureDetection/assets/64729967/bf7fc881-1d4d-4cc0-b714-9c85c92b410c)

For each action 30 frames are of key points are collected in a single data set and 30 such data are collected, then it is stored in the folder set up in the previous step using save() function of numpy.

![image](https://github.com/Akshat5349/GestureDetection/assets/64729967/3a6cce22-0dab-4000-9e79-a9aea6d6d80a)

Then it is loaded in array using load() function of numpy which is then fed to the LSTM model in training and predictions.

![image](https://github.com/Akshat5349/GestureDetection/assets/64729967/11334c1f-8423-4ea7-a041-8468d7884b4b)

Then the model is saved in actual program.

## PREDICTIONS

<img alt="image" src="https://github.com/Akshat5349/GestureDetection/assets/64729967/cd43013c-dded-45d8-81d9-bf200fba18fe">

The train model is loaded and is used to make predictions of probability of the detected sign of which the sign with maximum probability is appended to the sentence array.

![image](https://github.com/Akshat5349/GestureDetection/assets/64729967/b2b9ed1e-4ae7-4ff9-af92-81a51c381cb4)

This sentence array printed over the video stream of the program.

![image](https://github.com/Akshat5349/GestureDetection/assets/64729967/15115b3b-4cd0-4680-8ff3-ac168ac8a0c2)
