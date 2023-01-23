# Building RESNET With Residual Networks
The main benefit of a very deep network is that it can represent very complex functions. It can also learn features at many different levels of abstraction, from edges (at the shallower layers, closer to the input) to very complex features (at the deeper layers, closer to the output).

However, using a deeper network doesn't always help. A huge barrier to training them is vanishing gradients: very deep networks often have a gradient signal that goes to zero quickly, thus making gradient descent prohibitively slow.

Residual network solves this problem.

In ResNets, a "shortcut" or a "skip connection" allows the model to skip layers:  

![skip connection]("images/skip_connection_kiank.png")

The image on the left shows the "main path" through the network. The image on the right adds a shortcut to the main path. By stacking these ResNet blocks on top of each other, you can form a very deep network. 

There are two main types of blocks are used in a ResNet, depending mainly on whether the input/output dimensions are the same or different: "identity block" and the "convolutional block."
