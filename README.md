# kneron_yolov5
This repository contains benchmarks of YOLOv5, that i've done on NPU Kneron-720.

## Yolov5S
I used Kneron's best model as a baseline, they trained model for 600 epochs. All my models was trained for 600 epochs with standard training routine.
|        model         | image size |mAP @<br>IoU=0.5:0.95<br>fp32  |  mAP @<br>IoU=0.5:0.95<br>int8|  FPS on KL-720    | 
| :------------------: | :--------: |:----------------------------: | :----------------------------:| :---------------: | 
|Kneron's YOLOv5s-leaky|    640     |           0.361               |             0.315             |       24.36       | 
|   YOLOv5s-leaky      |    640     |           0.361               |             0.331             |       24.36       |
|   YOLOv5s-leaky      |    416     |           0.335               |             0.307             |       53.8        | 
|   YOLOv5s-leaky      |    352     |           0.315               |             0.288             |       73.8        | 

## Yolov5m
600 epochs, standard training routine.
|        model         | image size |mAP @<br>IoU=0.5:0.95<br>fp32  |  mAP @<br>IoU=0.5:0.95<br>int8|  FPS on KL-720    | 
| :------------------: | :--------: |:----------------------------: | :----------------------------:| :---------------: | 
|   YOLOv5m-leaky      |    640     |           0.432               |             0.400             |       10.10       |          
|   YOLOv5m-leaky      |    416     |           0.400               |             0.368             |       23.55       |                 
|   YOLOv5m-leaky      |    352     |           0.376               |             0.345             |       31.42       |         

## Yolov5m improved
300 epochs with standard training routine and 300 epochs with extended COCO dataset with previously unlabelled data, that i labelled using YOLOv5-x model.
|        model         | image size |mAP @<br>IoU=0.5:0.95<br>fp32  |  mAP @<br>IoU=0.5:0.95<br>int8|  FPS on KL-720    | 
| :------------------: | :--------: |:----------------------------: | :----------------------------:| :---------------: | 
|   YOLOv5m-leaky      |    640     |           0.444               |             0.406             |       10.10       |          
|   YOLOv5m-leaky      |    416     |           0.411               |             0.376             |       23.55       |                 
|   YOLOv5m-leaky      |    352     |           0.389               |             0.355             |       31.42       | 

