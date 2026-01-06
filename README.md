
# Airbnb Listings Analysis
### Identifying Demand Drivers beyond just Price and Availability

This project analyzes Airbnb listing data to understand why certain listings underperform despite having competitive prices and high ratings. Rather than treating availability as a proxy for demand, the analysis focuses on **host behavior**, **booking constraints**, and **stay flexibility.**






## Project Objectives

- Understand whether **availability_365** reflects guest demand or host behavior
- Identify factors driving high and low demand using recent reviews
- Compare performance across boroughs, with a focus on **Manhattan** and **Brooklyn**
- Determine whether restrictive minimum-night rules contribute to underperformance
- Provide clear, data-backed recommendations for hosts and the platform


## Key Skills Demonstrated

- Python **(Pandas, NumPy)**
- **Visualizations** using Python **(Matplotlib, Seabron, Plotly Express)**
- Data cleaning & feature engineering
- **Exploratory Data Analysis (EDA)**
- Marketplace & behavioral analytics
- Business-focused data storytelling



## Business Questions Answered

- Is availability_365 a reliable indicator of demand?
- Why do Brooklyn listings outperform Manhattan despite similar supply?
- How do minimum-night restrictions affect review volume?
- Are low-review listings driven by poor guest experience?
## Dataset Overview

This project uses an Airbnb listings dataset covering five New York City boroughs. Each row represents a single listing and includes information about the host, location, price, booking rules, availability, and guest reviews.

The dataset contains both active and inactive listings and reflects host-controlled settings such as minimum nights and calendar availability, rather than actual bookings.

**Key variables used in the analysis include:**

- Borough and neighborhood
- Host ID and number of listings per host
- Price and minimum nights
- Availability over 365 days
- Reviews, recent reviews (last 12 months), last review date, and ratings

**Several features were engineered, including:**

- Host categories
- Stay categories based on minimum nights
- Review-based demand groups
- Flags for potentially inactive listings

The dataset is well suited for **analyzing host behavior, booking restrictions, and demand patterns**, rather than predicting exact revenue.
## Workflow

1. **Data Loading & Preparation**

- Removed duplicate listings
- Dropped invalid and fully null rows
- Standardized data types for analysis
- Staged cleaned data for exploration

2. **Data Cleaning & Feature Engineering**

- Converted rating fields from strings to floats
- Flagged studio listings
- Created price_per_bedroom feature
- Handled extreme price outliers (capped at $1500)
- Created stay categories based on minimum_nights
- Classified hosts into Casual, Small Business, Professional, and Large Business

3. **Exploratory Data Analysis (EDA)**

- Host behavior analysis using **host_id**
- Supply and availability distribution across boroughs
- Correlation checks between **price, availability, reviews, and ratings**
**Identified potentially inactive listings using:**
- Availability
- Reviews in the last 12 months
- Year of last review
## Key Findings

1. Availability Is Not a Measure of Demand

- No meaningful relationship between availability and price
- No meaningful relationship between availability and reviews
- Listings with zero availability often showed no recent activity
**Conclusion:** Availability reflects host decisions, not guest demand.

2. Host Behavior Drives Underperformance

- **~60% of listings belong to casual hosts**
**Casual hosts are more likely to:**
- Block calendars
- Have inactive listings
- Use restrictive minimum-night rules

3. Low Reviews Do Not Mean Poor Quality

- Ratings are heavily skewed toward high scores
- Many low-review listings are still highly rated
- **Underperformance is driven by accessibility, not guest dissatisfaction**
## Main Analysis Question

**Although Manhattan and Brooklyn have similar supply levels:**

- **Brooklyn listings appear more often in the high-review group**
- **Manhattan listings are overrepresented in the low-review group**

**This occurs despite Manhattan having more short-stay listings.**

**Why?**

### *Role of Unrated Listings in Manhattan Underperformance*
A key difference between Manhattan and Brooklyn lies in the volume of unrated listings, particularly among short-stay listings.

- Manhattan has **1,648** unrated listings, compared to **1,080** in Brooklyn
- Manhattan also contains significantly more unrated weekend-stay listings
- While **Brooklyn only has 47 unrated** weekend-stay listings

This suggests that while Manhattan appears to offer more short-stay supply, **a large portion of that supply does not convert into reviews**, reducing visibility and perceived demand.

**Key Implication:** Manhattan’s underperformance is driven not by a lack of short-stay listings, but by a higher share of short-stay listings that remain unrated, **making them less competitive in search and review-based demand metrics.**
## Impact of Minimum-Night Restrictions

- Weekend stays consistently appear more in high-demand groups
- Monthly stays dominate the dataset but underperform in reviews

**Estimated:**

- ~55% of Manhattan listings may be underperforming
- ~38% due to restrictive minimum-night rules alone
- ~36% of Brooklyn listings show similar patterns

**Key Insight:**
Shorter stays enable demand, but their impact depends on competition and host engagement.
## Business Impact

This project shows how:

- Host-controlled rules directly affect listing performance
- Platforms risk misinterpreting availability as demand
- Many listings could improve performance without lowering prices

The analysis provides a framework for identifying hidden underperformance in marketplace data.
## Recommendations

### **For Hosts**

- Allow stays of 7 nights or fewer, especially on weekends
- Avoid keeping calendars closed for long periods, as this reduces visibility and review activity
- Actively encourage guests to leave reviews especially for listings with:
    - No ratings 
    - Very few recent reviews 

**Conclusion:** Listings with no ratings or very low reviews appear less trustworthy to guests and are shown less frequently in search results. Increase review activity will help improve **visibility**, **credibility**, and **demand.**


### **For the Platform**

- Do not treat availability as a demand metric
- Flag inactive listings separately from low-performing ones
- Educate hosts on the cost of restrictive booking rules
## Limitations & Nuance

- **Availability shows when a host allows bookings, not actual bookings**
- **Reviews are a proxy for demand; not all guests leave reviews**
- Long-term stays naturally generate fewer reviews
- Host intent (blocking vs inactivity) is inferred, not directly observed
- **Minimum nights improve performance within a borough but do not fully explain differences between boroughs**

Despite these limitations, the findings consistently show that booking flexibility and host behavior play a major role in demand visibility.
## Conclusion

This project demonstrates the ability to challenge assumptions, work with imperfect real-world data, and extract insights that matter to both businesses and users.
