This repository aims at reproducing the framework proposed in ["Task-Driven Dictionary Learning"](https://arxiv.org/pdf/1009.5358) as a baseline for further exploration in a goal-oriented communication fashion. The core of the framework is to design a dictionary learning algorithm in a supervised perspective. In particular, we consider the sparse mixing vectors 

$$
\alpha^*(x,D) = \underset{\alpha}{\mathrm{argmin}} ||x - D\alpha||_2^2 + \lambda ||\alpha||_1
$$ 

representing a signal $x \in \mathcal{X}$ with respect to a dictionary $D$ together with a label $y \in \mathcal{Y}$ associated to the signal $x$. 

The joint learning problem arises as a risk minimization formulated as 

$$
\underset{D \in \mathcal{D}, W \in \mathcal{W}}{\mathrm{min}} \mathbb{E}_{y,x}[\mathcal{l}_s(y, W, \alpha^*(x,D))]
$$

where we want to learn at one time the dictionary $D$ and the parametrization $W$ of the model carrying the supervised task, i.e. in predicting $y$ through the sparse vector $\alpha^*(x,D)$ encoding for $x$. The expectation works as a theoretical approach that is tackled via stochastic optimization of empirical risk. 

