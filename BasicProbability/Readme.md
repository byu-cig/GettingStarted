# Basic Probability

Much of the learning we encounter in physics is deterministic in nature (think differential equations), but in an experimental setting, probability always plays a role. In the byu coherent imaging group, this is especially true. Not only is data collection often noisy, quantum mechanical effects also play a role in adding noise to our problems. 

This directory goes over some basic probability and covers the following topics:

- Basic Set Theory and Probability Definitions
- Properties of Probability Density Function and Probability Mass Functions
- Independence and Identical Distributions
- Expected Values
- Multivariate Distributions
- Further Study

## Basic Set Theory and Probability Definitions

It's important to understand that statistical inference is based on the sound mathematical concepts of set theory. When I was first learning statistics, this information was not presented and the methods felt very ad hoc because of that. Unfortunately, this involves a decent amount of set theory that is not overly complex, but can be long. This section attempts to ignore most of this information, but give an intuitive explanation of why set theory is important. 

### Set Theory

Sets are collections of objects with no restriction on what those objects are. In terms of probability theory, a set will have an associated probability with each element of the set. For example, consider rolling a die. There are 6 possible outcomes, so our set, which we'll call $S$ is a six element set. So, we have that

$$S = {1, 2, 3, 4, 5, 6}$$

In our case, we will assume that all possibilities have a probability of 1/6. While it may be obvious, it is important to note that the sum of all possibilities is equal to one.

### Probability Definitions

To move from set theory to probability theory, we have to define what a random variable is. The definition we will give is not exactly accurate, but is close enough for a start. A random variable is a mapping from a set with it's associated probabilities to the real number line. Consider the set $S$ that we just defined. There are several possible mappings that we could consider. 

We could consider one that preserves the set exactly as it is. On a number line, this would look like the following image.



Here, we see that the probabilities are preserved such that one through six each have a probability of 1/6. Alternatively, we may consider the random variable that maps all even number of the set $S$ to zero and all odd numbers to one. In this case, the picture would change to this image.


Now, both zero and one have an equal probability of 1/2. Again, we must note that the sum of all probabilities that the random variable considers adds to one. This is because a random variable always maps eveerything in the set to the real line and does not map the same thing to two separate places.

In practice, we don't work with sets and map them to the reals, we work directly with random variables. These will usually have names such as the Gaussian distribution or the Bernoulli distribution. However, it is important to know that these came from foundational mathematical concepts that have just as much validity as say, calculus.

## Probability Density Functions and Probability Mass Functions

Probability density functions (PDFs) and probability mass functions (PMFs) are functions that represent the mapping random variables define. PDFs are continuous, whereas PMFs are discrete. Intuitively PMFs are simpler to understand. For each point where the PMF is defined, a value is given representing a probability. If all of the values of the PMF are summed, it gives a value of one. On the other hand, the value of a PDF at a certain point is not a probability. Instead, probabilities can be found by integrating the PDF. What this means is that probabilities of PDFs can no longer be defined at a point, but rather over some region.
