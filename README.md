# Signal Processing in BCI

This repository contains a project developed during my Master's in Bioinformatics. The project focuses on signal processing techniques applied to Brain-Computer Interface (BCI) data, specifically analyzing EEG signals from motor tasks.

## Dataset

The dataset used in this project consists of EEG recordings from subjects performing grasp-and-lift (GAL) trials. Key details about the dataset include:

- **Source**: Luciw MD, Jarocka E, Edin BB (2014). Multi-channel EEG recordings during 3,936 grasp and lift trials with varying weight and friction. *Scientific Data* 1:140047.
- **Subjects**: 12 individuals, each with 10 series of trials.
- **Trials**: Approximately 30 trials per series (varies slightly).
- **Events**: Six events detected during each trial:
  - HandStart
  - FirstDigitTouch
  - BothStartLoadPhase
  - LiftOff
  - Replace
  - BothReleased

### Data Format

The data is stored in CSV files:
- `*_data.csv`: Contains raw EEG data from 32 channels (sampling rate: 500Hz).
- `*_events.csv`: Contains ground truth labels for the six events.

## Project Description

This project implements signal processing and machine learning techniques to analyze and classify EEG signals. The main steps include:

1. **Preprocessing**:
   - Loading EEG data using Python libraries such as `mne`.
   - Filtering and normalizing the signals.

2. **Feature Extraction**:
   - Applying methods like Common Spatial Patterns (CSP) to extract relevant features from the EEG data.

3. **Classification**:
   - Using machine learning models such as Linear Discriminant Analysis (LDA) to classify events.
   - Evaluating model performance using cross-validation techniques.

4. **Visualization**:
   - Plotting topographical maps of brain activity.
   - Visualizing signal spectra using tools like Welch's method.

## Dependencies
The project relies on the following Python libraries:

- `numpy`
- `pandas`
- `mne`
- `matplotlib`
- `scikit-learn`
- `scipy`

