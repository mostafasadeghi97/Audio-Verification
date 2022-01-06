# Voice Verification 


## Dependencies

- Python 3.6
- numpy
- librosa
- pysoundfile
- sounddevice
- matplotlib
- scikit-learn
- tensorflow
- keras

## Dataset

I Collected this data from friends and family. It contains numbers from 0-12 and 20 and 99



Example:

```
├── wav0
│  ├── 1.wav
│  ├── 2.wav
│  ├── 3.wav
│  ...
...
└── wav0
   ├── 0.wav
   ├── 1.wav
   ├── 2.wav
   ...
```

## Feature Extraction

Put audio files (`.wav` untested) under `data` directory and run the following command:

`python feat_extract.py`

Features and labels will be generated and saved in the directory.

## Classify with SVM

Make sure you have `scikit-learn` installed and `feat.npy` and `label.npy` under the same directory. Run `svm.py` and you could see the result.

## Classify with Multilayer Perceptron

Install `tensorflow` and `keras` at first. Run `nn.py` to train and test the network.

## Classify with Convolutional Neural Network

- Run `cnn.py -t` to train and test a CNN. Optionally set how many epochs to train on.
- Predict files by either:
  - Putting target files under `predict/` directory and running `cnn.py -p`
  - Recording on the fly with `cnn.py -P`
