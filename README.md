# kadenze-deep-creative-apps
My own assignments to Kandenze creative applications of deep learning in TensorFlow

**Disclaimer:** be aware of the Kadenze code of conduct if you are enrolled in the course. Copying the code from this repository and pretending it to be yours would be bad (evil). Even looking into it may be an infringement. Plagiarism is not tolerated. You are now informed, behave with honor.

## Overview

The Kadenze course "creative applications of deep learning in TensorFlow" is a great MOOC to learn the TensorFlow framework and manipulate fascinating neural network architectures, like variational autoencoders (VAE) or recurrent neural network (RNN) with LSTM cells. For me it has been a great opportunity to develop my burgeoning creative skills.

You will experience latent space exploration (if you don't know what a latent space is, read [this good introduction][fastforward-vae]). The following manifold has been generated during the course with the dataset of my choice:

![Galaxy Zoo manifold][galaxy-manifold]

The Galaxy Zoo dataset is not expressive enough, so the visual and artistic impact is not as good as expected. Nevertheless, you can perfectly observe relevant variations of galaxy shape, sharpness, orientation, existence of stars in the field, etc.

For the project, I came to play around with generative hand writing (see below for full credits on inspiration and external code use). After a training on human hand writing, the code is able to generate a kind of [ansemic writing][wikipedia-asemic]:

![Generative hand writing][glyphs-rnn]

## Installation and setup

You can find the installation instruction on the [CADL repository][cadl-install]. I have a slightly different setup since I use Anaconda.

On OS X, download the Anaconda [installation script][continuum-download] for Python 3.5 and follow the Continuum instructions. Then, install TensorFlow:

````
$ conda create -n tensorflow python=3.5
$ source activate tensorflow
(tensorflow)$ conda install ipykernel
(tensorflow)$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-0.11.0rc1-py3-none-any.whl
(tensorflow)$ pip install --upgrade --ignore-installed $TF_BINARY_URL
````

There are for sure many more dependencies, I'm used to install them one by one when required. That's also a good reason for using a Conda environment.

## Contribution

As this repository stored my own work and since the course is over for me, there is no need to update it. I will also most likely not accept any contribution.

## Credits and license

+ the main credits go to [Parag Mital][pkmital] and [Kadenze][kadenze], all materials are distributed under the Apache license v2.0 and the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license
+ the assignments come from the [CADL GitHub repository][github-cadl], you can find in this repository amazing code, like a ready-to-use VAE/GAN net (strong computing power will be required to train it by yourself)
+ the course heavily relies on the [CelebFaces Attributes Dataset][mmlab-celeba]
+ the picture of the [galaxy NGC 4536][wikimedia-n4536] used in the session 2 and 4 is credited to Adam Block/Mount Lemmon SkyCenter/University of Arizona and is distributed under the Creative Commons Attribution-ShareAlike 3.0 United States license, the picture has been transformed by the creative processes of the course
+ I have used the [Galaxy Zoo data][kaggle-galaxy-zoo] published on the Kaggle challenge web page for the first assignments (see further references to the Galaxy Zoo behind the link)
+ the code of the project is totally based on the project [write-rnn-tensorflow][github-write-rnn] by the great [Hardmaru][twitter-hardmaru], the net is trained on the [IAM On-Line Handwriting Database][iam-handwriting-database], freely available for non-commercial use once registered
+ the project has been inspired by the artwork [sand-glyphs][github-sand-glyphs], by the way, I highly recommend to have a look at the other creations of [Anders Hoff][twitter-incovergent] (alias Inconvergent) and you will for sure spend a good time reading his [blog][inconvergent]
+ the picture of the [Pleiades][wikimedia-pleiades] is in the public domain and authored by NASA, ESA, AURA/Caltech, Palomar Observatory

[fastforward-vae]: http://blog.fastforwardlabs.com/post/148842796218/introducing-variational-autoencoders-in-prose-and
[wikipedia-asemic]: https://en.wikipedia.org/wiki/Asemic_writing

[cadl-install]: https://github.com/pkmital/CADL#what-is-notebook
[continuum-download]: https://www.continuum.io/downloads#_macosx
[pkmital]: https://github.com/pkmital
[kadenze]: https://www.kadenze.com/

[github-cadl]: https://github.com/pkmital/CADL
[mmlab-celeba]: http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html
[wikimedia-n4536]: https://commons.wikimedia.org/wiki/File:N4536s-crop.jpg
[kaggle-galaxy-zoo]: https://www.kaggle.com/c/galaxy-zoo-the-galaxy-challenge/data
[github-write-rnn]: https://github.com/hardmaru/write-rnn-tensorflow
[twitter-hardmaru]: https://twitter.com/hardmaru
[iam-handwriting-database]: http://www.fki.inf.unibe.ch/databases/iam-on-line-handwriting-database
[github-sand-glyphs]: https://github.com/inconvergent/sand-glyphs
[twitter-incovergent]: https://twitter.com/inconvergent
[inconvergent]: http://inconvergent.net/
[wikimedia-pleiades]: https://en.wikipedia.org/wiki/File:Pleiades_large.jpg

[galaxy-manifold]: /assets/img/manifold-galaxy.png "Galaxy Zoo manifold"
[glyphs-rnn]: /assets/img/glyphs-rnn.png "Generative hand writing"
