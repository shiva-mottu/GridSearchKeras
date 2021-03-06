# GridSearchKeras
Implemented GridSearch Using Keras

This section lists some handy tips to consider when tuning hyperparameters of your neural network.

1) k-fold Cross Validation. You can see that the results from the examples in this post show some variance. A default cross-validation of 3 was used, but perhaps k=5 or k=10 would be more stable. Carefully choose your cross validation configuration to ensure your results are stable.

2) Review the Whole Grid. Do not just focus on the best result, review the whole grid of results and look for trends to support configuration decisions.

3) Parallelize. Use all your cores if you can, neural networks are slow to train and we often want to try a lot of different parameters. Consider spinning up a lot of AWS instances.

4) Use a Sample of Your Dataset. Because networks are slow to train, try training them on a smaller sample of your training dataset, just to get an idea of general directions of parameters rather than optimal configurations.

5) Start with Coarse Grids. Start with coarse-grained grids and zoom into finer grained grids once you can narrow the scope.

6) Do not Transfer Results. Results are generally problem specific. * Try to avoid favorite configurations on each new problem that you see. It is unlikely that optimal results you discover on one problem will transfer to your next project. Instead look for broader trends like number of layers or relationships between parameters.

7) Reproducibility is a Problem. Although we set the seed for the random number generator in NumPy, the results are not 100% reproducible. There is more to reproducibility when grid searching wrapped Keras models than is presented in this post.
