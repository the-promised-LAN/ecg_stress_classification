# Stress Classification using single-channel ECG
VR Stress Assesment from proprietary dataset

## Main Approaches

Note: Using Leave-One-Subject-Out (LOSO) evaluation paradigm for all

### Models
1. InceptionTime architecture ([source repo](https://github.com/hfawaz/InceptionTime)) 
	- Regression (224x1 time-series input to 224x1 labels)
	- Original: Multiclass classification (224x1 input to 3-class output)
	
2. SE-Net variants
	- SE-ResNet14
	- ISE-ResNet14
	- ISE-Net matching Multi-ECG Classification paper

### Data Processing
- Time-series window: 1 second, 5 second, or 224-samples (1 R-R cycle)
- Post processing: Gramien Angular Fields (GAF), Markov Transition Fields (MTF), Recurrence Plots (RP)

## Files

#### Jupyter notebooks
- [data_exploration.ipynb](https://github.com/the-promised-LAN/ecg_stress_classification/blob/main/data_exploration.ipynb) - data exploration and statistics
- [inceptiontime_ecg.ipynb](https://github.com/the-promised-LAN/ecg_stress_classification/blob/main/inceptiontime_ecg.ipynb) - LOSO experiments with InceptionTime
- [se-net_3class.ipynb](https://github.com/the-promised-LAN/ecg_stress_classification/blob/main/se-net_3class.ipynb) - LOSO experiments with SENets

#### Other
- [InceptionTime.py](https://github.com/the-promised-LAN/ecg_stress_classification/blob/main/inceptionTime.py) - InceptionTime model 

## References
- InceptionTime - https://github.com/hfawaz/InceptionTime
