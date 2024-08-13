# Glove Detection with Yolov5 on Intel OpenVINO

![glove 6](https://github.com/user-attachments/assets/5d0d29ca-5d15-4bcf-9620-87bec78cb48d)

this is a ipynb demo for detecting glove defects using opoenvino
repo is provided by Allen (@allenwsh)

deploy the .ipynb script on Google colab and run.

# Description

Glove Defect Detection using Open-Source YoloV5 and OpenVINO
Use Case Requirement: To detect glove defects (touching, hole). 

The use case was experimented with some original images sample. For this showcase, l used CVAT (A open-sourced tool co-developed by Intel) to annotate and label the images. 3 labels were assigned (defect, glove missing and glove detected)

For training, an alternative to Intel developer tools would be using public pre-trained models. My choice was YoloV5 by Ultralytics. A new custom model is developed using pre-trained weights of Yolov5s on COCO128.

Next, the model was downsampled (FP32 to FP16) and optimised using OpenVINO Model Optimizer. This would provide us with the Intermediate Representation (IR) files required to run inferencing on OpenVINO IE Runtime.

Initial test results: Able to detect the anomalies and glove though with less than optimum conf threshold. Granted, our dataset has a small sample size and I'm not professional AI Engineer =P.

![glove1](https://github.com/user-attachments/assets/7e1366c3-86f0-4dbf-9c4f-806512ca7527)

![glove2](https://github.com/user-attachments/assets/c51e7a5c-2034-429a-aa3d-fc94a190700a)

![glove3](https://github.com/user-attachments/assets/1deab884-38f3-47ef-ac36-dbd14df4e808)

![glove5](https://github.com/user-attachments/assets/a002b767-0da1-4ede-90b4-9aa1aab9cc85)
