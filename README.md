# Self-Optimize-Neural-Network
Self optimized Feed Forward, Recurrent and Convolutional Neural Network using Bayesian Optimization

#### 1. Feed-Forward Neural Network to classify Iris type (done)

#### 2. Recurrent Neural Network to classify text sentiment (in training)

#### 3. Convolutional Neural Network to classify CIFAR 10 (in training)

Bayesian optimization works by constructing a posterior distribution of functions (gaussian process) that best describes the function you want to optimize. As the number of observations grows, the posterior distribution improves, and the algorithm becomes more certain of which regions in parameter space are worth exploring and which are not, as seen in the picture below.

![alt text](https://raw.githubusercontent.com/fmfn/BayesianOptimization/master/examples/bo_example.png)

## Feed-Forward Iris
```text
Initialization
-------------------------------------------------------------------------------------------------------------------------
 Step |   Time |      Value |   activation |      beta |   dropout_rate |   learning_rate |   num_hidden |   size_layer | 
stop after 200 iteration with train cost 9.328038, valid cost 6.830622, train acc 0.477589, valid acc 0.344333
    1 | 00m00s |    0.34433 |       0.1557 |    0.0741 |         0.5189 |          0.6100 |       2.2780 |     109.6324 | 
stop after 200 iteration with train cost nan, valid cost nan, train acc 0.339286, valid acc 0.333333
    2 | 00m06s |    0.33333 |       1.5493 |    0.2110 |         0.9648 |          0.6746 |       8.4695 |     406.6496 | 
stop after 200 iteration with train cost 353764719888.678528, valid cost 323302490112.000000, train acc 0.407589, valid acc 0.338667
    3 | 00m19s |    0.33867 |       1.2247 |    0.0866 |         0.4345 |          0.1704 |      10.1839 |     715.3899 | 
    
.....

Maximum NN accuracy value: 0.731667
Best NN parameters:  {'dropout_rate': 0.98999999999999999, 'beta': 9.9999999999999995e-07, 'learning_rate': 0.0001, 'size_layer': 979.22638102861038, 'activation': 2.0, 'num_hidden': 2.0}
```
