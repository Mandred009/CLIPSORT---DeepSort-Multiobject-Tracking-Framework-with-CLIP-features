# CLIPSORT: Multi-Object Tracking with CLIP Features

A from-scratch implementation of DeepSORT for multi-object tracking, featuring CLIP, DINOv2, and ResNet feature extractors.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

<p align="center">
  <img src="demo.gif" alt="CLIPSORT Demo" width="800"/>
</p>

- Complete Demo Video: https://youtu.be/DlhetgxPCvI
- Models and Related Files: https://drive.google.com/drive/folders/1C9SY023XiH443Ka4spOZOFqxh2otMKbx?usp=sharing

## Features

- **From-scratch DeepSORT** - Custom Kalman filter, cascade matching, Hungarian assignment
- **Multiple feature extractors** - CLIP, DINOv2, ResNet50
- **Zero-shot tracking** - No task-specific training required
- **Configurable** - YAML-based configuration

## Installation

```bash
git clone https://github.com/yourusername/CLIPSORT-DeepSort_Multiobject_Tracking_Framework_with_CLIP_features.git

cd CLIPSORT-DeepSort_Multiobject_Tracking_Framework_with_CLIP_features

pip install -r requirements.txt
```

## Files
```
├── main.py              # Entry point
├── deepsort.py          # Tracker implementation
├── kalman.py            # Kalman filter
├── yolo.py              # YOLO detector
├── clip_feature.py      # CLIP extractor
├── dino_feature.py      # DINOv2 extractor
├── resnet_feature.py    # ResNet extractor
├── config.yaml          # Configuration
└── requirements.txt
```

## Usage
- Run the main.py file and specify the path to the testing video in the script.
- Configure the yaml file to change the feature extractors or the hyperparameters.

## References
```
@inproceedings{wojke2017simple,
  title={Simple Online and Realtime Tracking with a Deep Association Metric},
  author={Wojke, Nicolai and Bewley, Alex and Paulus, Dietrich},
  booktitle={IEEE International Conference on Image Processing (ICIP)},
  year={2017},
  pages={3645--3649},
  organization={IEEE}
}
@inproceedings{radford2021learning,
  title={Learning Transferable Visual Models From Natural Language Supervision},
  author={Radford, Alec and Kim, Jong Wook and Hallacy, Chris and Ramesh, Aditya and Goh, Gabriel and Agarwal, Sandhini and Sastry, Girish and Askell, Amanda and Mishkin, Pamela and Clark, Jack and others},
  booktitle={International Conference on Machine Learning (ICML)},
  year={2021},
  pages={8748--8763},
  organization={PMLR}
}
@article{oquab2023dinov2,
  title={DINOv2: Learning Robust Visual Features without Supervision},
  author={Oquab, Maxime and Darcet, Timothée and Moutakanni, Théo and Vo, Huy and Szafraniec, Marc and Khalidov, Vasil and Fernandez, Pierre and Haziza, Daniel and Massa, Francisco and El-Nouby, Alaaeldin and others},
  journal={arXiv preprint arXiv:2304.07193},
  year={2023}
}
```
