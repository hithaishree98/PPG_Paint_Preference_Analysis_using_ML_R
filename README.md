# PPG_Paint_Preference_Analysis_using_ML_R

## Project Sections & What We Learned

### Part I – Exploration  
**What I set out to learn:**  
- Understand how the six color measurements (R, G, B, Hue, Saturation, Lightness) are distributed and interrelated.  
- See whether popular paints (“outcome = 1”) differ noticeably in their color profiles.  

**What I discovered:**  
- The basic color channels (R, G, B) tend to rise and fall together, while Hue varies independently.  
- Popular paints skew toward brighter, more saturated colors—people seem to favor vivid, high-lightness finishes.

---

### Part II – Regression  
**What I set out to learn:**  
- Can we accurately predict the continuous “response” property (e.g. durability/gloss) solely from color inputs?  
- Which modeling approach (linear vs. tree-based vs. boosting) works best?  

**What I discovered:**  
- Simple linear models capture a rough trend, but more flexible methods (Random Forest, XGBoost) reduce prediction error by ~25%.  
- The best model (XGBoost) nails most of the variation—suggesting that even complex color–response relationships can be learned from just six inputs.

---

### Part III – Classification  
**What I set out to learn:**  
- Can we distinguish “popular” versus “less popular” paints by their color formulas?  
- Which classifier gives the most reliable results?  

**What I discovered:**  
- Naive Bayes and logistic regression both perform admirably, but a tuned Gradient Boosting Machine edges them out.  
- Overall accuracy tops out around 95%, meaning color alone is a very strong signal of popularity.

---

### Part IV – Interpretation  
**What I set out to learn:**  
- Which specific color features drive model decisions?  
- Are there particular paints that remain hard to predict?  

**What I discovered:**  
- Lightness and Saturation in the HSL color space are the most decisive factors for both the continuous and binary tasks—people like bright, vivid finishes.  
- A handful of outlier paint formulas consistently confuse every model, hinting at unique combinations that depart from typical trends.

---

Dive into the details—code, charts, and full narrative—by opening the corresponding HTML reports:  
> `Part1_Exploration.html`, `Part2_Regression.html`, `Part3_Classification.html`, `Part4_Interpretation.html`.  
