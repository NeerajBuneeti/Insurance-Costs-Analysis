# **Analysis of Insurance Costs**

### Overview
This project analyzes an insurance dataset to identify key factors influencing medical costs and develops predictive models for forecasting expenses. The study leverages statistical analysis, data visualization, and machine learning techniques to uncover insights that can aid insurers, policymakers, and individuals.

---

### Dataset Description
- **Source**: Publicly available insurance dataset.
- **Number of Records**: 1,338.
- **Features**:
  1. `age`: Age of the policyholder (numeric).
  2. `sex`: Gender (categorical: male/female).
  3. `bmi`: Body Mass Index (numeric).
  4. `children`: Number of dependents (numeric).
  5. `smoker`: Smoking status (categorical: yes/no).
  6. `region`: Residential region in the US (categorical: northeast/southeast/northwest/southwest).
  7. `expenses`: Medical costs billed by health insurance (numeric).

---

### Problem Statement
Healthcare costs are a growing concern globally, impacting financial well-being and access to medical services. This project aims to understand the factors driving medical expenses and develop predictive models to enhance cost efficiency and healthcare planning.

---

### Objectives
1. Identify key factors influencing medical expenses.
2. Develop predictive models for accurate expense forecasting.
3. Provide actionable insights for healthcare policy and insurance pricing.

---

### Methodology

#### Data Preprocessing
- Checked for missing values (none found).
- Converted categorical variables (`sex`, `smoker`, `region`) into factors.
- Identified and removed outliers using Z-scores.

#### Exploratory Data Analysis (EDA)
- Visualized distributions of features using histograms, boxplots, and scatter plots.
- Key findings:
  - Smokers incur significantly higher medical expenses.
  - Positive correlations between age, BMI, and expenses.

#### Feature Engineering
- Created polynomial features for `age` and `BMI` to capture nonlinear relationships.
- Grouped ages into categories (`Age_Group`) for better interpretability.

#### Model Selection and Development
1. **Linear Regression**:
   - Simple yet interpretable model.
   - R² = 0.758 on training data.
2. **Polynomial Regression**:
   - Captured nonlinear relationships.
   - Improved R² to 0.762.
3. **Regularized Regression**:
   - Lasso (λ = 72.58) and Ridge (λ = 915.88) to prevent overfitting.
4. **Log-transformed Linear Regression**:
   - Addressed heteroscedasticity; achieved R² = 0.775.

#### Model Evaluation
- Metrics used: Mean Squared Error (MSE), R², cross-validation scores.
- Cross-validation ensured robustness across data splits.

---

### Results and Insights
1. **Significant Predictors**:
   - Smoking status: Smokers incur ~$23,926 more in expenses.
   - Age & BMI: Positive correlation with expenses.
   - Number of children: Each additional child increases costs by ~$505.
2. **Model Performance**:
   - Best model: Log-transformed regression with R² = 0.775.
3. **Regional Differences**:
   - Southeast and Southwest regions have lower average expenses compared to the Northeast.

---

### Conclusion
The analysis highlights smoking status, age, BMI, and number of children as primary drivers of medical expenses. The log-transformed regression model provided the best performance, offering actionable insights for healthcare policy and insurance pricing.

---

### Future Work
1. Incorporate additional features such as income or lifestyle habits for better predictions.
2. Explore advanced machine learning models like Random Forests or Gradient Boosting for improved accuracy.
3. Extend the analysis to larger, more diverse datasets for generalizability.

---

### How to Run the Project

#### Prerequisites
1. Install R or Python (depending on your preferred environment).
2. Required libraries:
   - For R: `tidyverse`, `ggplot2`, `caret`, `glmnet`.
   - For Python: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`.

#### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/insurance-cost-analysis.git
   cd insurance-cost-analysis
   ```
2. Load the dataset (`insurance.csv`) into your working directory.
3. Run the analysis script:
   ```bash
   Rscript analysis.R
   # OR if using Python:
   python analysis.py
   ```
4. View results in the output directory (`/results`).

---

Feel free to contribute by submitting issues or pull requests!

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/33749695/70682a89-c717-4ccf-8966-5eab62fc04c2/annotated-Analysis-20of-20Insurance-20Costs.pdf
[2] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/33749695/8c6fa2ea-0227-4cab-9f71-46c9cb395678/Project-1.html
[3] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/33749695/56683318-6168-4932-ba0c-0635e6951090/insurance_project-1.html
[4] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/33749695/70682a89-c717-4ccf-8966-5eab62fc04c2/annotated-Analysis-20of-20Insurance-20Costs.pdf
[5] https://www.hatica.io/blog/best-practices-for-github-readme/
[6] https://coding-boot-camp.github.io/full-stack/github/professional-readme-guide/
[7] https://tilburgsciencehub.com/topics/collaborate-share/share-your-work/content-creation/readme-best-practices/
[8] https://www.makeareadme.com
[9] https://github.com/banesullivan/README
[10] https://github.com/othneildrew/Best-README-Template
[11] https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/
[12] https://gist.github.com/PurpleBooth/109311bb0361f32d87a2
[13] https://www.youtube.com/watch?v=rCt9DatF63I
[14] https://stackoverflow.com/questions/9331281/how-can-i-test-what-my-readme-md-file-will-look-like-before-committing-to-github
[15] https://www.youtube.com/watch?v=E6NO0rgFub4
[16] https://gist.github.com/DomPizzie/7a5ff55ffa9081f2de27c315f5018afc
[17] https://www.reddit.com/r/learnprogramming/comments/vxfku6/how_to_write_a_readme/
[18] https://www.readme-templates.com
[19] https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
[20] https://rahuldkjain.github.io/gh-profile-readme-generator/
[21] https://github.com/jehna/readme-best-practices
[22] https://readme.so
[23] https://docs.github.com/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes
[24] https://www.reddit.com/r/programming/comments/l0mgcy/github_readme_templates_creating_a_good_readme_is/
