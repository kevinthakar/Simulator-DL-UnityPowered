The project aims at trying to simulate a driverless-car-like behaviour in a known environment, using the open-source simulator available. It trains the model using images, which it gains from its virtual cameras in the manual mode of the simulator. These images teach the software to simulate driverless-like behaviour based on the responses saved in the maual mode.

# How_to_simulate_a_self_driving_car

## Overview

We're going to use Udacity's [self driving car simulator] as a testbed for training an autonomous car. 

## Dependencies

You can install all dependencies by running one of the following commands

You need a [anaconda] or [miniconda] to use the environment setting.

```python
# Use TensorFlow without GPU
conda env create -f environments.yml 

# Use TensorFlow with GPU
conda env create -f environment-gpu.yml
```

Or you can manually install the required libraries (see the contents of the environemnt*.yml files) using pip.


## Usage


### Run the pretrained model

Start up The Udacity Self-Driving Simulator choose a scene and press the Autonomous Mode button.  Then, run the model as follows:

```python
python drive.py model.h5
```

### To train the model

You'll need the data folder which contains the training images.

```python
python model.py
```

This will generate a file `model-<epoch>.h5` whenever the performance in the epoch is better than the previous best.  For example, the first epoch will generate a file called `model-000.h5`.




