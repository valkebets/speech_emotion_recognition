# Speech emotion recognition



## Summary

The goal of this project is to build a deep learning model for emotion recognition from speech. We classify speech into 3 emotions (positive, negative, neutral), after extracting spectral and prosodic features from speech data coming from 5 open datasets. We also use data augmentation to increase the data size and make the model more generalizable. We first deploy 2 classic machine learning models (Support Vector Machine, Random Forest classifiers) to get a first benchmark, then we train a Convolutional Neural Networks model.


## Data

Speech data was downloaded from 5 open datasets:

* [Berlin Emo-DB database](http://www.emodb.bilderbar.info/download/) which includes 535 audio files spoken by 10 professional speakers (5 males and 5 females), displaying 7 emotions (anger, boredom, anxiety, happiness, sadness, disgust, and neutral). 

* [Crowd-sourced Emotional Mutimodal Actors Dataset (Crema-D)](https://github.com/CheyneyComputerScience/CREMA-D)
which includes 7442 clips of 12 sentences spoken by 91 actors (48 males and 43 females), between the ages of 20 and 74 coming from a variety of races and ethnicities, displaying 6 emotions (angry, disgusted, fearful, happy, neutral, and sad).

* [Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)](https://doi.org/10.1371/journal.pone.0196391)
which includes 1440 files (60 trials per actor x 24 actors). The RAVDESS contains 24 professional actors (12 female, 12 male), vocalizing two lexically-matched statements in a neutral North American accent, displaying 8 emotions (calm, happy, sad, angry, fearful, surprise, and disgust expressions).

* [Surrey Audio-Visual Expressed Emotion (Savee)](http://kahlan.eps.surrey.ac.uk/savee/Database.html)
which includes 480 clips recorded from four native English male speakers (identified as DC, JE, JK, KL), postgraduate students and researchers at the University of Surrey aged from 27 to 31 years, displaying 7 emotions (anger, disgust, fear, happiness, sadness and surprise, neutral).

* [Toronto emotional speech set (Tess)](https://tspace.library.utoronto.ca/handle/1807/24487) 
which includes 2800 files recorded by two actresses (aged 26 and 64 years) that spoke a set of 200 target words in the carrier phrase "Say the word _',  and diplaying 7 emotions (anger, disgust, fear, happiness, pleasant surprise, sadness, and neutral). 


## Usage

The notebook was tested on Python 3.9, using the Librosa and Parselmouth packages to analyze audio files, as well as Scikit-learn for ML models and Tensorflow for DL models.


## Future directions

Some ideas for future directions:

1. Developing a separate model for men and women

2. Add datasets:

- Danish Emotional Speech Database (DES)
- Interactive Emotional Dyadic Motion Capture (IEMOCAP)

3. Add features:

- energy (prosody)
- formants (high-frequency)
- spectrum centroid
- spectrum cut-off frequency
- correlation density (short-time speech signal spectral distribution)
- fractal dimension (nonlinearity of speech signal)
- Linear Predictor Coefficients (LPC)
- Mel Energy-spectrum Dynamic Coefficients (MEDC)
- Perceptual Linear Prediction cepstrum coefficients (PLP)

4. Apply dimensionality reduction to features

5. Try other DL architectures:

- ResNet
- multilayer perceptron
- RNN + Long Short Term Memory networks (LSTM)
- Deep Boltzmann Machine

6. Use end-to-end DL framework (i.e., no feature extraction)

