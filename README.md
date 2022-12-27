# GAN-Based-Music-Genre-Transfer
A GAN based music genre transfer for variable length songs.

# Abstract
The Oxford dictionary defines music as sounds that are arranged in a way that
makes listening enjoyable or exciting. Having good taste in music or being able to
play a musical instrument is a skill. Unfortunately, not everyone is endowed with
this skill since not every audio signal can be labeled as a music. In this work, we
are attempting to allow one to generate music of different emotions or genres from
existing music of various durations without being subject to a copyright claim as
it easier for an amateur to create music from an existing music rather than create
a new one. The GAN architecture is one of the most commonly used approaches
for creating novel, synthetic instances of data that can be passed off as real data
at first glance. We have developed an architecture based on GANs that trains on
music of different genres in order to generate music associated with those genres.
While the adversarially modified music has a longer duration than the one liable
for a copyright claim, it cannot be considered theft because it has been modified
into a different genre.

# Methodology

For our final architecture, we used a Deep Convolutional GAN or DCGAN which has a discriminator
and a generator network. We trained our model on multiple epochs for a particular music genre
making our discriminator train to classify whether an audio signal correspond to that particular music
genre or not. Additionally, we kept improving our generator network which is fed random noise as an
input.
Once trained on several epochs or when the error went below a particular threshold , we stopped
training and used the generator network to produce some music based on some input.
Our generator network now knows how to modify a particular music to match it with the genre it was
trained on. We take advantage of this and provide music of any genre of length 30 seconds (more
than copyright claim threshold) and adversarially modify the original music

# Dataset used

Finding the correct dataset was a challenge and after careful considerations, we used a combination of
3 datasets GACMIS (Genre Automated Classification using Machine Learning of Indian Songs)
consisting of 6 genres Indian songs each having 100 songs, Indian Music Genre Dataset (Kaggle)
consisting of 5 genres Indian songs each having 100 songs, FMA (Free Music Archive) consisting
of 8 gneres English songs each having 1000 songs, but since we are training mainly of Indian Hindi
songs, we have used just a small amount of data from FMA dataset.

# How to Run

There are two ways of running this project

1. Use Existing Trained Models with .h5 file
2. Generate from scratch.

## Use Existing Trained Models with .h5 file
Run the test section of .ipynb file with the appropriate genre weights as the path and pass the songpath.
This will generate a spectrogram and output newly genre transfered song.

## Generate from scratch.
To generate everything from scratch, run each cell of .ipynb file which will train on the genre provided and store the weights after each 10 epochs.

# Results

Sample outputs have been provided in the output directory.
AB-5.mp4 is Sufi to bhajan
Ab-6.mp4 is Semi classical to bhajan










