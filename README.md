# Q1: 
The **Geometric distribution**  defined by the probability mass function best models the except number of tries required for a successfully grabbing:

$$ P(X = k) = (1 - p)^{k-1} p $$

Where:
- $X$ is the number of tries until success.
- $k$ is the number of trials.
- $p$ is the probability of success on any given trial.

#### Estimate $p$ from the Data
- If we observe the number of trials $k$ to get a success, the average number of trials over many observations will give us an estimate of the expected number of trials, $E[X]$, which for a Geometric distribution is given by:

$$ E[X] = \frac{1}{p}$$

Therefore, we can estimate $p$ as:

$$
p = \frac{1}{\text{average number of trials}}
$$

#### Fit the Geometric Distribution
Once the data (say, $X_1, X_2, ..., X_n$) get collected, we can compute the sample mean $\hat{E}[X]$, and then estimate $p$:

$$
\hat{E}[X] = \frac{1}{n} \sum_{i=1}^{n} X_i
$$
$$
\hat{p} = \frac{1}{\hat{E}[X]}
$$

### Other things to be notified:
For this kind of machine, there is a low probability/frequency that the machanical claw will close with enough force, which means that even if a player has moved the claw to a right position, there is a high probabilty that the claw will "slcak off" which lead to a failure. Besides, players' sense of space varies from person to person. So even if the geometric distribution may best models the number of trial, I seriously doubt whether this event can be represented by a simple geometric distribution.



# Q2:
#### Set Hypothesis

**Null Hypothesis ($H_0$):** The observed distribution matches the Cleveland plant's distribution or Hackettstown plant's distribution.

**Alternative Hypothesis ($H_a$):** The observed distribution does not match either distribution.

#### Observed Counts
Then count the number of candies of each color (Red, Orange, Yellow, Green, Blue, Brown) across several packets of M&Ms. Let these observed counts be $O_{\text{red}}, O_{\text{orange}}, \dots, O_{\text{brown}}$.

#### Expected Counts
Use the proportions for each plant to calculate the **expected counts** for the Cleveland and Hackettstown distributions:

$$
E_{\text{color, Cleveland}} = \text{Total candies observed} \times \text{Cleveland proportion for that color}
$$

$$
E_{\text{color, Hackettstown}} = \text{Total candies observed} \times \text{Hackettstown proportion for that color}
$$

#### Perform a Chi-Square Test
For each plant's distribution, compute the **Chi-Square statistic**:

$$
\chi^2 = \sum_{\text{color}} \frac{(O_{\text{color}} - E_{\text{color}})^2}{E_{\text{color}}}
$$

Where:
- $O_{\text{color}}$ is the observed count for each color.
- $E_{\text{color}}$ is the expected count for each color based on the plant's distribution.

Repeat this calculation for both Cleveland and Hackettstown distributions.

#### Compare $\chi^2$ Values
Compare the calculated $\chi^2$ statistic to the **critical value** from the Chi-Square table (or compute a p-value using statistical software). The critical value depends on:
- Degrees of freedom ($df = \text{number of colors} - 1 = 5$).
- Desired significance level (e.g., $\alpha = 0.05 $).

The plant with the smaller $\chi^2$ value is more likely to be the source of the packets.

---

### Bonus: Flaws in the Article's Methodology
The author used the sample proportions to construct simultaneous confidence intervals. Then he made a judgement by finding certain color was not in the confidence interval instead of judging from the overall closeness of observed distribution to the expected distribution."# Solutions-To-Undergraduate-and-Master-Research-Opportunities" 
