# NeuralTransfer
Neural Style Transfer
Repo contains code used to impart the style of a processed image onto the content of another.

## Intro
 
Image analysis and transformation is a prominent and growing field in
data science and machine learning. Through image transformation, it is
possible to render the content of pictures in different styles. Neural style
transfer allows us to take photographs and merge the information contained
within them with the artistic styles of a separate picture

## Data

The first task is to crop and reformat the images into a square. Cropping
ensures that any unwanted noise on the border of the image is excluded, and
squaring the image creates a more uniform input.
The second task loads and pre-processes images that are read in. It downloads a file from a specified URL if not already in the cache. Then it reads an
image from the file into an array, and converts the image into a float32 array. It
then normalizes the pixel values by dividing by 255. Finally, the pictures are
plotted after they have been loaded and pre-processed.

## Model

VGG19 was used as the pre-built model(<https://keras.io/api/applications/vgg/>). Other image classification convolutional neural networks such as ResnetV2, MobileNet, and DenseNet were also
attempted.
When attempting to merge content and style images through ResnetV2,
MobileNet, and DenseNet, outputted images were either the
unaltered content image, or a slightly distorted version of the content image.
