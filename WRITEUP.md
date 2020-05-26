# Edge People Counter App

This app is a people counter app deployed at the edge. The app detects people in the frame, the average time they spend in the frame and also counts the total number of people that have been through the frame. 

## Processing Custom Layers

The model used for this project is the Faster rcnn inception v2 trained on the coco dataset. Model was downloaded from the Tensorflow Objct detection model Zoo and no additional processing was done to the custom layers. 

##  Model Performance

I tested one model, the Faster_rcnn_inception_v2_coco_2018_01_28 for this app as I was satisfied with it's performance in making inference. I compared model performance by comparing Latency and memory of the model before and after conversion to Intermediate representation. 

* Latency before conversion 1271ms
* Latency after conversion 889ms

* Memory before conversion 562mb 
* Memory after conversion 281mb 

## Assess Model Use Cases

Some of the potential use cases of the people counter app are; To help improve Access control of a building by keeping track of people coming and going, Concerts control to stick to the capacity of venue.

Each of these use cases would be useful because it would help prevent unwanted access to building and also help prevent overcrowding at events. 

## Assess Effects on End User Needs

Lighting, model accuracy, and camera focal length/image size have different effects on a deployed edge model. The potential effects of each of these are as follows:

* If lighting is too dim or if model is to be used in the dark, more work would have to go into selecting the right model or including some custom layers to improve inference in low light conditions. 

* If model accuracy is poor, then it would probably not identify everyonee passing through the frame and would end up being redundant and can lead to overcrowding.

* If focal length is increased, model might be too narrow and not capture the full frame, miss some people in the frame and if decreased can reduce inference power of model.