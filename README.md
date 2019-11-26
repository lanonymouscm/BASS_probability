# BASS_probability

It contains the searched probability of ImageNet training images, from the papar: BASS: Bayesian-based Automatic Sampler Search.

The paper samples crops for ImageNet while the generated 100 epochs of crops are hard to upload. Moreover, we find that only sampling at image level achieves comparable effect.

We upload the searched probability of each image sorted by their index in the original meta file. Users may use the probability to sample images during the training of ImageNet by unzipping the uploaded file and renorming the probability in it to sum 1. The results on ResNet18-100-epoch is 71.2% compared with the uniform sampling baseline 70.2%.
