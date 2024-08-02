This project aims at reproducing the framework proposed in ["Task-Driven Dictionary Learning"](https://arxiv.org/pdf/1009.5358) as a baseline for further exploration in a goal-oriented communication fashion. The core of the framework is to design a dictionary learning algorithm in a supervised perspective. In particular, we consider the sparse mixing vectors $\alpha^*(x,D) = \mathrm{argmin} ||x - D\alpha||_2^2 + \lambda_1 ||\alpha||_1 + \lambda_2 ||\alpha||_2^2$ representing a signal $x \in \mathcal{X}$ with respect to a dictionary $D$ together with a label $y \in \mathcal{Y}$ associated to the signal $x$. 

The joint learning problem arises as a risk minimization formulated as 

$$
\underset{D \in \mathcal{D}, W \in \mathcal{W}}{\mathrm{min}} \mathbb{E}_{y,x}[\mathcal{l}_s(y, W, \alpha^*(x,D))] + \frac{\nu}{2}||W||_F^2
$$

where we want to learn at one time the dictionary $D$ and the parametrization $W$ of the model carrying the supervised task. 

