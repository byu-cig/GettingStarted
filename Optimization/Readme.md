# Optimization

In our research, optimization is the underlying method of solving the problems we encounter. Our problems will have a set of unknowns that we want to solve for. We will then formulate the problem so that the solution lies at the minimum or maximum of some function, called an objective function. Optimization problems are usually set up in this way and attempt to find the values of unknowns that achieve the maximum or minima of the defined function.

We will cover some topics that are important to consider when solving optimization problems. These are:

- Discrete vs Continuous Optimization
- Convex vs Non-Convex Optimization
- Loca vs Global Optimization

## Discrete vs Continuous Optimization

As mentioned, optimization problems usually are set up so that whatever algorithm is used is looking for either a maximum or minimum of a function by changing some unknown parameters of that function. However, these parameters may have some restrictions, or constraints, that they must follow. In the case where parameters must be on discrete points, many complications can arise. 

To me, this is fairly counterintuitive. A constraint reestricts the space, so in my mind, we are limiting the search space that we must search over. However, as soon as we move from a continuous to discrete domain, the ability to use calculus disappears, and the problem becomes combinatoric. While it is true that this often means that the search spaace is finite, the size of the search space grows exponentially with additional dimensions, making problems impossible to solve through brute force methods. Additionally, search methods are usually implemented in an ad hoc way because there is no clear way to solve these problems.

The point of this section is to tell you that, while continuous optimization problems are hard to solve, be grateful that they are not discrete. However, if you have a discrete problem, the best advice I can give is to devise a method that guarantees that as you search, your objective function will always decrease. This way you can be sure that you will always improve your answer. After this, care must be taken to improve the convergence of the solution while maintaning strong bounds on your original search method.

## Convex vs Non-Convex Optimization
