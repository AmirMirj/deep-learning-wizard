!!! info
    This is a list of growing number of papers and implementations I think are interesting.

## Long Tailed Recognition
- [Large-Scale Long-Tailed Recognition in an Open World](https://arxiv.org/abs/1904.05160)
    - Frequently in real world scenario there're new unseen classes or samples within the tail classes
    - This tackles the problem with dynamic embedding to bring associative memory to aid prediction of long-tailed classes
    - The model essentially combines direct image features with embeddings from other classes
    
## Deep Reinforcement Learning
- [An Empirical Analysis of Proximal Policy Optimization with Kronecker-factored Natural Gradients](https://arxiv.org/pdf/1801.05566.pdf)
	- Shows 2 SOTA for deep RL currently (2018 / early 2019): PPO and ACKTR
	- Attempts to combined PPO objective with K-FAC natural gradient optimization: PPOKFAC
	- Does not improve sample complexity, stick with either PPO/ACKTR for now

## Optimization
- [Online Learning Rate Adaptation with Hypergradient Descent](https://arxiv.org/abs/1703.04782)
	- Reduces the need for learning rate scheduling for SGD, SGD and nesterov momentum, and Adam,
	- Uses the concept of hypergradients (gradients w.r.t. learning rate) obtained via reverse-mode automatic differentiation to dynamically update learning rates in real-time alongside weight updates
	- Little additional computation because just needs just one additional copy of original gradients store in memory
	- Severely under-appreciated paper

## Architecture Search
- [DARTS: Differentiable Architecture Search](https://arxiv.org/abs/1806.09055)
    - Neural search algorithm based on gradient descent and continuous relaxation in the architecture space. 
    - A good move towards automatic architecture designs of neural networks.
	
## Network Pruning
- [EigenDamage: Structured Pruning in the Kronecker-Factored Eigenbasis](https://arxiv.org/abs/1905.05934)
    - Compared to existing Hessian-based methods, this works on the KFE
    - Reported 10x reduction in model size and 8x reduction in FLOPs on Wide ResNet32 (WRN32)
    
    
## Bayesian Deep Learning
- [Fast and Scalable Bayesian Deep Learning by Weight-Perturbation in Adam](https://arxiv.org/abs/1806.04854)
    - Variational Adam (Vadam), an alternative to varianal inference via dropout.
    - Vadam perturbs the network's weights when backpropagating, allowing low computation cost uncertainty estimates. 
    - Not as good as dropout in terms of performance, but a good direction for computationally cheaper options.

## Explainability
- [A Unified Approach to Intepreting Model Predictions](https://arxiv.org/pdf/1705.07874.pdf)
    - Introduces SHAP (SHapley Additive exPlanations)
    - "SHAP assigns each feature an importance value for a particular prediction"
        - Higher positive SHAP values (red) = increase the probability of the class
        - Higher negative SHAP values (blue) = decrease the probability of the class

## Cautious
- [Same Stats, Different Graphs: Generating Datasets with Varied Appearance and Identical Statistics through Simulated Annealing](https://www.autodeskresearch.com/publications/samestats)
    - Shows through scatterplots that multiple toy datasets although visually very different can have similar summary statistics like mean, standard deviation and pearson correlation
    - This paper emphasises the need to always visualize your data
    
## Visualization
- [Netron](https://github.com/lutzroeder/netron)
    - Easily visualize your saved deep learning models (PyTorch .pth, TensorFlow .pb, MXNet .model, ONNX, and more)
    - You can even check out each node's documentation quickly in the interface

## Missing Values
- [BRITS](https://arxiv.org/abs/1805.10572)
    - If you face problems in missing data in your time series and you use existing imputation methods, there is an alternative called BRITS where it learns missing values in time series via a bidirectional recurrency dynamical system