# BASS_probability

It contains the searched probability of ImageNet training images, from the papar: BASS: Bayesian-based Automatic Sampler Search.

The paper samples crops for ImageNet while the generated 100 epochs of crops are hard to upload. Moreover, we find that only sampling at image level achieves comparable effect.

We upload the searched probability of each image sorted by their index in the original meta file. Users may use the probability to sample images during the training of ImageNet by unzipping the uploaded file and renorming the probability in it to sum 1. The results on ResNet18-110-epoch is 71.3% compared with the uniform sampling baseline 70.3%.

To reproduce the experiment, the learning rate should be warm-uped from 0.2 to 0.8 in the first 2500 iterations and decay x0.1 at 30, 60, 90 epochs. The batch size is 2048 and weight decay is 1e-4. The optimizer is mini-batch SGD with nesterov and momentum 0.9. Only random flip, random crop and color-jitter are used for augmentation.
