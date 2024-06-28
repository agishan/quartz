# Probability Distributions Cheat Sheet

## 1. Binomial Distribution

**Formula:**
$$ P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k} $$

**Explanation:**
The Binomial distribution models the number of successes in a fixed number of independent Bernoulli trials (yes/no outcomes) with the same probability of success. It is used in scenarios where you have a fixed number of trials and are interested in the number of times a particular event occurs.

**Example:**
A fair coin is flipped 10 times. What is the probability of getting exactly 6 heads?

$$ P(X = 6) = \binom{10}{6} (0.5)^6 (0.5)^{10 - 6} $$

---

## 2. Geometric Distribution

**Formula:**
$$ P(X = k) = (1 - p)^{k - 1} p $$

**Explanation:**
The Geometric distribution models the number of trials needed to get the first success in a series of independent Bernoulli trials with the same probability of success. It is used when you are interested in the number of attempts required to achieve a first success.

**Example:**
What is the probability that the first success in a series of Bernoulli trials occurs on the 4th trial, if the probability of success on each trial is 0.3?

$$ P(X = 4) = (0.7)^{4 - 1} (0.3) $$

---

## 3. Negative Binomial Distribution

**Formula:**
$$ P(X = k) = \binom{k - 1}{r - 1} p^r (1 - p)^{k - r} $$

**Explanation:**
The Negative Binomial distribution models the number of trials needed to achieve a fixed number of successes in a series of independent Bernoulli trials with the same probability of success. It is used when you are interested in the number of trials required to achieve a specified number of successes.

**Example:**
What is the probability of having 5 failures before achieving 3 successes in a series of Bernoulli trials with a success probability of 0.4?

$$ P(X = 8) = \binom{8 - 1}{3 - 1} (0.4)^3 (0.6)^{8 - 3} $$

---

## 4. Exponential Distribution

**Formula:**
$$ f(x; \lambda) = \lambda e^{-\lambda x} $$

**Explanation:**
The Exponential distribution models the time between events in a Poisson process, where events occur continuously and independently at a constant average rate. It is used in scenarios such as the time between arrivals of customers or the lifespan of products.

**Example:**
If the average time between arrivals of customers at a service center is 5 minutes, what is the probability that the next customer arrives in less than 3 minutes?

$$ f(x < 3; \lambda = \frac{1}{5}) = 1 - e^{-\frac{1}{5} \cdot 3} $$

---

## 5. Poisson Distribution

**Formula:**
$$ P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!} $$

**Explanation:**
The Poisson distribution models the number of events occurring in a fixed interval of time or space, where events occur with a known constant mean rate and independently of the time since the last event. It is used in scenarios such as the number of calls received at a call center or the number of arrivals at a service point.

**Example:**
A call center receives an average of 4 calls per minute. What is the probability that exactly 5 calls will be received in a given minute?

$$ P(X = 5) = \frac{4^5 e^{-4}}{5!} $$

---

## 6. Hypergeometric Distribution

**Formula:**
$$ P(X = k) = \frac{\binom{K}{k} \binom{N - K}{n - k}}{\binom{N}{n}} $$

**Explanation:**
The Hypergeometric distribution models the number of successes in a sequence of \( n \) draws from a finite population without replacement, where the population contains exactly \( K \) successes. It is used in scenarios where sampling without replacement is involved, such as quality control or card games.

**Example:**
In a deck of 52 cards, what is the probability of drawing exactly 3 aces in 5 draws without replacement?

$$ P(X = 3) = \frac{\binom{4}{3} \binom{48}{2}}{\binom{52}{5}} $$
