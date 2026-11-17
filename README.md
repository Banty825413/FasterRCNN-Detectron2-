# FasterRCNN-Detectron2

# Hard Hat Detection with Detectron2

Detects whether people are wearing a safety helmet, using Faster R-CNN (ResNet-50 FPN) fine-tuned with Detectron2 on a Roboflow hard hat dataset. The notebook runs end to end in Google Colab: dataset download, training, evaluation and inference on your own images.

What the notebook does
Installs Detectron2 and downloads the dataset from Roboflow (COCO format)
Registers the train and validation sets
Visualizes ground-truth boxes as a data sanity check
Fine-tunes a COCO-pretrained Faster R-CNN R50-FPN model
Evaluates with COCO metrics (AP, AP50, AP75)
Runs inference on uploaded images and gives a helmet / no-helmet result
Classes
Class	Meaning
head	Bare head, no helmet
helmet	Person wearing a helmet
Hard-Hat	Dummy parent class added by Roboflow; never predicted
Results (validation set)
Metric	Score
AP (IoU 0.50:0.95)	62.7
AP50	94.8
AP75	74.4
AP small / medium / large	52.6 / 70.7 / 76.5
AP head / helmet	62.2 / 63.2

Small or distant objects are the weakest area.

How to run
Open the notebook in Google Colab.
Set Runtime → Change runtime type → GPU.
Add your own Roboflow API key where the notebook downloads the dataset.
Run the cells in order.
