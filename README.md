## Executive Summary: A/B Testing Website Conversion Rates  


This company wanted to know if a new website page (treatment) could increase customer conversions compared to the old page (control). Low conversions from visitors meant lost sales, and the business needed proof before rolling out the new design.  

I analyzed the A/B test data (over 288,000 users) to check if the new page had a meaningful impact on conversion rate.  

---

### What I Did  

1. **Cleaned the data**: Removed users who saw the wrong page for their assigned group.  
2. **Explored the data**: Looked at user groups, conversion rates, and session times.  
3. **Ran a two-sample Z-test**: Checked if the difference in conversion rates was statistically significant.  
4. **Calculated a 95% confidence interval**: Found the possible range of the true difference.  
5. **Tested for practical significance**: Compared results to the minimum detectable effect (MDE) of 2%.  

---

### Key Findings  

- **Control group conversion rate:** 12.03%  
- **Treatment group conversion rate:** 11.87%  
- **Difference:** -0.16% (treatment slightly lower)  
- **p-value:** 0.1953 → **Not statistically significant**  
- **95% confidence interval:** -0.4% to +0.1% → Includes 0  
- **Practical significance:** Did not meet the 2% minimum detectable effect  

---

### What It Means  

- The new page **did not outperform** the old page.  
- There is **no evidence** of a meaningful change in conversion rates.  
- Even the best-case scenario (upper bound of the CI) shows a 0.1% increase, far below the 2% goal.

---

## Exploratory Data Analysis (EDA)

### Session Time by Conversion

<img width="1010" height="391" alt="Session Time by Conversion" src="https://github.com/user-attachments/assets/3ad40efa-4d68-49ed-ba7a-78fc56ca3bc5" />


**Insights:**
- Converted and non-converted users show nearly identical average session durations (~30 minutes).
- This indicates that session length alone isn't a strong conversion predictor.
- Key implications:
  - Conversion drivers are likely qualitative factors (UX, content quality, CTA effectiveness)


### Conversion Rate by Country

<img width="1154" height="379" alt="Conversion Rate by Country" src="https://github.com/user-attachments/assets/1664a247-af7a-401b-a1bd-ad4e81e93dca" />


**Insights:**
- The US leads with 12.05% conversion, followed closely by CA (11.95%) and UK (11.53%).
- Regional differences are minimal (<0.6% variance), suggesting:
  - The experience is equally effective across these markets
  - Cultural/localization factors may have limited impact
  - Potential for standardized global campaigns
 
---

## Data Collection  

The data for this project was obtained from a Kaggle dataset containing results from a live website A/B test.    
- Users were randomly assigned to **control** (old page) or **treatment** (new page) groups.  
- Each record included user ID, group assignment, landing page, conversion status (0/1), country, and session duration.  
- After cleaning invalid assignments and duplicates, the dataset contained **288,541 users**:  
  - Control group: 144,226 users  
  - Treatment group: 144,315 users 

---

## A/B Test Analysis  

### 1. Hypotheses  

- **Null Hypothesis (H₀):**  
  There is no difference in conversion rates between the control and treatment groups.  
  $$p_{control} = p_{treatment}$$  

- **Alternative Hypothesis (H₁):**  
  There is a difference in conversion rates between the control and treatment groups.  
  $$p_{control} \neq p_{treatment}$$  

### 2. Statistical Testing  

We performed a **two-sample Z-test for proportions** to compare the conversion rates:  

- **Control group conversion rate:** 12.03%  
- **Treatment group conversion rate:** 11.87%  
- **Observed difference:** -0.16%  

**p-value:** 0.1953  
- Since the p-value > 0.05, we **failed to reject the null hypothesis**.  

**95% Confidence Interval:** [-0.4%, +0.1%]  
- The CI includes 0, meaning the true difference could be negative or positive.  

### 3. Practical Significance  

We used a **Minimum Detectable Effect (MDE)** of **2%** to assess if the difference matters in practice.  
- The entire CI lies far below ±2%.  
- This shows the observed difference is not practically meaningful.

### 4. Z-test Interpretation  

<img width="577" height="454" alt="Gaussian" src="https://github.com/user-attachments/assets/31cb7e04-589f-4ae4-bc51-05ff2257c327" />


- **Standard Error (SE):** 0.0012  
  - Shows the expected variation in the difference of conversion rates.  
- **Test Statistic (Z):** 1.295  
  - The observed difference is 1.295 standard errors away from 0.  
- **Z-critical (±1.96):**  
  - Threshold for a 95% confidence level.  

**Conclusion:**  
Since 1.295 < 1.96, the test statistic does not fall in the rejection region.  
We fail to reject the null hypothesis: there is no statistically significant difference.

---

## Recommendations  

- **Do not roll out the new page:** There is no evidence that the new page improves conversions.  
- Focus on testing bigger changes to the user experience that could impact conversion more meaningfully (≥2% difference).  
- Consider running follow-up tests with clearer design changes or stronger call-to-action elements.  

---

## Limitations  

1. **Short test duration:** If the test ran for too few days, it might not capture longer-term user behavior.  
2. **Single metric focus:** We only analyzed conversions, not revenue or engagement.  
3. **Data integrity:** While duplicates and mis-assignments were cleaned, other tracking errors could exist.  

---

## Future Work  

1. Run follow-up tests targeting specific user segments (e.g., new vs returning users).  
2. Expand metrics: Include revenue per user and engagement time in analysis.  
3. Optimize test duration and sample size to improve power.  
4. Consider multivariate tests to analyze multiple page elements at once.  

---

## Connect With Me  

I am open to **freelance projects or full-time roles** in **data analytics, product analytics, and A/B testing**.  

📧 **Email:** [oidiagbonmwen@gmail.com]  
🔗 **LinkedIn:** [https://www.linkedin.com/in/osaretin-idiagbonmwen-33ab85339/] 

If you need a data-driven problem solver who can help you run experiments and turn insights into growth, let's talk!  

