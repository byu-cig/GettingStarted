# Basic Probability

Much of the learning we encounter in physics is deterministic in nature (think differential equations), but in an experimental setting, probability always plays a role. In the byu coherent imaging group, this is especially true. Not only is data collection often noisy, quantum mechanical effects also play a role in adding noise to our problems. 

This directory goes over some basic probability and covers the following topics:

- Basic Set Theory and Probability Definitions
- Properties of Probability Density Function and Probability Mass Functions
- Independent and Identicallly Distributed Data
- Multivariate Distributions
- Further Study

## Basic Set Theory and Probability Definitions

It's important to understand that statistical inference is based on the sound mathematical concepts of set theory. When I was first learning statistics, this information was not presented and the methods felt very ad hoc because of that. Unfortunately, this involves a decent amount of set theory that is not overly complex, but can be long. This section attempts to ignore most of this information, but give an intuitive explanation of why set theory is important. 

### Set Theory

Sets are collections of objects with no restriction on what those objects are. In terms of probability theory, a set will have an associated probability with each element of the set. For example, consider rolling a die. There are 6 possible outcomes, so our set, which we'll call $S$ is a six element set. So, we have that

$$S = \\\{1, 2, 3, 4, 5, 6\\\}$$

In our case, we will assume that all possibilities have a probability of 1/6. While it may be obvious, it is important to note that the sum of all possibilities is equal to one.

### Probability Definitions

To move from set theory to probability theory, we have to define what a random variable is. The definition we will give is not exactly accurate, but is close enough for a start. A random variable is a mapping from a set with it's associated probabilities to the real number line. Consider the set $S$ that we just defined. There are several possible mappings that we could consider. 

We could consider one that preserves the set exactly as it is. On a number line, this would look like the following image.



Here, we see that the probabilities are preserved such that one through six each have a probability of occuring equal to 1/6. Alternatively, we may consider the random variable that maps all even number of the set $S$ to zero and all odd numbers to one. In this case, the picture would change to this image.


Now, both zero and one have an equal probability of occuring equal to 1/2. Again, we must note that the sum of all probabilities that the random variable considers adds to one. This is because a random variable always maps eveerything in the set to the real line and does not map the same thing to two separate places.

In practice, we don't work with sets and map them to the reals, we work directly with random variables. These will usually have names such as the Gaussian distribution or the Bernoulli distribution. However, it is important to know that these came from foundational mathematical concepts that have just as much validity as say, calculus.

## Probability Density Functions and Probability Mass Functions

Probability density functions (PDFs) and probability mass functions (PMFs) are functions that represent the mapping random variables define. PDFs are continuous, whereas PMFs are discrete. Intuitively PMFs are simpler to understand. For each point where the PMF is defined, a value is given representing a probability. If all of the values of the PMF are summed, it gives a value of one. On the other hand, the value of a PDF at a certain point is not a probability. Instead, probabilities can be found by integrating the PDF. What this means is that probabilities of PDFs can no longer be defined at a point, but rather over some region. Here, when the PDF is integrated over the reals, the integral equals one.

When working with PDFs and PMFs in our research, the most common ones we will encounter are named distributions. These are distributions that are fairly common and have been used extensively in research before. Because they have been used so much, these distributions are often easy to work with as many of their properties are known.

## Independent and Identically Distributed Data

Often, when working in the field of statistics, the term "independent and identically distributed", or i.i.d, data. Before going to the i.i.d. part of this term, we will start by discussing the term data. Normally, when we think of data collection, we think of them as known quantities, something we have just measured. However, in statistics, it is often the case that data is thought of as having a distribution and having probability of being values. However, in the mind of a statistician, this is possible data that has yet to be collected. In that sense, we can think of the data as being a random variable, rather than data points. It is then possible to use statistical inference on this hypothetical data.

Since the data has a distribution, we can then talk about what that distribution may look like. i.i.d data is a classification that specifies the relatedness of the distributions of different data points. When two random variables are independent, it means that when one variable is known, it gives no information about the other random variable. A good example of this is flipping a coin. One flip of the coin does not affect future flips of the coin. Mathemtically, independence means that the probability of both events occuring is equal to the probability of each one separately occuring multiplied together, or in other words,

$$P(A \cap B) = P(A)P(B)$$

The other half of i.i.d. is identically distributed. This means that the distributions of the data are all equivalent functions.

## Multivariate Distributions

In the context of our research, multivariate distributions arise mainly because we have lot of data, which has an unknown joint distrribution. However, if the data is indpendent, the joint distribution can be found easily. Because independence mathematically means multiplication, the joint distribution of independent data is the PDFs or PMFs of the data multiplied together. The main difference between inference with multivariate distributions versus univariate distributions is the change in demensionality of the operators used. The most applicable are the mean and variance, which are changed to a vector and a matrix, respectively.

## Further Study

This writeup is by no means a proper introduction in probability theory. Rather, it gives an introduction to specific terminology that you will immediately encounter while working on the research projects in the byu coherent imaging group. Additionaly topics that are just as fundamental and are worth looking up are:

- Cumulative Distribution Functions
- Expected Values
- Conditional Distributions
- Probability Transformations
- Bayes Theorem
