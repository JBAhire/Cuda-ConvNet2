# CUDA-CONVNET
## I've released an update to cuda-convnet, called cuda-convnet2. The two main new features are faster training on Kepler-generation GPUs and support for multi-GPU training.

This is a fast C++/CUDA implementation of convolutional (or more generally, feed-forward) neural networks. It can model arbitrary layer connectivity and network depth. Any directed acyclic graph of layers will do. Training is done using the back-propagation algorithm.

Fermi-generation GPU (GTX 4xx, GTX 5xx, or Tesla equivalent) required.
Documentation

    Compiling -- how to check out and compile this code.
    Data -- what kind of data this net can train on.
    LayerParams -- how to specify an architecture for the net.
    NeuronTypes -- types of hidden unit nonlinearities.
    TrainingNet -- how to train the net.
    Options -- the command-line arguments that the net takes.
    ViewingNet -- how to look inside the checkpoints saved by the net.
    CheckingGradients -- how to numerically test the gradients for correctness.

## Fast results

    11% error on CIFAR-10 in 75 minutes, with image translations and horizontal reflections (def, params).
    13% error on CIFAR-10 in 25 minutes, with image translations and horizontal reflections (def, params).
        See Methodology for details of training.

            Filters learned by this net:

               

    18% error on CIFAR-10 in 20 minutes, without any image translations/transformations/preprocessing (def, params).
    26% error on CIFAR-10 in 80 seconds, without any image translations/transformations/preprocessing (def, params).
