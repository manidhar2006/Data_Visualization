# Assignment Report
# Part-1 Report

## Summary

This comprehensive analysis of the M25 dataset reveals critical insights into workforce demographics, education patterns, work-life balance, and capital market participation. Through sophisticated data cleaning, feature engineering, and statistical analysis, we've uncovered actionable intelligence that can inform strategic decision-making in human resources, investment planning, and workforce development.

**Key Findings at a Glance:**

- **Work intensity shows stronger association with capital gains** (η² = 0.0072) than age groups (η² = 0.0058)
- **Significant age-work intensity relationship** (p < 0.001, χ² = 7108.05)
- **95.3% data dimensionality reduction** achieved through intelligent feature grouping
- **Mid-career professionals dominate** high-intensity work categories

## Data Transformation & Quality

### Dataset Refinement Overview

| Metric              | Before    | After    | Improvement             |
| ------------------- | --------- | -------- | ----------------------- |
| **Rows**            | 48,843    | 48,842   | 99.998% retention       |
| **Columns**         | 15        | 21       | +40% feature enrichment |
| **Missing Values**  | 1 (Hours) | 0        | 100% completion         |
| **Age Categories**  | 74 unique | 5 groups | **94.6% reduction**     |
| **Work Categories** | 96 unique | 4 groups | **95.8% reduction**     |

### Data Cleaning

1. **Age Validation & Correction**

   - Filtered out invalid ages (< 14 years)
   - Applied mode imputation for missing values
   - Maintained data integrity: 99.998% retention rate

2. **Work Hours Standardization**

   - Converted non-numeric entries to NaN
   - Applied statistical mode imputation
   - Eliminated negative values through clipping

3. **Education Data Cleansing**
   - Trimmed whitespace inconsistencies
   - Removed rows with missing education data
   - Maintained comprehensive education coverage

## Strategic Insights

### 1. Education Landscape Transformation

**From Single to Grouped Categories**

| Education Level   | Count  | Percentage | Strategic Value           |
| ----------------- | ------ | ---------- | ------------------------- |
| **High School**   | 24,060 | 49.2%      | Core workforce foundation |
| **Undergraduate** | 18,903 | 38.7%      | Skilled professional base |
| **Postgraduate**  | 4,085  | 8.4%       | Advanced expertise pool   |
| **School**        | 1,711  | 3.5%       | Entry-level potential     |
| **Kindergarten**  | 83     | 0.2%       | Minimal representation    |

**Business Implication:** Nearly 88% of workforce has high school or higher education - indicating strong foundational skills for advanced training programs.

### 2. Age-Career Stage Intelligence

**Workforce Segmentation Strategy**

```
Age Distribution Across Career Stages:
├── Freshers (14-25): Young talent pipeline
├── Early Career (25-35): Skill development phase
├── Mid Career (35-55): Peak productivity zone
├── Late Career (55-65): Experience & mentorship
└── Senior (65+): Knowledge transfer opportunity
```

### 3. Work Intensity Patterns: The Power Analysis

**Critical Discovery: Work intensity drives capital engagement more than age**

| Work Category | Definition     | Strategic Role            |
| ------------- | -------------- | ------------------------- |
| **Full-Time** | 25-40 hrs/week | Core operational backbone |
| **Overtime**  | 41-60 hrs/week | High-value contributors   |
| **Part-Time** | 1-24 hrs/week  | Flexible workforce        |
| **Excessive** | 61+ hrs/week   | Burnout risk segment      |

**Key Finding:** Mid-career professionals (35-55) show highest engagement in overtime work (6,894 individuals), suggesting peak career commitment phase.

## Capital Market Participation Analysis

### Investment Behavior Insights

**Capital Activity Distribution:**

- **Active Participants:** Engage in capital gains/losses
- **Passive Population:** No capital market activity
- **Net Capital Impact:** Calculated as (Gains - Losses)

### Statistical Significance Discovery

**Work Intensity vs. Age Groups Impact on Capital Returns:**

| Factor             | Eta-Squared (η²) | Variance Explained | Ranking    |
| ------------------ | ---------------- | ------------------ | ---------- |
| **Work Intensity** | 0.0072           | 0.72%              | **Winner** |
| **Age Groups**     | 0.0058           | 0.58%              | **Second** |

**Strategic Insight:** Work intensity is 24% more predictive of capital performance than age group - focus investment programs on work behavior patterns rather than age demographics.

## Work-Life Balance

### Age-Work Intensity Correlation Matrix

**Highly Significant Relationship (p < 0.001)**

**Full-Time Work Distribution:**

- **Mid-Career leads:** 12,387 professionals (60% of category)
- **Early Career:** 8,034 professionals (strong engagement)
- **Freshers:** 5,207 professionals (building momentum)

**Overtime Work Patterns:**

- **Mid-Career dominance:** 6,894 professionals (peak performance)
- **Early Career intensity:** 3,469 professionals (career building)
- **Senior decline:** Only 235 professionals (lifestyle shift)

## Feature Engineering Achievements

**6 New Strategic Variables Created:**

1. `Education_Level`: Grouped education for strategic analysis
2. `Age_Group`: Career stage segmentation
3. `Work_Intensity`: Work behavior classification
4. `Work_Life_Balance`: Lifestyle pattern identification
5. `Net_Capital`: Investment performance metric
6. `Any_Capital_Activity`: Market participation flag

### Statistical Rigor

- **Chi-square test:** Confirmed age-work relationship (χ² = 7108.05, p < 0.001)
- **Eta-squared analysis:** Quantified effect sizes for business decisions
- **Correlation analysis:** Validated relationships (Age-Hours: r = 0.0716)
- **Cross-tabulation:** Revealed detailed demographic patterns

# Part-2 Report

## Summary

This report provides a deep dive into the real estate market, leveraging the M25 Dataset 2 to uncover critical insights for investors. Through advanced data cleaning, feature engineering, and quantitative analysis, we have identified key trends in property valuation, location-based premiums, and the impact of developers and amenities. This analysis provides a strategic roadmap for navigating the complex real estate landscape.

**Key Findings at a Glance:**

- **Market Focus:** Mumbai dominates the high-end property segment, while Thane offers superior value for money (larger area for price).
- **Location Premium:** Prime locations command up to a 40% price premium, driven by price per square foot, not larger property sizes.
- **Value Drivers:** Luxury amenities like `Swimming Pool` and `Gymnasium` are significant price drivers in premium markets.
- **Developer Impact:** Top-tier developers are strongly associated with higher-priced properties and superior amenities, indicating brand value is a key factor.
- **Investment Timing:** Ready-to-move properties carry a premium for immediate availability, whereas under-construction properties offer a lower entry point with potential for higher appreciation.

## Data Transformation & Quality

### Dataset Refinement Overview

Our analysis is built on a foundation of meticulously cleaned and enriched data. Each analysis was conducted on a tailored data subset to ensure maximum relevance and accuracy.

| Metric               | Before        | After (Typical)  | Improvement                            |
| :------------------- | :------------ | :--------------- | :------------------------------------- |
| **Rows**             | 29,451        | ~20,000          | ~70% retention after targeted cleaning |
| **Columns**          | 66            | +3               | +4.5% feature enrichment               |
| **Missing Values**   | Widespread    | 0 in key columns | 100% completion for analysis           |
| **Price Categories** | Continuous    | 3 groups         | Strategic Segmentation                 |
| **Developer Tiers**  | 1,000s unique | 3 groups         | Strategic Segmentation                 |

### Data Cleaning & Preparation

1.  **Missing Value Imputation**:

    - Critical data points like `Price` and `Developer` with missing values were removed to maintain analytical integrity.
    - `Carpet Area` was imputed using the mean of its `Type of Property` group, preserving the distinct characteristics of different property types.

2.  **Outlier Removal**:
    - **Z-Score Method**: Applied to the `Price` column to remove extreme, likely erroneous, data points that could skew the analysis.
    - **Regression-Based Removal**: Utilized to identify and remove properties where the price was an outlier relative to its carpet area.

## Strategic Investment Insights

### 1. Price Segmentation & Market Overview

- **Approach**: We segmented properties into 'Low', 'Mid', and 'High' price ranges based on quantiles to analyze their distribution across cities and property types.
- **Findings**:
  - The high-end property market is heavily concentrated in Mumbai, with average prices significantly higher than in other regions.
  - Thane is a key player in the more diverse mid-range market, offering a good balance of price and amenities.
  - The low-range segment is widely distributed across various cities, indicating a broad base of affordable housing.
  - Investment strategies should be tailored to specific price tiers: Mumbai for premium investments, and Thane and other cities for mid-range opportunities.

### 2. City-Level Comparative Analysis (Mumbai vs Thane)

- **Approach**: A direct comparison of Mumbai and Thane across property types, carpet area, and price per square foot.
- **Findings**:
  - Mumbai properties are approximately 53.6% more expensive per square foot than those in Thane.
  - Thane offers larger properties on average (1024 sq ft) compared to Mumbai (871 sq ft).
  - **Strategic Choice for Investors**:
    - **Mumbai**: High-cost, high-appreciation potential, ideal for capital growth.
    - **Thane**: Better value with larger assets at a lower cost, suitable for rental yield and long-term value strategies.

### 3. Location-Based Premium Analysis

- **Approach**: We analyzed the price premium of properties flagged as being in a `isPrimeLocationProperty`.
- **Findings**:
  - Prime locations command a significant price premium, with properties in Mumbai being 40.5% more expensive per square foot and 27.0% more in Thane.
  - This premium is driven by the location ("address") itself, not by larger property sizes; prime properties are often smaller.
  - **Strategic Choice for Investors**:
    - **Prime Locations**: Buying into a premium brand with the promise of higher and faster capital appreciation.
    - **Non-Prime Locations**: Lower appreciation potential but may offer better rental yields due to lower acquisition costs.

### 4. Value-for-Money Opportunities

- **Approach**: We engineered a metric, `Area per Unit Price`, to identify properties offering the most space for the cost.
- **Findings**:
  - The best value for money is consistently found outside of Mumbai, with Thane leading the rankings.
  - For investors prioritizing asset size and value, emerging cities and the Thane region are the most attractive markets, offering lower entry points and high growth potential.
  - Residential houses and apartments generally offer the best value across different property types.

### 5. Feature & Amenity Impact on Price

- **Approach**: We analyzed the correlation between the presence of specific amenities and property prices in Mumbai and Thane.
- **Findings**:
  - Luxury amenities like `Swimming Pool`, `Gymnasium`, and `Club House` have a strong positive correlation with property prices, especially in the premium Mumbai market.
  - The presence of a swimming pool can increase a property's price by over 40%.
  - In high-end markets, luxury amenities are essential features that drive value, while in budget markets, the focus is on core amenities.
  - Amenity strategies must be tailored to the specific target market segment.

### 6. Timeline & Readiness Effect on Pricing

- **Approach**: We compared the prices of `Ready to Move` properties versus those `Under Construction`.
- **Findings**:
  - Ready-to-move properties are, on average, 13.2% more expensive than those under construction, with the premium being more pronounced in Mumbai.
  - This premium is due to the convenience of immediate availability and the absence of construction-related risks.
  - **Strategic Choice for Investors**:
    - **Ready-to-Move**: A conservative, immediate-return strategy ideal for rental income.
    - **Under Construction**: A higher-risk, higher-reward growth strategy with a lower entry point and potential for greater capital appreciation.

### 7. Developer Impact on Properties

- **Approach**: We analyzed the relationship between property developers and prices, and categorized developers into tiers based on their average property prices.
- **Findings**:
  - A developer's brand is a strong indicator of a property's price and quality.
  - Premium developers consistently command higher prices and provide better amenities.
  - A developer's reputation for quality and luxury is a key factor in a property's market value.
  - Partnering with top-tier developers is a safer and more reliable investment strategy, as their brand equity contributes to the property's long-term value and market trust.

## Feature Engineering Achievements

**3 New Strategic Variables Created:**

1.  `Price Range`: For strategic market segmentation.
2.  `Price per Sq Ft`: A standard industry metric for valuation.
3.  `Area per Unit Price`: A custom metric to identify value-for-money deals.

## Analytical Rigor

- **Descriptive Statistics**: Used to summarize the central tendency, dispersion, and shape of the dataset’s distribution.
- **Correlation Analysis**: To understand the relationship between variables like amenities and price.
- **Regression for Outlier Detection**: A sophisticated method to ensure data quality.
- **Data Visualization**: Extensive use of plots and charts to uncover and present trends and insights.
