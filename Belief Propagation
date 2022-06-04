This lab is a tutorial on belief propagation, one of the many approaches for solving graphical models. The actual goal is to build a model for identifying faults with coffee machines. You're given a graphical model of how a coffee machine works, that connects observations to possible failure modes. Belief propagation is then used to calculate the probability of each failure (marginal probability) given the available evidence (observations). This is broken up as:

Given the graphical model for the state of a coffee machine learn the distributions from data. This is basic (Bayesian) statistics.
Implement belief propagation, so you can evaluate the probability of each failure given the available evidence. This is broken down into a number of steps:
Conversion from Bayes net to factor graph, as BP is simplest to implement using the later. A factor graph is described in the slides, but is a bipartite graph of factors and random variables.
Belief propagation works by passing messages along the edges of a factor graph. Each message depends on other messages having already been sent, so the second step is to work out a valid order to send messages in.
Now you need to pass the messages, by implementing two functions: One to pass a message from a RV (random variable) to a factors, and another to pass a message from a factor to a RV.
Finally, the above two steps let you pass all of the messages and extract the final belief. There is an extra complication to handle observed random variables. This has been coded for you.
