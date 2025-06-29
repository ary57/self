# The Big Picture: Model Fitting
In machine learning, we're trying to build models that can make accurate predictions. To do this, we need to find the best parameter θ for our model. 

Machine learning has three components: 
* A **dataset** to learn from
* A **model** with parameters to tune
* A **loss function** to determine how well we're doing. 

The loss function tells us whether we're getting closer to or further from our destination. 

# Understanding Datasets
A dataset $D$ consists of $N$ samples, where each sample is a pair $(x_i, y_i)$: 
- **$x_i$** represents the input features. 
- $y_i$ represents the labels we want our model to learn to predict. 

Mathematically: $D = {(x_i, y_i)}^{N_i=1}$ 

# Loss Functions
A **loss function** $l(θ|x_i, y_i)$ measures how wrong our model is for a single example. It takes: 
- The model parameters θ
- An input $x_i$
- True label $y_i$
And returns a number representing the penalty for our prediction. 

## Expected Loss
**Expected loss** averages the loss over all possible examples: 
$$L(θ) = L(θ|D) = E_{x,y}~D[l(θ|x,y)]$$
Generally, lower loss is considered better performance and high loss is considered bad performance. 

Our learning algorithm finds parameters $θ$ that minimize this expected loss. 

# Specific Loss Functions for Different Problems

##  1. Linear Regression with L2 Loss

**Use case:** Predicting continuous values (house prices, temperatures, etc.)

**Model:** $ŷ = Wx + b$

**Loss function:** $l\left(\theta\left|x,y\right|\right)=\frac{1}{2}\left||y-y\right||_{2}^{2}$

The loss function above penalizes prediction that are far from the true value. The squaring of the function means the large errors are penalized more heavily than small errors. 
## 2. Binary Classification

**Use case:** Yes/no decisions, binary choices.

**Model:** $ŷ =\sigma(Wx+b)$

**Loss function:** $l(\theta|x,y)=-y\log(ŷ)-(1-y)\log(1-ŷ)$

The sigmoid function ensures the output is between 0 and 1, representing probabilities. This is called the **binary cross-entropy loss**.

## 3. Multi-class Classification

**Use case:** Choosing between multiple categories. 

**Model:** $ŷ = \text{softmax}(Wx + b)$

**Loss function:** $l\left(\theta\left|x,y\right|\right)=-y\log\left(ŷ\right)-\left(1-y\right)\log\left(1-ŷ\right)$

The softmax function ensures that the outputs form a valid probability distribution over all classes. It's called **cross-entropy loss**

# The Path Forward: Optimization

Once we know what loss function to use, machine learning becomes an optimization problem:
$$\theta = \text{argmin}{_\theta}L(\theta|D)$$
## Gradient Descent

Deep learning uses gradient descent: 
1. Compute the gradient $∇\theta L(\theta|D)$ in the direction of steepest increase. 
2. Step in the opposite direction to reduce loss. 
3. Use optimizers to update parameters. 
# Key Takeaways

The loss function can be seen as a "compass" in the machine learning landscape. 
It transforms the abstract goal of "learning" into a mathematical optimization problem. 
