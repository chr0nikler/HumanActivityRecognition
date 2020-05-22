
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

According to [this paper](http://kilyos.ee.bilkent.edu.tr/~billur/publ_list/cj14.pdf) the best results for all sensor use are

RRSS: 99.1 +- 0.13
10-fold: 99.2 +- 0.05
LIO: 91.0 

All produced by WEKA's ANN (SVM produced extremely similar results)

However, the paper also has results for when only 1 sensor is used for the sample data.

## Goal:

See how close a CNN using resnet34 or resnet 50 does compared to these results, for one sensor (acceleration) and for all sensors.

Why: 

Simply because I'm following the FastAI course to understand how their library makes creating deep learning neural networks easier to apply.
And human movement is cool. There's so much to it that we know, and so much we still are trying to understand.

## Plan of Attack

1. Normalize data as necessary.
2. Create images for each sample, with 1 sensor (accelerometer)
3. Create dataset out of image data
4. Run resnet34 over data, save results
5. Run resnet50 over data, save results
6. Break, compare results, see if any fine tuning helps, but don't sweat it past that.
7. Repeat 2-6, but with all sensor data? 

