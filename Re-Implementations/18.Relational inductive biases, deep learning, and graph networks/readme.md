#  Relational inductive biases, deep learning, and graph networks
- <ins>Author, Venue & Year</ins>: **Peter W. Battaglia, Jessica B. Hamrick, Victor Bapst, Alvaro Sanchez-Gonzalez, Vinicius Zambaldi, Mateusz Malinowski, Andrea Tacchetti, David Raposo, Adam Santoro, Ryan Faulkner, Caglar Gulcehre, Francis Song, Andrew Ballard, Justin Gilmer, George Dahl, Ashish Vaswani, Kelsey Allen, Charles Nash, Victoria Langston, Chris Dyer, Nicolas Heess, Daan Wierstra, Pushmeet Kohli, Matt Botvinick, Oriol Vinyals, Yujia Li, Razvan Pascanu, Arxiv, 2018**

### [Original Paper](https://arxiv.org/abs/1806.01261) 

## Summary

- The authors started with the principle of combinatorial generalization, an ability of human to construct new interferences, predictions, and behaviours from known building blocks. We can also call it the ability to make infinite use of finite means.

- Throughout the paper, the authors argued that graph networks is one direction to go if we aim at achieving combinatorial generalization. A important reason is that graph networks implement the relational inductive bias.

- What is an inductive bias? T. Mitchell defined an inductive bias as set of assumptions that the learner uses to predict outputs given inputs that it has not encountered. In a way, it resembles the modelling procedure in statistical inference, where we make assumptions of the procedure how the sample data are collected.

- In the process of learning, during which we gain knowledge by observing and interacting with the world, we need to search a space of solution for one that either provides a better explanation of the data, or offers higher awards. But what happens if there are multiple solutions that are equally good? An inductive bias allows a learning algorithm to prioritize one solution or one interpretation over another, independent of the observed data.

- Many techniques in statistics and machine learning implement the concept inductive bias either explicitly or implicitly. Probably the best known of them is the Occam’s Razor Principle: when multiple hypotheses make the same predictions, one should prefer the one with the fewest assumptions. Other examples listed by the authors include the choice and parametrization of the prior distribution in Bayesian inference and the techniques of regularization for regression and classification, which shrinks the parameters towards zero in order to avoid over-fitting. It can also be implemented in the architecture of the algorithm itself, for instance by preferring certain hypotheses heuristically.

- From the statistical perspective, inductive biases often trade flexibility for improved sample complexity, which is defined in machine learning as the number of training samples required to learn a target function, and can be understood in terms of the variance-bias trade-off. One form of inductive bias or another may improve the capacity of the conclusion being generalized, though this is not guaranteed until the model has been repeatedly tested and validated.

- The authors observe these models from the perspective of inductive biases. There are some relational inductive biases implemented, for instance the local inductive biases in CNN, however they are not yet strong enough. They believe that graphs, the mathematical model encoding objects and their relationships, in particular computations over graphs, support a strong relational inductive bias.

- From there, they propose to use graph structures explicitly for computation, especially in combination with the three types of neural networks listed above. They name the framework graph networks.

- A graph in the framework of graph networks is a 3-tuple consisting of nodes, edges, and global attributes. Computation in a full graph-network block involves iterative updates of attributes of edges, nodes, and the graph. Details can be found in the Algorithm 1 in the paper.

- The computation model reminds me strongly of physical models of networks as well as rule-based network-analysis methods such as Boolean network analysis. According to the authors, the function used to update the elements of a graph and to aggregate multiple effects as input to an element can be versatile. Even a neural network is possible to be used.

- Next, the authors went on introducing ideas how to implement the iterative update logic inside a graph network block. And they also discussed how to combine blocks of graph networks into a larger architecture of computation, for instance a sequential architecture, an encoder-decoder architecture, or a recurrent graph-network architecture.




