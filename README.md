# DDN-DE-experimental-data
Supplementary experimental data and comprehensive statistical results for the paper "DDN-DE: A Dynamic Diverse Neighborhoods-based Differential Evolution Algorithm with Self-learning Control Parameters".
Due to the manuscript's length limits, this repository provides the extended parameter sensitivity analysis results to ensure the reproducibility and transparency of our research.

---

## ⚙️ Parameter Sensitivity Analysis

In our proposed DDN-DE algorithm, achieving an optimal balance between exploration and exploitation relies on specific control parameters. We conducted sensitivity analyses on the CEC2017 benchmark suite ($D=30$) using the Wilcoxon rank-sum test at a significance level of $\alpha = 0.05$.

### 💡 How to read the tables
The statistical results in the tables are denoted by the format `+ / - / =`:
* **`+` (Better):** The number of test functions where the row parameter significantly outperforms the column parameter.
* **`-` (Worse):** The number of functions where the row parameter significantly underperforms compared to the column parameter.
* **`=` (Similar):** The number of functions where there is no statistically significant difference between the two parameters.

*Example: The entry `1/5/24` means the row parameter is significantly better on 1 function, worse on 5 functions, and statistically equivalent on 24 functions.*

---

### 1. Sensitivity Analysis of Neighborhood Size Parameter ($CP$)

The parameter CP controls the dynamic neighborhood size. **Table 3** presents the comprehensive statistical comparison for $CP \in \{0.1, 0.2, \dots, 0.8\}$.

**Table 3: Wilcoxon rank-sum test results obtained for different values of $CP$**

| $CP$ metric | 0.1 | 0.2 | 0.3 | 0.4 | 0.5 | 0.6 | 0.7 | 0.8 |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **0.1 (+/-/=)** | -- | 1/5/24 | 3/8/19 | 9/5/16 | 13/4/13 | 16/2/12 | 18/2/10 | 20/1/9 |
| **0.2 (+/-/=)** | 5/1/24 | -- | 2/5/23 | 5/2/23 | 10/2/18 | 16/3/11 | 19/2/9 | 22/2/6 |
| **0.3 (+/-/=)** | 8/3/19 | 5/2/23 | -- | 4/0/26 | 9/1/20 | 15/0/15 | 21/0/9 | 22/1/7 |
| **0.4 (+/-/=)** | 5/9/16 | 2/5/23 | 0/4/26 | -- | 1/0/29 | 11/0/19 | 15/0/15 | 20/0/10 |
| **0.5 (+/-/=)** | 4/13/13 | 2/10/18 | 1/9/20 | 0/1/29 | -- | 4/0/26 | 9/0/21 | 20/0/10 |
| **0.6 (+/-/=)** | 2/16/12 | 3/16/11 | 0/15/15 | 0/11/19 | 0/4/26 | -- | 3/0/27 | 15/1/14 |
| **0.7 (+/-/=)** | 2/18/10 | 2/19/9 | 0/21/9 | 0/15/15 | 0/9/21 | 0/3/27 | -- | 6/1/23 |
| **0.8 (+/-/=)** | 1/20/9 | 2/22/6 | 1/22/7 | 0/20/10 | 0/20/10 | 1/15/14 | 1/6/23 | -- |

**Analysis & Conclusion:**
Table 3 demonstrates that setting CP = 0.3 yields the most robust optimization performance. Pairwise comparisons reveal that this configuration consistently achieves statistically equivalent or superior results across the majority of the CEC2017 functions compared to other candidates. Consequently, CP = 0.3 is adopted as the default parameter.

<br>

### 2. Sensitivity Analysis of Superior Learning Probability ($spb$)

**Table 4** systematically outlines the statistical comparisons regarding the superior learning probability ($spb$) evaluated within the range of $\{0.1, 0.2, \dots, 0.9\}$. 

**Table 4: Wilcoxon rank-sum test results obtained for different values of $spb$**

| $spb$ metric | 0.1 | 0.2 | 0.3 | 0.4 | 0.5 | 0.6 | 0.7 | 0.8 | 0.9 |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **0.1 (+/-/=)** | -- | 1/1/28 | 1/5/24 | 1/4/25 | 2/6/22 | 1/6/23 | 3/5/22 | 5/2/23 | 10/2/18 |
| **0.2 (+/-/=)** | 1/1/28 | -- | 0/1/29 | 0/3/27 | 1/5/24 | 1/4/25 | 4/2/24 | 7/3/20 | 11/2/17 |
| **0.3 (+/-/=)** | 5/1/24 | 1/0/29 | -- | 0/1/29 | 0/2/28 | 2/4/24 | 3/2/25 | 8/3/19 | 13/1/16 |
| **0.4 (+/-/=)** | 4/1/25 | 3/0/27 | 1/0/29 | -- | 0/0/30 | 1/2/27 | 3/0/27 | 7/1/22 | 12/1/17 |
| **0.5 (+/-/=)** | 6/2/22 | 5/1/24 | 2/0/28 | 0/0/30 | -- | 1/1/28 | 4/1/25 | 10/1/19 | 11/2/17 |
| **0.6 (+/-/=)** | 6/1/23 | 4/1/25 | 4/2/24 | 2/1/27 | 1/1/28 | -- | 3/0/27 | 9/1/20 | 10/1/19 |
| **0.7 (+/-/=)** | 5/3/22 | 2/4/24 | 2/3/25 | 0/3/27 | 1/4/25 | 0/3/27 | -- | 5/1/24 | 10/1/19 |
| **0.8 (+/-/=)** | 2/5/23 | 3/7/20 | 3/8/19 | 1/7/22 | 1/10/19 | 1/9/20 | 1/5/24 | -- | 10/0/20 |
| **0.9 (+/-/=)** | 2/10/18 | 2/11/17 | 1/13/16 | 1/12/17 | 2/11/17 | 1/10/19 | 1/10/19 | 0/10/20 | -- |

**Analysis & Conclusion:**
As indicated in Table 4, the algorithm achieves peak stability and competitive superiority when spb is set to 0.5 or 0.6. To maintain a balanced learning mechanism by preventing premature convergence and sustaining evolutionary momentum, spb = 0.5 is selected as the standard configuration.
<br>

### 3. Sensitivity Analysis of Orthogonal Learning Probability ($opb$)

Furthermore, we conducted a parameter sensitivity analysis for the orthogonal learning probability ($opb$) within the range of $\{0.1, 0.2, \dots, 0.9\}$. The results are detailed in **Table 5**.

**Table 5: Wilcoxon rank-sum test results obtained for different values of $opb$**

| $opb$ metric | 0.1 | 0.2 | 0.3 | 0.4 | 0.5 | 0.6 | 0.7 | 0.8 | 0.9 |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **0.1 (+/-/=)** | -- | 3/1/26 | 3/3/24 | 7/2/21 | 8/3/19 | 9/2/19 | 12/2/16 | 10/3/17 | 15/2/13 |
| **0.2 (+/-/=)** | 1/3/26 | -- | 1/1/28 | 1/1/28 | 7/2/21 | 6/3/21 | 8/2/20 | 9/2/19 | 11/3/16 |
| **0.3 (+/-/=)** | 3/3/24 | 1/1/28 | -- | 1/1/28 | 4/2/24 | 7/4/19 | 10/2/18 | 8/4/18 | 12/2/16 |
| **0.4 (+/-/=)** | 2/7/21 | 1/1/28 | 1/1/28 | -- | 2/2/26 | 5/3/22 | 8/2/20 | 9/2/19 | 13/2/15 |
| **0.5 (+/-/=)** | 3/8/19 | 2/7/21 | 2/4/24 | 2/2/26 | -- | 3/2/25 | 5/2/23 | 7/2/21 | 11/4/15 |
| **0.6 (+/-/=)** | 2/9/19 | 3/6/21 | 4/7/19 | 3/5/22 | 2/3/25 | -- | 4/2/24 | 5/2/23 | 12/2/16 |
| **0.7 (+/-/=)** | 2/12/16 | 2/8/20 | 2/10/18 | 2/8/20 | 2/5/23 | 2/4/24 | -- | 4/2/24 | 10/2/18 |
| **0.8 (+/-/=)** | 3/10/17 | 2/9/19 | 4/8/18 | 2/9/19 | 2/7/21 | 2/5/23 | 2/4/24 | -- | 7/0/23 |
| **0.9 (+/-/=)** | 2/15/13 | 3/11/16 | 2/12/16 | 2/13/15 | 4/11/15 | 2/12/16 | 2/10/18 | 0/7/23 | -- |

**Analysis & Conclusion:**
The Wilcoxon rank-sum test results in Table 5 confirm that opb = 0.1 secures a highly competitive stance. At this value, the algorithm is statistically no worse than—and frequently superior to—configurations utilizing higher probabilities. Thus, opb = 0.1 is chosen to maximize search efficiency.
