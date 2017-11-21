# interactive-intro-rl

## An Interactive Introduction to Reinforcement Learning

In this repository, we store the code presented for the first of Big Data's open seminar series, *An Interactive Introduction to Reinforcement Learning*, presented at 2017-11-21. In this talk, we introduce various algorithms for solving the exploration/exploitation trade-off in reinforcement learning. We present two scenarios: the Multi-Armed Bandit (Bernoulli) setting, and the Contextual Bandit setting. The algorithms and concepts are presented with mathematical concepts, code, and interactive animations conveyed using Jupyter Notebooks.

### What you'll learn

#### The Multi-Armed Bandit problem

We will present the Multi-Armed Bandit problem, the simplest setting of reinforcement learning, which is perfect for ilustrating the exploration/exploitation trade-off. Suppose that you face a row of slot machines (bandits) on a casino. Each one of the $K$ machines has a fixed probability $\theta_k$ of providing a binary reward to you. You have to decide which machines to play, how many times to play each machine and in which order to play them, in order to maximize your cumulative reward. 

If after a few plays you bet everything on the best machine so far, you risk getting stuck with a suboptimal strategy, as you lack sufficient information to discard the others. If you explore too much, you risk wasting many of your plays gathering information instead of making profits. 

We will show many algorithms to address this dilemma, highlighting a very promising heuristic, which despite being very old (1933) was rediscovered recently showing state-of-the-art results: **Thompson Sampling**. To illustrate the algorithms, we show interactive animations like [this one](), to show the algorithm choices over time along with the posterior distributions for the bandit probabilities $\theta_k$.


#### The Contextual Bandit problem

We also present the Contextual Bandit problem, which is almost the same as the Multi-Armed Bandit problem, but the bandit probabillities $\theta_k$ are actually a function of some exogenous variables:

$$\theta_k(x) = f(x)$$

To solve this problem, we implement two algorithms: (a) an $\epsilon$-greedy strategy using a regular logistic regression for modeling $\theta_k(x)$ and (b) Thompson Sampling with the Online Logistic Regression by Chapelle & Li on their 2011 paper "An Empirical Evaluation of Thompson Sampling". The Online Logistic Regression allows for uncertainty in its coefficients, such that we can have not only a point estimate for $\theta_k(x)$, but a distribution. The fitting process of the algorithm is studied with [this animation](). We also show animations like the ones shown in the first section.


### Required libraries

We use Python 3.6.2. Most of the requirements are satistified by installing the Anaconda Python distribution. The following libraries are required:

* **Jupyter Notebook** (to make use of IPython functions)
* **numpy** and **scipy** for calculations, distibutons and optimization
* **matplotlib** and **seaborn** for visualizations
* **pandas** to manipulate data
* **sklearn** to run Logistic Regression
* **tqdm** to time simulation executions

### Running the Notebooks

The Notebooks are self-contained. We encorage you to clone the repository and run the Notebooks, changing parameters as you like. Any feedback is deeply appreciated.

