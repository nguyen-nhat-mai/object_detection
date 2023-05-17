# Computer Vision: Detection of dangerous objects in baggage to automate control at airports

## CRP ESSEC-Centralesupelec & Deloitte

## Group Members:
Vanshika SHARMA, Nhat Mai NGUYEN, Akshay SHASTRI, Léna AIX, Maxime MULOT


## Problem Description: 
The primary goal of this project is to detect various objects from X-ray images of baggage using deep learning-based object detectors. Currently, most airports and railway stations rely on manual inspections to view X-ray images of the bag to reveal its contents. The proposed system aims to automate this process with YOLOv5 as it provides real-time speed.

## Database:
This project uses images from the GRIMA database. 

## Object Classes:
We have annotated 14 types of objects from the images used in this project. The GRIMA database did not contain annotations for most of them. The types of objects used in this project are shown in the image below. The https://www.makesense.ai/ open-source web app was used as a tool for object annotation.

![Object class Labels](https://github.com/nguyen-nhat-mai/object_detection/blob/main/readme_images/labels.PNG)

## Train-Test Split:
This project used 900 images from the GRIMA database, 545 of which were used for training, 259 for validation and 96 for training. We enriched the train set using various types of augmentations.

## Object Detector:
A pre-trained YOLOv5m6 object detector from ![Ultralytics](https://github.com/ultralytics) trained on the Microsoft Common Objects in Context (MS COCO) dataset was used. The model was finetuned on the 900 images from the GRIMA database.

## Training Process Description:
The head of the model have been trained once on 100 epochs. Then, it has been finetuned by unfreezing all the layers with a smaller learning rate (please check the process guide for details).

## Results:
The sample detections obtained from the object detector are shown below.

![Sample Detections](https://github.com/nguyen-nhat-mai/object_detection/blob/main/readme_images/Final_result.PNG)


