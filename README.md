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
 ![Raw ECG Signal](images/raw_ecg_signal.png )
 The raw ECG signal contains baseline wander and high-frequency noise, which can negatively affect downstream analysis. 

 ### Cleaned ECG Signal 
 ![Cleaned ECG Signal](images/cleaned_ecg_signal.png )
 After preprocessing, the ECG waveform becomes significantly clearer, allowing more reliable heartbeat segmentation. 

 ### Multiple Heartbeat Segments 
 ![Multiple Heartbeats](images/multiple_heartbeats.png )
 This visualization shows several extracted ECG heartbeats, confirming consistent segmentation across different cardiac cycles. 

 ### Single Heartbeat Segment 
 ![Single Heartbeat](images/single_heartbeat.png )
 A single heartbeat segment is visualized to illustrate the fixed-length input provided to the neural network model. 

 ### ECG Beat with Grad-CAM 
 ![GradCAM ECG Beat](images/gradcam_ecg_beat.png )
 Grad-CAM highlights the regions of the ECG beat that contribute most to the model’s prediction, providing interpretability. 

 ### Grad-CAM – Normal Beat 
 ![GradCAM Normal](images/gradcam_normal.png )
 For normal heartbeats, the model primarily focuses on the QRS complex, which is clinically relevant. 

 ### Grad-CAM – Arrhythmic Beat 
 ![GradCAM Arrhythmia](images/gradcam_arrhythmia.png )
 For arrhythmic beats, Grad-CAM reveals different attention patterns, indicating that the model captures abnormal signal characteristics. 

 ##  Model Interpretation 
 The Grad-CAM visualizations demonstrate that the model bases its decisions on meaningful ECG regions rather than noise. 
 This improves trustworthiness and provides insight into the learned representations of the deep learning model. 

## Run Online (Colab)
You can run the full pipeline and experiments in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ali-mohamadpour/ecg-arrhythmia-detection/blob/main/ecg_arrhythmia_detection.ipynb)


