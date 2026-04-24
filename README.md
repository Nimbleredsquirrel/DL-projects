# Deep Learning Projects

Case studies from a deep learning course covering regression, image classification, and object detection.

## Notebooks

**[Regression.ipynb](Regression.ipynb)**
Year-of-release prediction on the Million Song Dataset (90 audio features, continuous target). Two parts: a linear regression with manual gradient descent as a baseline (test RMSE 10.72), then a deep network with BatchNorm, GELU, Dropout, Adam + ExponentialLR scheduler (test RMSE 8.72, meets the ≤8.75 threshold).

**[Tiny ImageNet.ipynb](Tiny%20ImageNet.ipynb)**
Image classification on Tiny ImageNet (200 classes). Two parts: ResNet18 trained from scratch with AutoAugment and CyclicLR, reaching 44.7% accuracy; then ConvNeXt-Base pretrained on ImageNet1K with a frozen backbone and a replaced classifier head, reaching 84.1% accuracy. Both meet the required thresholds (0.44 and 0.84) for full marks.

**[YOLO (you only live once).ipynb](<YOLO%20(you%20only%20live%20once).ipynb>)**
Object detection on a small playing cards dataset (6 classes, ~300 images, PascalVOC format). Two approaches: a custom YOLO v1 implementation from scratch using a ResNet50 backbone with a 16x16 detection head and a hand-written multi-component loss (localization, box size, classification, confidence); and YOLOv8n from the ultralytics library trained for 50 epochs. The custom implementation is functional but unpolished; YOLOv8 gives noticeably cleaner detections.
