# Fake-Human-Face-using-GAN
objective: To generate fake faces of human¶
Generative adversarial networks (GANs) are algorithmic architectures that use two neural networks, pitting one against the other (thus the “adversarial”) in order to generate new, synthetic instances of data that can pass for real data. They are used widely in image generation, video generation and voice generation.

GANs are made up of two components -

Generator - generates new data instances
Discriminator - tries to distinguish the generated or fake data from the real dataset.

Discriminative algorithms try to classify input data; that is, given the features of an instance of data, they predict a label or category to which that data belongs. So discriminative algorithms map features to labels. They are concerned solely with that correlation.

One the other way, loosely speaking, generative algorithms do the opposite. Instead of predicting a label given certain features, they attempt to predict features given a certain label.

While training they both start together from scratch and the generator learn to shape the random distribution through the training epochs.
![image](https://github.com/user-attachments/assets/2f47b3f1-37f8-4821-9902-f7ae767f93da)



Working of GAN
In the paper that introduced GANs, the generator tries to minimize the following function while the discriminator tries to maximize it:

![image](https://github.com/user-attachments/assets/53044682-9412-4715-b732-d1c2bde1753a)


In this function:

D(x) is the discriminator's estimate of the probability that real data instance x is real.

Ex is the expected value over all real data instances.

G(z) is the generator's output when given noise z.

D(G(z)) is the discriminator's estimate of the probability that a fake instance is real.

Ez is the expected value over all random inputs to the generator (in effect, the expected value over all generated fake instances G(z)).

The generator can't directly affect the log(D(x)) term in the function, so, for the generator, minimizing the loss is equivalent to minimizing log(1 - D(G(z))).
