# Saudi Vehicles Dataset

A satellite imagery dataset for vehicle detection in Saudi Arabia, prepared
for the paper **“Vehicle Detection from Overhead Satellite Images in Saudi
Arabia with YOLOv12”** by Muhamad Syukron and Radical Rakhman Wahid.

The paper can be read and downloaded from the
[Journal of Engineering and Technological Sciences](https://jets.itb.ac.id/jets/article/view/856).

## Download

The dataset is hosted on Zenodo:
**<https://zenodo.org/records/24388620>**

Download `saudi_vehicle_dataset.zip` and unzip it. It has this structure:

```
saudi_vehicle_dataset/
├── train/                 # 317 images + YOLO labels
│   ├── images/
│   └── labels/
├── val/                   # 71 images + YOLO labels
│   ├── images/
│   └── labels/
├── test/                  # 112 images + YOLO labels
│   ├── images/
│   └── labels/
└── buraydah_unlabeled/    # 100 extra Buraydah images, no labels yet
```

The images in `buraydah_unlabeled/` were not used in the paper's
experiments.

The annotations are released under CC BY 4.0. The images are Google Maps
satellite imagery, © Google and its imagery providers. They are not covered
by the CC BY 4.0 license and are included for non-commercial research only.

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
