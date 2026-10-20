<p align="center">
  <img src="https://github.com/joshuabufi-analyst/Asheville-Airbnb-Listings-Analysis/blob/main/photos/Airbnb_Logo_B%C3%A9lo.svg.webp" width="150">
</p>

<h1 align="center" style="font-size: 56px;">
  Asheville Market Expansion Analysis
</h1>

<h2 align="center" style="font-size: 40px;">
  Background &amp; Overview
</h2>

Founded in 2007, Airbnb began when two hosts welcomed three guests into their San Francisco home. Since then, it has grown into a global platform with more than 5.5 million hosts and over 2.5 billion guest arrivals worldwide. Through unique accommodations, experiences, and services, Airbnb enables travelers to connect more authentically with local communities, including Asheville, North Carolina.

Reporting to management, this project evaluates pricing, demand, and host activity trends in Asheville from 2011 to 2025 to help a travel startup assess the feasibility of market expansion. The analysis identifies promising neighborhoods and property types while evaluating potential risks, such as seasonal demand fluctuations, market competition, and reliance on a small number of hosts. Insights and recommendations are provided on the following key areas:

#### **North Star Metrics**
  - **Comparative and Ranking Analysis:** Analyzing Airbnb's Room Type and Neighborhood to assess Median RevPAL and Seasonality Risk
  - **Review & Demand Analysis:** Evaluation of historical booking patterns, focusing on Demand Growth Rate and Supply Growth Rate
  - **Host Analysis:** An assessment of the Top Host Share by Revenue and Median Occupancy Rate

<h2 align="center" style="font-size: 40px;">
  Executive Summary
</h2>

<p align="center">
  <strong>Chart Title</strong>
</p>

<p align="center">
  <img src="https://github.com/joshuabufi-analyst/Asheville-Airbnb-Listings-Analysis/blob/main/photos/Dashboard.png" width="100%">
</p>

<h2 align="center" style="font-size: 40px;">
  Data Structure Overview
</h2>

Airbnb's database structure as seen below consists of three tables: details about each listing, neighborhood codes for listings and historical review activity by listing, with a total row count of 321, 433 records.

<p align="center">
  <img src="https://github.com/joshuabufi-analyst/Asheville-Airbnb-Listings-Analysis/blob/main/photos/ERD.png" width="750">
</p>

*The Excel utilized to organize, prepare and visualize data for the ad hoc report can be found [here](https://github.com/joshuabufi-analyst/Asheville-Airbnb-Listings-Analysis/blob/main/Dashboard/Project%201.xlsb).*

<h2 align="center" style="font-size: 40px;">
  Insights Deep Dive
</h2>

### Caveats & Assumptions
  This analysis applies several assumptions and methodological adjustments to address limitations in the available data. These measures provide a consistent basis for calculating and comparing key performance metrics, while the stated caveats highlight where results may differ from actual or independently verified business outcomes. Therefore, the findings should be interpreted in light of the assumptions and limitations outlined in the analysis.

**Scope of Rental Duration:** The analysis focuses on short-term rentals, defined for this project as stays lasting a few days to fewer than 30 consecutive nights. This scope reflects the conventional short-stay accommodation market, where bookings generate platform service-fee revenue for Airbnb through its website and app. Longer stays were excluded to maintain a consistent focus on short-term accommodation patterns. This cutoff is an analytical assumption rather than a restriction on Airbnb's business model, which also accommodates longer-term stays.

**Missing Price Treatment:** Listings with missing or invalid prices were excluded from the Median RevPAR calculation because a valid price is required to calculate this metric. Price imputation using the median of a specific room type and neighborhood was avoided because listing prices may vary considerably based on property size, location, condition, amenities, and other characteristics that cannot be fully captured by these groupings. These listings remained included in other KPI calculations where the required data fields were available and valid.

**Active Listing Definition:** Listing activity was assessed using two criteria: at least one review in the last 12 months and a reviews-per-month value greater than zero. `availability_365` was analyzed separately because the dataset defines it as the number of days a listing is available for booking within the next 365 days. Unavailable dates may reflect guest bookings or host-blocked calendars; therefore, availability alone cannot reliably establish listing activity or demand. This approach avoids imposing an arbitrary availability threshold and reduces the risk of misclassifying active listings.

**Recent Market Activity Filter:** The market expansion analysis includes listings whose last review date falls between June 16, 2024, and June 16, 2025. This 12-month window serves as a proxy for recent guest activity, helping focus the analysis on listings with evidence of recent market participation. 

### Comparative and Ranking Analysis:
The market's overall median RevPAL (Revenue per Available Listing) is $35.84, below the assigned threshold of $40 per night, indicating that the typical listing generates less revenue per available night than the target benchmark. Meanwhile, the Seasonality Risk Index of 0.15 is below the 0.30 threshold, suggesting relatively low seasonal risk under the established methodology. Together, these findings indicate that **the market has below-target revenue potential but relatively low seasonality risk**. Although revenue performance may be consistently below the target, further analysis is needed to determine whether the market offers sufficient profitability and long-term expansion potential.

### Review & Demand Analysis:
### Host Analysis:

<h2 align="center" style="font-size: 40px;">
  Recommendations
</h2>

Based on the uncovered insights, here are actionable items that Airbnb can take away from our analysis.
