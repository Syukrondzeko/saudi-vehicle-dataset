# Saudi Vehicles Dataset

A satellite imagery dataset for vehicle detection in Saudi Arabia, prepared
for the paper **“Vehicle Detection from Overhead Satellite Images in Saudi
Arabia with YOLOv12”** by Muhamad Syukron and Radical Rakhman Wahid.

The paper can be read and downloaded from the
[Journal of Engineering and Technological Sciences](https://jets.itb.ac.id/jets/article/view/856).

## Dataset contents

The dataset contains Google Maps overhead imagery
from Riyadh, Jeddah, Khobar, Dammam, and Buraydah. The images were collected are 500 × 500 pixels, and include zoom levels of 10 m and 20 m. The paper reports 5,609 vehicle annotations. Each vehicle has a bounding box and a single class, `vehicle`, in YOLO label format.

## Reproducing the paper's experiments

For the vehicle detection experiments, the paper used Ultralytics YOLOv12,
Python 3.10.2, Ultralytics 8.3.327, and Google Colab with an NVIDIA T4 GPU,
with a batch size of 16, a learning rate of 0.002, and a maximum of 200
iterations (the term used in the paper). The paper evaluated precision,
recall, F1-score, and mAP50. These settings describe the model experiments
and are not prerequisites for recreating the dataset files.
