neural-financial-prediction-encog-java
==================

We report on our analysis of the feasibility of using artificial neural networks (ANNs) to perform financial time series prediction. Using subsets of 7 different financial time series, we generate and train 29,718 types of multi-layer perceptron NNs and then evaluate them on test data consisting of S&P 500 end-of-day time series data. Our metric for evaluation was the accuracy to which each NN predicted the direction of the end-of-day price of the S&P 500 on the subsequent day.

Our analysis proceeds in two stages. First, we generate 29,718 different NNs by allowing numerous parameters to vary, including temporal lag, how many days back in time to start the training data, the number of hidden layers, the neuron count within each hidden layer, the training algorithm, and the subset of the 7 different financial time series that we used as inputs. From this analysis, we find that, with the single exception of the back propagation training algorithm, all of the training algorithms have mean accuracies between 48-52% but have max accuracies clustered between 60-70%. The various Resilient Propagation (RPROP) and Quick Propagation (QPROP) training algorithms have the highest max returns. In the phase of the analysis, we reduce our NN parameter space to only consider the RPROP and QPROP training algorithms, and we focus on extracting finer granularity results with respect to the parameters. We find that mean accuracies increase roughly linearly with the increase in temporal lag of the training data. Additionally, we find that increasing the number of neurons in the first and second hidden layer produces increased mean accuracy, but adding neurons in a third or fourth hidden layer do not significantly affect results. Finally, we utilize these results to train and test 1000 optimized NNs and compare their mean accuracies with those from 1000 baseline NNs. We find that the optimized results produce a mean directional accuracy that is 5.6% greater than the baseline case.
