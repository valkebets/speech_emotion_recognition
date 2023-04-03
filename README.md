# Speech emotion recognition



## Summary

This notebook is partly based on [Shivam Burnwal's Kaggle notebook] (https://www.kaggle.com/code/shivamburnwal/speech-emotion-recognition)

I modified and extended it for my own use:

* classification of 3 emotions (positive, negative, neutral) instead of 7 emotions from the original datasets (e.g., happy, sad, angry, fearful, disgusted, surprised, neutral)
* extraction of prosodic features
* modelling included classic machine learning models (Support Vector Machine, Random Forest classifiers), and more recent deep learning models (Convolutional Neural Networks (CNNs).


## Data

Speech data was downloaded from 5 open datasets:

* [Crowd-sourced Emotional Mutimodal Actors Dataset (Crema-D)](https://github.com/CheyneyComputerScience/CREMA-D)
which includes 7442 clips of 12 sentences spoken by 91 actors (48 males and 43 females), between the ages of 20 and 74 coming from a variety of races and ethnicities, displaying 6 emotions: angry, disgusted, fearful, happy, neutral, and sad

* [Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)](https://doi.org/10.1371/journal.pone.0196391)
which includes 1440 files (60 trials per actor x 24 actors). The RAVDESS contains 24 professional actors (12 female, 12 male), vocalizing two lexically-matched statements in a neutral North American accent, displaying 8 emotions (calm, happy, sad, angry, fearful, surprise, and disgust expressions).

* [Surrey Audio-Visual Expressed Emotion (Savee)](http://kahlan.eps.surrey.ac.uk/savee/Database.html)
which includes 480 clips recorded from four native English male speakers (identified as DC, JE, JK, KL), postgraduate students and researchers at the University of Surrey aged from 27 to 31 years, displaying 7 emotions (anger, disgust, fear, happiness, sadness and surprise, neutral).

* [Toronto emotional speech set (Tess)](https://tspace.library.utoronto.ca/handle/1807/24487) 
which includes 2800 files recorded by two actresses (aged 26 and 64 years) that spoke a set of 200 target words in the carrier phrase "Say the word _',  and diplaying 7 emotions (anger, disgust, fear, happiness, pleasant surprise, sadness, and neutral). 


## Features

I extracted spectral and prosodic features from the data, after augmenting the data to increase training data.


## Usage

The notebook was run on Python 3.9, using the Librosa and Parselmouth packages to analyze audio files, and Tensorflow Keras for DL modelling.



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

