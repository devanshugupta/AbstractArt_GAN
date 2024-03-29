# AbstractArtGAN
GANs, or Generative Adversarial Networks, are a type of
neural network architecture that allow neural networks to
generate data. In the past few years, they’ve become one of
the hottest subfields in deep learning, going from generating
fuzzy images of digits to photorealistic images of faces.
I found GANs fascinating, and in an effort to understand
them better, I thought that I’d make this project, and in the
process of explaining the math and code behind them,
understand them better myself.

• Abstract ART creation through Generative Adversarial
Networks.
• Real data taken from wiki-art images cubism, high
renaissance.
• Deep convolutional neural networks (DC-GAN) used to create abstract art.
• Trained on Google Colab for GPUs and TPUs usage.

# Method:
GANs learn a probability distribution of a dataset by putting
two neural networks against each other.
Training generative adversarial networks involve two
objectives:

1. The discriminator maximizes the probability of
assigning the correct label to both training examples
and images generated by the generator. Such that
the policeman becomes better at differentiating
between fakes and real paintings.
2. The generator minimizes the probability that the
discriminator can predict that what it generates is
fake. Such that the generator becomes better at
creating fakes

# Working Of GAN:

1. The GAN plays a minimax game, where the entire
network attempts to optimize the function V(D,G). This
is the equation that defines what a GAN is doing:

2.![Capture](https://user-images.githubusercontent.com/22978896/124722550-c793c180-df27-11eb-9d98-83a8ebec8d58.PNG)


3. Now to anyone who isn’t well versed in the math behind
it, it looks terrifying, but the idea it represents is simple,
yet powerful. It’s just a mathematical representation of
the two objectives as defined above.
4. The generator is defined by G(z), which converts some
noise z we input into some data, like images.
5. The discriminator is defined by D(x), which outputs the
probability that the input x came from the real dataset
or not.
6. We want the predictions on the dataset by the
discriminator to be as close to 1 as possible, and on the
generator to be as close to 0 as possible. To achieve this,
we use the log-likelihood of D(x) and 1-D(z) in the
objective function.
7. The log just makes sure that the closer it is to an
incorrect value, the more it is penalized.
# Results:
The final results are 100th image,as shown, the
paintings have some degree of strokes and color
matching that stimulates some kind of abstract art feeling. I have tried to make clearer shapes and color-matching by optimisation of weights in the GAN and
the best results can be seen below.


![Capture](https://user-images.githubusercontent.com/22978896/124722976-340ec080-df28-11eb-8028-dd191509ea6d.PNG)
