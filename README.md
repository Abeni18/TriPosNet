[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/sota/object-detection-on-ua-detrac-for/object-detection-on-ua-detrac)](https://paperswithcode.com/sota/object-detection-on-ua-detrac)  <br>
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/sota/object-detection-on-uavdt-for/object-detection-on-uavdt)](https://paperswithcode.com/sota/object-detection-on-uavdt)  <br>
# TriPosNet
#### Repository for the paper : "TriPosNet : Attention Based Keypoint Anchor-free Small-object Detection Framework"
#### The code will be available upon acceptance of the paper. 
## Abstract
Most object detection research focuses on identifying large objects covering a substantial portion of the image frame, while small object detection is often overlooked. Small objects, such as those commonly encountered in aerial computer vision, are challenging to detect and classify since they occupy a small percentage of the image. We propose TriPoslNet, a keypoint based object detection framework that employs a novel keypoint encoder and attention mechanism to enhance small object detection performance. The keypoint encoder addresses the representational imbalance between small and large objects by effectively encoding object information in a heatmap representation. The attention mechanism infers attention along both the spatial and channel axes, and then multiplies the attention maps with the input feature map to adaptively emphasize small object features. Using our proposed method, we achieve state-of-the-art performance on benchmark-dataset including UDETRAC and the UAVDT dataset, which primarily consists of small objects. 

## Model

![Framework](Arch/TriposNetPng.PNG "")

# Results

### Results on UA-DETRAC
- Prediction result from the trianed TriPosNet model is avaialble : [Prediction_result/UA-DETRAC](https://github.com/Abeni18/TriPosNet/tree/main/Prediction_result/UA-DETRAC)
- The summrized result is presented as follows

| Model                                      | Overall          | Easy             | Medium           | Hard             | Cloudy           | Night            | Rainy            | Sunny            |
|--------------------------------------------|------------------|------------------|------------------|------------------|------------------|------------------|------------------|------------------|
| TriPosNet (ours)                             | 88.43% | 97.83% | 93.12% | 79.81% | 91.37% | 90.29% | 83.24% | 91.32% |
| SpotNet                           | 86.80% | 97.58% | 92.57% | 76.58% | 89.38% | 89.53% | 80.93% | 91.42% |
| CenterNet | 83.48%          | 96.50%          | 90.15%          | 71.46%          | 85.01%          | 88.82%          | 77.78%          | 88.73%          |
| FG-BR\_Net         | 79.96%          | 93.49%          | 83.60%          | 70.78%          | 87.36%          | 78.42%          | 70.50%          | 89.8%           |
| HAT            | 78.64%          | 93.44%          | 83.09%          | 68.04%          | 86.27%          | 78.00%          | 67.97%          | 88.78%          |
| GP-FRCNNm         | 77.96%          | 92.74%          | 82.39%          | 67.22%          | 83.23%          | 77.75%          | 70.17%          | 86.56%          |
| R-FCN           | 69.87%          | 93.32%          | 75.67%          | 54.31%          | 74.38%          | 75.09%          | 56.21%          | 84.08%          |
| EB            | 67.96%          | 89.65%          | 73.12%          | 53.64%          | 72.42%          | 73.93%          | 53.40%          | 83.73%          |
| Faster R-CNN          | 58.45%          | 82.75%          | 63.05%          | 44.25%          | 66.29%          | 69.85%          | 45.16%          | 62.34%          |
| YOLOv2       | 57.72%          | 83.28%          | 62.25%          | 42.44%          | 57.97%          | 64.53%          | 47.84%          | 69.75%          |
| RN-D              | 54.69%          | 80.98%          | 59.13%          | 39.23%          | 59.88%          | 54.62%          | 41.11%          | 77.53%          |
| 3D-DETnet       | 53.30%          | 66.66%          | 59.26%          | 43.22%          | 63.30%          | 52.90%          | 44.27%          | 71.26%          |
