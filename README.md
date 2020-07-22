# Construction Worker Safety Equipment Detection
[![TensorFlow 1.15](https://img.shields.io/badge/TensorFlow-1.15-FF6F00?logo=tensorflow)](https://github.com/tensorflow/tensorflow/releases/tag/v1.15.0)
[![Python 3.6](https://img.shields.io/badge/Python-3.6-3776AB)](https://www.python.org/downloads/release/python-360/)

<p align="center">
  <img src="/docs/predict.png" width="40%">
</p>

Detecting Construction Worker Safety Equipment (Helmet and Vest) using Tensorflow Object Detection API for Tensorflow 1

## How to use
* Install [Tensorflow Object Detection API for Tensorflow 1](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1.md)
* Install Tensorflow 1.15
if you are using anaconda, you can install it with

```bash
conda install tensorflow-gpu=1.15
```

for tensorflow built for gpu, or if you want CPU-only tensorflow

```bash
conda install tensorflow=1.15
```
if you are using pip

```bash
pip install tensorflow=1.15
```
I recommend you to use the GPU version for performance reason
* clone this repository

```bash
git clone git@github.com:jerrylasama/Construction-Worker-Safety-Equipment-Detection.git
```

* run the detect.py after you install the requirements

## Training the model
* Install [Tensorflow Object Detection API for Tensorflow 1](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1.md)
* Install Tensorflow 1.15
* I used [faster_rcnn_inception_v2_coco](http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_v2_coco_2018_01_28.tar.gz) for this model, you can also use other model if you don't want to retrain the model provided here. But if you want to retrain the model provided here, you can replace the pipeline.config and model checkpoint using the one I provided here.
* Edit the pipeline config paths
* For more references please refer to [Tensorflow Object Detection API GitHub](https://github.com/tensorflow/models/tree/master/research/object_detection)


## Evaluation Results
The model was trained for 200k steps, and yield 0.48 coco mAP

### Precision
![Precision](/docs/DetectionBoxes_Precision.png)

### Recall
![Recall0](/docs/DetectionBoxes_Recall0.png)
![Recall1](/docs/DetectionBoxes_Recall1.png)

### Loss
![Loss](/docs/Loss.png)
