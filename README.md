 # ECG Arrhythmia Detection 

 Deep Learning–based ECG Arrhythmia Detection using the MIT-BIH Arrhythmia Dataset. 

 ##  Overview 
 This project implements an end-to-end deep learning pipeline for automatic detection of cardiac arrhythmias from ECG signals. 
 The notebook covers signal preprocessing, heartbeat segmentation, deep learning–based classification, and model interpretation. 
 All results and visualizations shown below are directly generated from the provided code. 

 ##  Dataset 
 - MIT-BIH Arrhythmia Database 
 - Sampling rate: 360 Hz 
 - Source: PhysioNet 

 ##  Signal Processing Pipeline 
 1. ECG signal loading using WFDB 
 2. Signal preprocessing and noise removal 
 3. Heartbeat segmentation 
 4. Deep learning–based classification 
 5. Model interpretation using Grad-CAM 

 ##  Results and Analysis 

 ### Raw ECG Signal 
 ![Raw ECG Signal](IMG/raw_ecg_signal.png )


 ### Cleaned ECG Signal 
 ![Cleaned ECG Signal](IMG/cleaned_ecg_signal.png )

 ### Multiple Heartbeat Segments 
 ![Multiple Heartbeats](IMG/multiple_heartbeats.png )

 ### Single Heartbeat Segment 
 ![Single Heartbeat](IMG/single_heartbeat.png )

 ### ECG Beat with Grad-CAM 
 ![GradCAM ECG Beat](IMG/gradcam_ecg_beat.png ) 

 ### Grad-CAM – Normal Beat – Arrhythmic Beat 
 ![GradCAM Normal](IMG/gradcam_normal_arrhythmia.png )


 ##  Model Interpretation 
 The Grad-CAM visualizations demonstrate that the model bases its decisions on meaningful ECG regions rather than noise. 
 This improves trustworthiness and provides insight into the learned representations of the deep learning model. 

## Run Online (Colab)
You can run the full pipeline and experiments in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ali-mohamadpour/ecg-arrhythmia-detection/blob/main/ecg_arrhythmia_detection.ipynb)

##  Project Analysis and Insights

This project implements a fully end-to-end ECG analysis pipeline, starting from raw ECG signals and progressing through preprocessing, heartbeat segmentation, deep learning–based classification, and model interpretability.

Signal preprocessing plays a critical role in improving ECG quality by reducing noise and baseline wander, which enables more reliable heartbeat segmentation and model input preparation.

Heartbeat segments are extracted around detected cardiac cycles and normalized to a fixed length to ensure consistency across samples when fed into the convolutional neural network.

To improve transparency and trustworthiness, Grad-CAM is employed to visualize which regions of the ECG signal contribute most to the model’s predictions. The resulting visualizations indicate that the model focuses on clinically meaningful regions, such as the QRS complex, rather than noise-dominated areas.

This implementation is designed for research and educational purposes and demonstrates how deep learning models can be combined with signal processing and interpretability techniques for ECG analysis.

