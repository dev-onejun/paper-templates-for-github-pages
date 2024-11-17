---
two-columns: true
author: '
$$
\begin{array}{c}
\huge{\text{Homework #6}} \\
\hline
\mathbf{\text{Wonjun Park}} \\
\text{Computer Science} \\
\text{University of Texas at Arlington} \\
\text{Arlington, TX, USA} \\
\href{mailto:wxp7177@mavs.uta.edu}{\text{wxp7177@mavs.uta.edu}} \\
\end{array}
$$
'
etc: '
$\cdot$ Note that the problems are not intended to be realistic models for the corresponding situations but rather dramatically simplified scenarios. <br/>
$\cdot$ This is individual work, and not a group project; do not share solutions. All work turned in must be your own work. <br/>
$\cdot$ For the questions below, please include all the calculations.
'
---

**1. We are interested to study a sensor system and we know that the sensor noise is distributed normally and has a mean of 5 and a standard deviation of 0.25 . There is a new sensor which we want to see how it works so  we take 10 measurements and the results are: {4.5, 5.2, 5.3, 4.6, 4.9, 5.5, 4.2, 5.1, 4.1, 4.5}. Can you show that the sensors generate different data?**

**Include your calculations and the significance scores. (15 points)**

$\quad$ According to the problem, $M_0 = 5, \sigma = 0.25, n = 10$ and the sample mean is calculated as

$$
\begin{array}{l}
\bar{X} = \frac{4.5 + 5.2 + 5.3 + 4.6 + 4.9 + 5.5 + 4.2 + 5.1 + 4.1 + 4.5}{10} = \frac{47.9}{10} = 4.79
\end{array}
$$

$\quad$ Although the number of samples is less than 30, following the instruction in the course material, z-test is adopted to test the hypothesis since the population follows a normal distribution. Using z-test,

$$
\begin{align*}
i) & \quad \begin{array}{ccc} H_0: & M = 5 \\ H_1: & M \neq 5 & \text{(two-tailed Z-test)} \end{array} \\
ii) & \quad \alpha = 0.05 \to Z_{\frac{\alpha}{2}} = 1.96 \\
iii) & \quad Z = \frac{4.79 - 5}{\frac{0.25}{\sqrt{10}}} = \frac{-0.21}{0.079} \simeq -2.6563 (\lt -1.96) \\
iv) & \quad \text{Therefore, reject the null hypothesis } H_0
\end{align*}
$$

$\quad$ As a result, the sensors generate different data.

**2. In order to evaluate the runtime performance of an algorithm, we measured it's run time performance on 15 samples and the results are: {17.5, 16.3, 18.4, 14.9, 16, 16.5, 18.5, 15.9, 18, 18.5, 18.1, 15.3, 17.6, 17.7, 17.8}. The population has an average runtime performance of 16.5. Is there any difference between the first algorithms and the population?**

**Evaluate the significance of the hypothesis, explain and list your calculations, test choices, and conclusion drawn. (15 points)**

$\quad$ With the given $M_0 = 16.5, n = 15$, the sample mean and the sample standard deviation are calculated as

$$
\begin{array}{ll}
\bar{X} & = \frac{17.5 + 16.3 + 18.4 + 14.9 + 16 + 16.5 + 18.5 + 15.9 + 18 + 18.5 + 18.1 + 15.3 + 17.6 + 17.7 + 17.8}{15} \\
& = \frac{257}{15} \simeq 17.13 \\
S & = \sqrt{\frac{\sum_{i=1}^{n}(X_i - \bar{X})^2}{n-1}} = \sqrt{\frac{20.3935}{14}} \simeq 1.2069
\end{array}
$$$\quad$ For the number of samples less than 30, using t-test,

$$
\begin{align*}
i) & \quad \begin{array}{ccc} H_0: & M = 16.5 \\ H_1: & M \neq 16.5 & \text{(two-tailed (sided) one sample T-test)} \end{array} \\
ii) & \quad \alpha = 0.05 \to t_{\alpha, n-1} = t_{5\%, 14} = 2.145 \\
iii) & \quad T_14 = \frac{17.13 - 16.5}{\frac{1.2069}{\sqrt{15}}} \simeq 2.025 (\lt 2.145) \\
iv) & \quad \text{Therefore, accept the null hypothesis } H_0
\end{align*}
$$

$\quad$ In conclusion, there is no significant difference between the first algorithm and the population.

**3. One way to measure a person’s fitness is to measure their body fat percentage. Average body fat percentages vary by age, but according to some guidelines, the normal range for men is 15-20% body fat, and the normal range for women is 20-25% body fat. Our sample data is from a group of men and women who did workouts at a gym three times a week for a year. Then, their trainer measured the body fat. The table below shows the data.**

$$
\begin{array}{|c|c|}
\hline
\mathbf{\text{Group}} & \mathbf{\text{Body Fat Percentages}} \\
\hline
\mathbf{\text{Men}} & \begin{array}{c|c|c|c|c}
13.3 & 6.0 & 20.0 & 8.0 & 14.0 \\
\hline
19.0 & 18.0 & 25.0 & 16.0 & 24.0 \\
\hline
15.0 & 1.0 & 15.0 & & \\
\end{array} \\
\hline
\mathbf{\text{Women}} & \begin{array}{c|c|c|c|c}
22.0 & 16.0 & 21.7 & 21.0 & 30.0 \\
\hline
26.0 & 12.0 & 23.2 & 28.0 & 23.0 \\
\end{array} \\
\hline
\end{array}
$$

**Is there any significant difference between body fat percentages of men vs women? (20 points)**

$\quad$ There are two different sample groups (men, women) so that two sample T test is used to compare these two groups. Calculating the required values with $n_1 = 13, n_2 = 10$,

$$
\begin{array}{ll}
\bar{X}_1 & = \frac{13.3 + 6.0 + 20.0 + 8.0 + 14.0 + 19.0 + 18.0 + 25.0 + 16.0 + 24.0 + 15.0 + 1.0 + 15.0}{13} \\
& = \frac{194.3}{13} \simeq 14.94 \\
\bar{X}_2 & = \frac{22.0 + 16.0 + 21.7 + 21.0 + 30.0 + 26.0 + 12.0 + 23.2 + 28.0 + 23.0}{10} \\
& = \frac{222.9}{10} \simeq 22.29 \\
S_1 & = \sqrt{\frac{\sum_{i=1}^{n_1}(X_i - \bar{X}_1)^2}{n_1-1}} \simeq 6.8426 \\
S_2 & = \sqrt{\frac{\sum_{i=1}^{n_2}(X_i - \bar{X}_2)^2}{n_2-1}} \simeq 5.3197 \\
\sigma_{12} & = \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}} = \sqrt{\frac{6.8426^2}{13} + \frac{5.3197^2}{10}} \simeq 2.5361 \\
\end{array}
$$

$\quad$ Conducting the two sample T test,

$$
\begin{align*}
i) & \quad \begin{array}{ccc} H_0: & M_1 = M_2 \\ H_1: & M_1 \neq M_2 & \text{(two-tailed (sided) T-test)} \end{array} \\
ii) & \quad \alpha = 0.05 \to t_{\alpha, n_1 + n_2 - 2} = t_{5\%, 21} = 2.080 \\
iii) & \quad T_{21} = \frac{22.29 - 14.94}{2.5361} \simeq 2.8587 (\gt 2.080) \\
iv) & \quad \text{Therefore, reject the null hypothesis } H_0
\end{align*}
$$

$\quad$ There is consequently a significant difference in body fat percentages between men and women groups.

**4. A researcher wants to do a research on people's body height (in meter) in a specific city so he measures the height of 36 random persons and the results are: {1.8, 1.72, 1.85, 1.38, 1.58, 1.65, 1.9, 1.83, 1.9, 1.7, 1.75, 1.23, 1.6, 1.65, 1.45, 1.42, 1.82, 1.87, 1.53, 1.65, 1.59, 1.78, 1.69, 1.52, 1.82, 1.63, 1.78, 1.98, 1.62, 1.6, 1.82, 1.62, 1.8, 1.75, 1.82, 1.52}. Suppose that from previous studies which has been done 50 years ago, the average height of persons  was determined to be 1.8 and standard deviation is 0.3 in this city.**

**Can this data be used to show that the average height of individuals in this city has changed in the last 50 years(The acceptable threshold for significance is 1%)? (Show your calculations).(15 points)**

$\quad$ Since the number of samples is greater than 30 ($n = 36$), z-test is used to test the hypothesis with the given values $M_0 = 1.8, \sigma = 0.3$, and the sample mean which is derived as

$$
\begin{array}{l}
\bar{X} & = \frac{1.8 + 1.72 + 1.85 + 1.38 + 1.58 + 1.65 + 1.9 + \cdots + 1.82 + 1.52}{36} \\
& = \frac{60.62}{36} \simeq 1.684
\end{array}
$$

$\quad$ z-test concludes that the average height of individuals in the city has not changed in the last 50 years, showing that

$$
\begin{align*}
i) & \quad \begin{array}{ccc} H_0: & M = 1.8 \\ H_1: & M \neq 1.8 & \text{(two-tailed Z-test)} \end{array} \\
ii) & \quad \alpha = 0.01 \to Z_{\frac{\alpha}{2}} = 2.575 \\
iii) & \quad Z = \frac{1.684 - 1.8}{\frac{0.3}{\sqrt{36}}} = \frac{-0.116}{0.05} \simeq -2.32 (\gt -2.575) \\
iv) & \quad \text{Therefore, accept the null hypothesis } H_0
\end{align*}
$$

**5. In order to develop a new approach to solve a problem, a student develops a new approach (Method 1) and the result she gets are: {10, 4, 6, 7, 12, 5, 7, 4, 12, 10, 9, 10, 8, 5, 9}. The population has average performance of  8 (consider it as method 2) . The student compares the result and discovers that it seems that his method outperforms the population and she wants to prove it using significance testing with a 5% significance threshold.**

**Evaluate the results in terms of the hypothesis that method 1 has a higher performance than method 2. List all the steps (and formulas) involved in the test and what the result implies for the significance of the hypothesis. (15 points)**

$\quad$ Let me be clear that the number of results refers to the grade of the method. The higher the grade, the better the performance.

$\quad$ Given that $n=15, M_0 = 8, \alpha = 0.05$, the sample mean and the sample standard deviation are calculated as

$$
\begin{array}{ll}
\bar{X} & = \frac{10 + 4 + 6 + 7 + 12 + 5 + 7 + 4 + 12 + 10 + 9 + 10 + 8 + 5 + 9}{15} \\
& = \frac{118}{15} \simeq 7.87 \\
S & = \sqrt{\frac{\sum_{i=1}^{n}(X_i - \bar{X})^2}{n-1}} = \sqrt{\frac{101.7335}{14}} \simeq 2.6957
\end{array}
$$

$\quad$ The one sample T-test is conducted as below,

$$
\begin{align*}
i) & \quad \begin{array}{ccc} H_0: & M = 8 \\ H_1: & M \gt 8 & \text{(right-tailed (sided) one sample T-test)} \end{array} \\
ii) & \quad \alpha = 0.05 \to t_{\alpha, n-1} = t_{5\%, 14} = 1.761 \\
iii) & \quad T_{14} = \frac{7.87 - 8}{\frac{2.6957}{\sqrt{15}}} \simeq \frac{-0.13}{0.696} \simeq -0.1868 (\lt 1.761) \\
iv) & \quad \text{Therefore, accept the null hypothesis } H_0
\end{align*}
$$

resulting in the conclusion that there is not enough statistical evidence to prove that method 1 outperforms method 2.

**6. An instructor wants to use two exams in her classes next year. This year, she gives both exams to the students. She wants to know if the exams are equally difficult and wants to check this by looking at the differences between scores. If the mean difference between scores for students is “close enough” to zero, she will make a practical conclusion that the exams are equally difficult. Here is the data:**

$$
\begin{array}{|c|c|c|}
\hline
\mathbf{\text{Student}} & \mathbf{\text{Exam 1 Score}} & \mathbf{\text{Exam 2 Score}} \\
\hline
\text{Bob} & 63 & 69 \\
\hline
\text{Nina} & 65 & 65 \\
\hline
\text{Tim} & 56 & 62 \\
\hline
\text{Kate} & 100 & 91 \\
\hline
\text{Alonzo} & 88 & 78 \\
\hline
\text{Jose} & 83 & 87 \\
\hline
\text{Nikhil} & 77 & 79 \\
\hline
\text{Julia} & 92 & 88 \\
\hline
\text{Tohru} & 90 & 85 \\
\hline
\text{Michael} & 84 & 92 \\
\hline
\text{Jean} & 68 & 69 \\
\hline
\text{Indra} & 74 & 81 \\
\hline
\text{Susan} & 87 & 84 \\
\hline
\text{Allen} & 64 & 75 \\
\hline
\text{Paul} & 71 & 84 \\
\hline
\text{Edwina} & 88 & 82 \\
\hline
\end{array}
$$

**Is there any significant difference between the scores from 2 different exams? (20 points)**

$\quad$ The problem requires a paired sample T-test to compare the scores from two different exams. Calculating the required values with $n = 16$,

$$
\begin{array}{ll}
diff & = \{ -6, 0, -6, 9, 10, -4, -2, 4, 5, -8, -1, -7, 3, -11, -13, 6 \} \\
\bar{X_d} & = \frac{\sum_{i=1}^{n}diff_i}{n} = \frac{-21}{16} \simeq -1.3125 \\
S_d & = \sqrt{\frac{\sum_{i=1}^{n}(diff_i - \bar{X_d})^2}{n-1}} \simeq 7.002
\end{array}
$$

$\quad$ The paired sample T-test confirms that the exams are equally difficult, presenting that

$$
\begin{align*}
i) & \quad \begin{array}{ccc} H_0: & M_d = 0 \\ H_1: & M_d \neq 0 & \text{(two-tailed (sided) paired sample T-test)} \end{array} \\
ii) & \quad \alpha = 0.05 \to t_{\alpha, n-1} = t_{5\%, 15} = 2.131 \\
iii) & \quad T_{15} = \frac{-1.3125 - 0}{\frac{7.002}{\sqrt{16}}} \simeq -0.7498 (\gt - 2.131) \\
iv) & \quad \text{Therefore, accept the null hypothesis } H_0
\end{align*}
$$

### APPENDIX

* [Z-Table](https://en.wikipedia.org/wiki/Standard_normal_table#Cumulative_(less_than_Z))
* [T-Table](https://en.wikipedia.org/wiki/Student%27s_t-distribution#Table_of_selected_values)
