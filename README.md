# Real-Time Injury Risk Assessment in Athletes Based on Relative Joint Angles

This repository contains the implementation, datasets, and analysis for the paper "Real-Time Injury Risk Assessment in Athletes Based on Relative Joint Angles." The project leverages machine learning and computer vision techniques to assess injury risks based on athlete movements captured in video footage. The paper has been published in IEEE Xplore.

## Paper Link

Paper Link: [IEEE Xplore Paper](https://ieeexplore.ieee.org/document/10497417)  
DOI: [10.1109/ESCI59607.2024.10497417](https://doi.org/10.1109/ESCI59607.2024.10497417)

## Authors

- Bhuvi Ghosh
- Atharv Salian
- Harsh Shetye
- Parth Kapadia

## Introduction

This study proposes a real-time injury risk assessment method for athletes based on their relative joint angles. Traditional methods of injury risk assessment, such as manual observation and biomechanical analysis, have limitations in terms of accuracy, scalability, and objectivity. This paper introduces a data-driven approach leveraging pose estimation, joint angle computation, and machine learning classifiers to assess injury risk from video footage.

## Dataset Preparation

- **Videos**: The dataset consists of videos of athletes in motion during various track events, capturing a variety of movements.
- **Pose Estimation**: MediaPipe is used for extracting joint coordinates.
- **Features**: Joint angles (hip, knee, ankle) are calculated for both left and right limbs.
- **Preprocessing**: Videos are segmented into frames, and efforts are made to ensure diversity in running patterns and injury cases.
<div style="text-align: center;">
  <div style="display: inline-block; margin-right: 20px;">
    <img src="Readme image/image2.png" width="500" />
  </div>
</div>

## Methodology

- **Single-Frame Analysis**: Frame extraction is performed using OpenCV. Pose estimation and joint angle computation are followed by injury classification using LightGBM.
- **Multi-Frame Analysis**: Joint angle features are aggregated over multiple frames, with injury classification performed using Support Vector Machine (SVM).
- **Bootstrap Aggregating**: An ensemble method is used for final injury assessment, combining predictions from multiple models to improve reliability.

<div style="text-align: center;">
  <div style="display: inline-block; margin-right: 20px;">
    <img src="Readme image/image1.png" width="500" />
  </div>
</div>

## Statistical Analysis

- **Kolmogorov-Smirnov Test**: Used to validate the significance of joint angles as predictive markers.
- **Distribution Analysis**: Statistical tests are conducted to analyze the distribution of joint angles between injured and non-injured states.

## Model Performance

- **Comparison**: The performance of single-frame and multi-frame analysis approaches is compared.
- **Metrics**: Accuracy, precision, recall, and F1-score are used to evaluate model performance.
- **Best Approach**: The SVM-based multi-frame approach achieved the highest accuracy of 73.5%.

## Results

- The results demonstrate the feasibility of using video-based injury detection in athletes.
- Hyperparameter tuning for classifiers (e.g., LightGBM and SVM) is visualized to highlight the effectiveness of the chosen models.
- The model's generalizability and consistency across training and test datasets were confirmed through multiple validation tests.

## Conclusion

This work demonstrates the potential for using automated, scalable, and objective methods to assess injury risk in athletes. By combining computer vision and machine learning, the approach provides a viable tool for real-time injury risk assessment, with wide applications in sports medicine and injury prevention.

## Future Scope

- **Advanced Techniques**: Integration of more advanced methods such as vision transformers for improved pose estimation.
- **Dataset Expansion**: Incorporating richer datasets, including different sports and injury types, and larger-scale validations.
- **Cross-Sport Applications**: The methodology can be extended to various sports and motion analysis fields to assess injury risk.

## Installation

```bash
# Clone the repository
git clone https://github.com/bhuvighosh3/Real-Time-Injury-Risk-Assessment.git
cd Real-Time-Injury-Risk-Assessment

# Install dependencies
pip install -r requirements.txt
