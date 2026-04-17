# MS-285
Project Overview for final project in MS 285.

## Project Title
Training a YOLO model to detect sea otters (possibly seals?) in drone images. 

## Motivation
The research question that I will be attemping to answer in this project will be: Can a YOLO model consistently and accurately identify individual sea otters from drone images. This question is important because for my thesis my dataset will primarily consist of drone images from weekly scans over 52 weeks. This is a large amount of data, however, if a YOLO model can be trained to consistently and accurately detect sea otters in these images it will help my data analysis immensenly. It will not only reduce the amount of time it takes for me to analyze the images from one drone scan, but also may pick up on others that were hard for me to spot within the images. 

## Data
The dataset I will be using for my thesis will consist of aerial images from weekly drone scans occuring over approximately 52 weeks. The drone will be following an autonomous flight path for each site in Monterey Bay and Elkhorn Slough and taking a photo every 2 seconds. I am currently in the process of creating these maps so the number of photos for each site is currently unknown. My thesis had been stalled by permitting issues so I have not conducted any drone flights over otters, I have reached out to a researcher who has to see if I can borrow their images but have yet to hear back. For the sake of this project I may be using a dataset from researchers at Año Nuevo that took aerial images of elephant seals hauled out on shore. Those photos are currently stored in google drive folders labeled with the date of the drone flight and range from 60 to >100 photos per flight. I can't share the full dataset as I do not own it but have one folder in my google drive so it can be viewed as an example: https://drive.google.com/drive/folders/1j0RATMSJ1JQXpIDu4vOAvl3tFahqiVBA?usp=share_link.

## Model
As previously stated in my question I will be using a "You Only Look Once" model or as it is better known a YOLO model. To train the YOLO model I will provide it with a dataset of photos and then exexcute a training script. The hope is that in time and with the right prompts I will be able to get the model to consistently and accurately determine where the sea otters are present in the drone images. This model makes the most sense for my project due to my use of images as my dataset and the fact that the goal is to count each individual otter in the photos. With the use of this model, the counting process has the potential to be more efficient and perhaps more accurate. Sea otters amongst the kelp are sometimes hard to identify from an aerial point of view so I hope that this may be a useful tool for my thesis. I believe that the loss function I will use to evaulate my model will be a composite loss function due to the fact that this function simultaneously optimizes object localization and classification.

## Analysis
There are a couple of ways to evaulate the model I chose for this project. My first thought was to do a confusion matrix, but all that would really show me is how many otters were correctly identified and how many were incorrectly identified. If I truly want to evaluate the consistency and accuracy of my model the best thing to do would be to evaluate the total loss terms. If this value decreases as I train my model, it shows that my model is accurately and consistently identifying sea otters. However, if the value increases or does not change then I need to reevalute the model or my training script. This is important to my question because if the model does not create a more efficient way to identify sea otters then it may not be worth it to use in my project. If the model is accurate, consistent, and efficient then it could improve my analysis for my thesis. 





