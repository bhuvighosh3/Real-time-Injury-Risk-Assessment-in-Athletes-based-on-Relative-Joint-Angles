# Real-time-Injury-Risk-Assessment-in-Athletes-based-on-Relative-Joint-Angles

This repository contains the implementation, datasets, and analysis for the paper "Real-Time Injury Risk Assessment in Athletes Based on Relative Joint Angles". The project leverages machine learning and computer vision to assess injury risks from athlete movement captured in video footage.



## Paper Link

[https://ieeexplore.ieee.org/document/10497417](https://ieeexplore.ieee.org/document/10497417)
## Authors

- [@bhuvighosh3](https://github.com/bhuvighosh3)
- [@Atharv56](https://github.com/Atharv56)
- [@HarshShetye]
- [@ParthKapadia]


## Introduction

Explains the motivation for injury risk assessment in athletes.
Highlights the limitations of traditional methods and the advantages of machine learning.
Overview of the methodology, focusing on pose estimation and joint angle computation.


## Dataset Preparation

Description of the dataset, including:
- Videos of athletes in motion from various track events.
- Pose estimation using MediaPipe for extracting joint coordinates.
Features:
- Joint angles (hip, knee, ankle) calculated for left and right limbs.
Details on preprocessing steps, such as segmenting videos into frames and ensuring diversity in running patterns and injury cases.
## Methodology

- Single-Frame Analysis: Frame extraction using OpenCV. Pose estimation and joint angle computation. Injury classification using LightGBM.
- Multi-Frame Analysis: Aggregating joint angle features over multiple frames. Injury classification using SVM.
- Explanation of bootstrap aggregating for final injury assessment.
## Statistical Analysis

- Statistical tests (Kolmogorov-Smirnov) to validate the significance of joint angles as predictive markers
- Summary of distribution between injured and non-injured states.
## Model Performance

- Comparison of single-frame and mult-frame analysis approaches.
- Performance metrics: accuracy, precision, recall, F1-score.
- Highlight of the SVM-based multi-frame approach achieving the highest accuracy (73.5%).

## Results

- Key findings demonstrating the feasibility of video-based injury detection.
- Visualization of hyperparameter tuning for classifiers (e.g., LightGBM and SVM).
- Evidence of the model's generalizability and consistency across training and test data.
## Conclusion

- Summary of contributions, including automated, scalable, and objective injury risk assessment.
- Emphasis on the potential for real-world application and the role of AI in preventative sports medicine.
## Future Scope

- Possible improvements using advanced techniques like vision transformers.
- Integration of richer datasets and larger-scale validations.
- Potential applications in other sports and motion analysis fields.
