
# Human Activity Recognition

## Intro

There are 

* 8 subjects
* 19 activities
* 60 segments per activity per individual
* 45 sensor readings
* 125 samples per segment


Therefore, for our CNN, each sample can be a 125x45 pixel image. There are a total of 60 * 8 = 480 samples per activity. and 480 * 19 = 9120 total samples to work with.

### Data

Data is available at the [UCI machine learning repository](https://archive.ics.uci.edu/ml/datasets/Daily+and+Sports+Activities)

### Current Results

According to [this paper](http://kilyos.ee.bilkent.edu.tr/~billur/publ_list/cj14.pdf) the best results for accelerometer-only sensor use are

RRSS: 93.3 +- 0.48
10-fold: 95.5 +- 0.12
LIO: 81.0 


## Goal:

See how close a CNN using resnet34 does compared to these results, for only accelerometer.


## My Results

With a CNN, I achieved a **98.7%** accuracy. That is 3% higher than the highest achieved by the other methods used in the paper.

### Methods

Refer to preprocess_data.ipynb to see how the data was created, and RecNet.ipynb to see the training and results.
