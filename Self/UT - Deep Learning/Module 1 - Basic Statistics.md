# Basic Statistics
# Basic Statistics for Deep Learning

## Overview

Deep learning requires understanding basic statistics, including notation and fundamental concepts.

## Basic Notation

### Probability Notation

- **P(X = a)**: Probability that random variable **X** equals specific value **a**
- **Event**: A specific outcome or condition
	- `(X = a)` in **P(X = a)**
- **Random Variable**: A variable whose value is determined by chance
- **Specific Value**: A particular outcome of the random variable

### Probability Density

- **Discrete**: P(Y = α) is well-defined
- **Continuous**: P(Y = α) is not defined (equals 0)
- **Cumulative Probability**: P(α ≤ Y < α + 1/2)
- **Probability Density**: p(Y = α) = lim[ε→0] P(α - ε ≤ Y < α + ε) / (2ε)

### Unified Notation

|Symbol|Description|
|---|---|
|P(x) = P(X = x)|Probability of a discrete event|
|P(x) = p(X = x)|Probability density of a continuous event|

## Properties of P(x)

A function that captures the probabilities of any value x.

### Key Properties

1. **Non-negativity**: 0 ≤ P(x)
2. **Boundedness** (discrete only): 0 ≤ P(x) ≤ 1
3. **Summation (discrete)**: E[1] = Σ P(x) = 1
4. **Integration (continuous)**: E[1] = ∫ P(x)dx = 1

## Probability Distributions

### Definition

P(x) is a **probability distribution** - a function that maps:

- **Discrete**: P: {c₁, c₂, ..., cₙ} → [0, 1]
- **Continuous**: P: ℝ → ℝ

### Three Types of Distributions

1. **Data Generating Distribution**: The true underlying distribution
2. **Empirical Distribution**: Distribution observed from samples
3. **Model Distribution**: Distribution assumed by our model

## Expectation

### Definition

The expected value of function f(x) under distribution P:

$$E_{x \sim P}[f(x)] = \begin{cases} \sum_x P(x)f(x) & \text{discrete P} \\ \int_x P(x)f(x)dx & \text{continuous P} \end{cases}$$

### Short Forms

- E_P[f(x)]
- E[f(x)]
- E_P[f]
- E[f]

### Linearity of Expectation

- E[f(x) + g(x)] = E[f(x)] + E[g(x)]
- E[αf(x)] = αE[f(x)]

## Mean and Variance

### Mean

$$\mu_x = E_{x \sim P}[x]$$

### Variance

$$\sigma_x^2 = \text{Var}_{x \sim P}[x] = E_{x \sim P}[(x - \mu_x)^2]$$

## Important Distinctions

### Discrete vs Continuous Distributions

|Property|Discrete|Continuous|
|---|---|---|
|Variance|Always finite|Can be infinite|
|P(X) values|Always ≤ 1|Can be > 1|

## Sampling

### Notation

- **x ~ P**: x is sampled from distribution P

### Sampling Bias

- **Key Insight**: Samples are always biased
- **Infinite Samples**: Empirical distribution approaches data generating distribution
- **Finite Samples**: Always contain some bias

## Statistical Models

### General Form

$$f_θ: X → Y$$

Where:

- **X**: Input space
- **Y**: Output space
- **θ**: Model parameters

### Regression Model

$$f_θ: ℝⁿ → ℝᵈ$$

### Classification Model

$$f_θ: ℝⁿ → P(X), \text{ where } P(X) ⊂ ℝᵈ$$

### Machine Learning Goal

- **Objective**: Find optimal parameter θ
- **Method**: Learn from data

## Data Types

### Unlabeled Data

$$D = {x_1, x_2, ...} \text{ where } x_i \sim P_D$$

### Labeled Data

$$D = {(x_1, l_1), (x_2, l_2), ...} \text{ where } (x_i, l_i) \sim P_D$$

## Key Takeaways (TL;DR)

1. **Model**: A function f_θ: X → Y that maps data to predictions
2. **Expectation**: Measures the average value of f weighted by probability P
3. **Variance**: Measures deviation from the mean
4. **Sampling**: Always introduces bias, but approaches true distribution with infinite samples
5. **Goal**: Use statistical foundations to learn optimal parameters from data

---

## Related Concepts

- [[Probability Theory]]
- [[Machine Learning Fundamentals]]
- [[Statistical Inference]]
- [[Deep Learning]]

#statistics #probability #machine-learning #deep-learning
