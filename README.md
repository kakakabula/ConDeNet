# ConDeNet
# ConDeNet Official Repository
Official code & PUOD-3K dataset for the paper:
**Context-Detail Dual-path Fusion Network for Pavement Uneven Object Detection via Scale-adaptive Attention and Dynamic Channel Allocation**

## PUOD-3K Dataset
### 1. Dataset Overview
To address the challenge of multi-class pavement uneven object detection under complex real-world road scenes, we build a self-collected pavement uneven object detection dataset named PUOD-3K.
All images are captured by vehicle-mounted cameras covering urban roads, suburban roads, vehicle test tracks, campus and factory zones, supplemented with open non-commercial road pictures from the internet.

The dataset focuses on four typical pavement uneven objects: speed humps, manhole covers, potholes and puddles. Different from most existing public pavement datasets that only support single-category defect detection, PUOD-3K contains abundant samples with huge scale gaps, irregular outlines, variable lighting conditions and cluttered background interference. It can be used for autonomous driving road preview perception, pavement condition inspection and multi-class road anomaly detection tasks.

### 2. Dataset Basic Information
- Total image quantity: 3074
- Original image resolution: 1920 × 1080
- Train / Val / Test split ratio: 4 : 1 : 1
- Annotation format: COCO JSON
- Category label distribution:
  - Speed hump: 28.69%
  - Manhole cover: 20.02%
  - Pothole: 20.02%
  - Puddle: 31.26%
- Unified training input size: 640 × 640
- Training augmentation strategies: Mosaic, horizontal flip

### 3. File Structure of Dataset
```
data/
├── train/                # Training set images
├── val/                  # Validation set images
├── test/                 # Test set images
└── annotations/          # COCO format label files
    ├── train.json
    ├── val.json
    └── test.json
```

### 4. Dataset Download
The complete PUOD-3K dataset exceeds 100MB, which cannot be fully stored in GitHub. We provide the full compressed package via cloud disk for download:
> Cloud disk download link: [[https://pan.baidu.com/s/1iGDUp66nR5KUTWnh1uOwdw]]
> Extraction code: [c8in]

#### Usage Instructions
1. Download the compressed file from the above link;
2. Unzip the file and place the `data` folder directly into the root directory of this repository;
3. You can start training, verification and inference with the dataset.

#### Small Sample Preview on GitHub
A small number of sample images and partial annotation demos are stored in this repo for preview. If you need the complete training dataset, please download it from the cloud disk link above.

### 5. Dataset Limitations
1. Ultra-tiny distant targets: Faraway manhole covers occupy very few pixels with weak feature information, which may cause missing detection or low confidence prediction.
2. Confusing background interference: Roadside isolation belts with warning strips share similar texture features with speed humps, easily leading to false positive detection.

In future work, we will expand the dataset scale and add more hard samples to further improve the model’s robustness against tiny objects and confusing backgrounds.

### 6. Dataset License
The PUOD-3K dataset is released under **CC-BY 4.0 License**.
You are allowed to use, copy, distribute and modify this dataset for academic research and commercial applications, as long as you clearly cite our paper and this open-source repository.

## Citation
If you utilize the PUOD-3K dataset or ConDeNet model in your research, please cite our work:
```
@article{wang2026condenet,
  title={Context-Detail Dual-path Fusion Network for Pavement Uneven Object Detection via Scale-adaptive Attention and Dynamic Channel Allocation},
  author={Xuewei Wang, Yongxin Cao, Xiao Liang, Shaohua Li, Siyuan Li},
  journal={XXX},
  year={2026}
}

@misc{kakakabula2026condenet,
  title={ConDeNet: PUOD-3K Dataset and Dual-Path Detection Code for Pavement Uneven Objects},
  author={kakakabula},
  year={2026},
  publisher={GitHub},
  howpublished={\url{https://github.com/kakakabula/ConDeNet}}
}
```
## Reference link
Wang, X., Cao, Y., Liang, X., Li, S., & Li, S. Context-detail dual-path fusion network for pavement uneven object detection via scale-adaptive attention and dynamic channel allocation. Engineering Applications of Artificial Intelligence, 2026, 182(2), 115995. https://doi.org/10.1016/j.engappai.2026.115995

## Acknowledgement
This work is supported by the National Natural Science Foundation of China (52572481, U22A20246), the Natural Science Foundation of Hebei Province (F2025210053, F2024210051), Science and Technology Project of Hebei Education Department (HJYB202516, BJK2024128).

## Contact
If you have questions about dataset download, annotation standards or experimental reproduction, please contact the corresponding author.
