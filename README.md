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
  - **Revenue Viability Analysis:** Analyzing Airbnb's Room Type and Neighborhood to assess Median RevPAL and Seasonality Risk
  - **Review-Based Demand & Supply Analysis:** Evaluation of historical booking patterns, focusing on Demand Growth Rate and Supply Growth Rate
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

Airbnb's database structure as seen below consists of three tables: details about each listing, neighborhood codes for listings and historical review activity by listing, with a total row count of 321, 433 records. The overall dataset has a **Market Data Confidence Index of 92.14%**, exceeding the 90% threshold for high data confidence. This indicates that the dataset meets the established criteria for market data reliability, with relatively few identified data quality issues. However, the index does not guarantee that all records are accurate or free from documentation errors.

<p align="center">
  <img src="https://github.com/joshuabufi-analyst/Asheville-Airbnb-Listings-Analysis/blob/main/photos/ERD.png" width="750">
</p>

*The Excel utilized to organize, prepare and visualize data for the ad hoc report can be found [here](https://github.com/joshuabufi-analyst/Asheville-Airbnb-Listings-Analysis/blob/main/Dashboard/Project%201.xlsb).*

<h2 align="center" style="font-size: 40px;">
  Insights Deep Dive
</h2>

### Caveats & Assumptions
This analysis uses consistent assumptions and adjustments to calculate key metrics, but results should be interpreted in light of the following limitations:

**Scope of Rental Duration:** The analysis focuses on short-term rentals, defined for this project as stays lasting a few days to fewer than 30 consecutive nights. This scope reflects the conventional short-stay accommodation market, where bookings generate platform service-fee revenue for Airbnb through its website and app. Longer stays were excluded to maintain a consistent focus on short-term accommodation patterns. This cutoff is an analytical assumption rather than a restriction on Airbnb's business model, which also accommodates longer-term stays.

**Missing Price Treatment:** Listings with missing or invalid prices were excluded from the Median RevPAR calculation because a valid price is required to calculate this metric. Price imputation using the median of a specific room type and neighborhood was avoided because listing prices may vary considerably based on property size, location, condition, amenities, and other characteristics that cannot be fully captured by these groupings. These listings remained included in other KPI calculations where the required data fields were available and valid.

**Review-Based Demand Indicators:** The number of reviews submitted by Airbnb guests is used as a proxy for booking demand because actual booking records for individual listings are not publicly available due to privacy restrictions. This assumes that review activity is reasonably indicative of booking activity. However, since not all guests leave reviews, review counts may underestimate actual bookings and should not be interpreted as the exact number of reservations.

**Active Listing Definition:** Defined by at least one review in the past 12 months and a positive reviews-per-month value. Availability was assessed separately because unavailable dates may reflect bookings or host-blocked calendars.

**Recent Market Activity Filter:** The market expansion analysis includes listings whose last review date falls between June 16, 2024, and June 16, 2025. This 12-month window serves as a proxy for recent guest activity, helping focus the analysis on listings with evidence of recent market participation. 

### Revenue Viability Analysis:
The market's overall median RevPAL (Revenue per Available Listing) is $35.84 per night, below the assigned threshold of $40, indicating that the typical listing falls short of the revenue benchmark. Meanwhile, the Seasonality Risk Index (SRI) of 0.15 is below the 0.30 threshold, suggesting relatively low seasonal risk under the established methodology. Together, these findings indicate that **the market has below-target revenue potential but relatively low seasonality risk**. However, market-level results may conceal differences among neighborhoods and room types. Further analysis of each neighborhood–room type combination is therefore necessary to identify segments with sufficient revenue potential and more favorable conditions for long-term market expansion.

<table>
  <tr>
    <td width="40%" align="center">
      <p align="center">
      <strong>Homes/apartments in neighborhoods 28803 and 28805 have the most stable revenue potential.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q1.1.png" width="100%">
    </td>
    <td width="60%" valign="top">

  - **Promising opportunity** — Home/Apartment properties in neighborhoods 28803 and 28805 show low seasonality risk (0.28 and 0.14) and median RevPAL values of $43.60 and $40.80 per night, respectively, both exceeding the $40 threshold and indicating stable revenue potential.
  - **High risk, below-target revenue** — Neighborhoods 28804, 28801, and 28715 have high seasonality risk and median RevPAL below the target. Neighborhood 28715 has the highest risk (0.38), while 28801 and 28804 are at the 0.30 threshold. Hosts should improve listing photos and guest reviews, adjust rates to match seasonal demand, maintain competitive off-season pricing, and reserve peak-season profits to cover off-season expenses and potential cash shortfalls.
  - **Low risk, below-target revenue** — Neighborhoods 28732, 28704, and 28806 have low seasonality risk but median RevPAL below $40 per night. Neighborhood 28806 is closest to the target at $38.70. Hosts should assess ADR and occupancy to identify performance gaps, adjust off-peak rates or minimum-stay requirements to boost bookings, raise rates during strong demand, and improve listing photos and guest reviews to increase appeal.
    </td>
  </tr>
</table>

<table>
  <tr>
    <td width="60%" valign="top">

- **Promising opportunity** — Neighborhood 28732: Private rooms have a Seasonality Risk Index of 0.25 and the highest median RevPAL at $87.52 per night, indicating relatively stable demand and strong revenue potential.

- **High risk, below-target revenue** — Neighborhoods 28806, 28801, 28715, and 28803: Neighborhood 28803 has the highest risk index at 2.78. Hosts should improve listing photos and reviews, adjust pricing to seasonal demand, offer competitive off-season rates, and save peak-season earnings for slower periods.

- **Low risk, below-target revenue** — Neighborhoods 28704 and 28804: Neighborhood 28804 comes closest to the target at $37.72 per night. Hosts should assess ADR and occupancy, optimize off-season pricing and minimum stays, adjust rates during peak demand, and improve listing appeal to increase bookings.

- **High risk, above-target revenue** Neighborhood 28805: Median RevPAL exceeds the $40 target at $42.74 per night, but the Seasonality Risk Index is 0.44. Hosts should adjust seasonal pricing, offer competitive off-season rates, and save peak-season earnings for slower periods.
    </td>

    <td width="40%" align="center">
      <p align="center">
      <strong>Private Rooms in neighborhood 28732 have the most stable revenue potential.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q1.2.png" width="100%">
    </td>
  </tr>
</table>

<table width="100%">
  <tr>
    <td width="50%" align="center" valign="center">
      <p align="center">
        <strong>Hotel Rooms in neighborhood 28806 show high revenue potential, but seasonal demand remains inconclusive due to insufficient data.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q1.3.png" width="100%">
    </td>
    <td width="50%" align="center" valign="center">
      <p align="center">
        <strong>All neighborhoods with Shared Room properties exhibit low seasonality risk but below-target revenue.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q1.4.png" width="100%">
    </td>
  </tr>
</table>

  - Hotel Rooms in neighborhood 28806 have a median RevPAL of $54.74 per night, exceeding the $40 target. However, the **Seasonality Risk Index (SRI) of 0 is inconclusive** because it is based on only one September 2024 review, providing insufficient data to assess seasonal demand reliably. Because the coefficient of variation is sensitive to the number of observations, the zero index may reflect insufficient data rather than genuinely stable demand. Additional data are needed before determining the segment’s seasonality risk.

  - In contrast, Hotel Rooms in neighborhood 28803 have a low SRI of 0.22, below the 0.30 threshold, but a median RevPAL of only $1.58 per night. Hosts should investigate pricing, occupancy, and booking availability to identify revenue improvement opportunities before considering expansion.

  - Shared Rooms in neighborhoods 28801, 28804, and 28806 have SRI values **below the 0.30 threshold but exhibit below-target revenue potential.** Neighborhood 28801 has the highest median RevPAL among the three at $27.37 per night, still falling $12.63 below the $40 target. Hosts should assess ADR and occupancy to identify the causes of low revenue, optimize off-season pricing and minimum-stay requirements, adjust rates during peak-demand periods, and improve listing appeal to attract more bookings and increase revenue.

### Review-Based Demand & Supply Analysis:

The market recorded a year-over-year supply growth rate of **16.50%**, exceeding the established 15% threshold and indicating aggressive expansion in active listings. Meanwhile, the **review-based demand growth rate declined by 37.95%**, suggesting a substantial contraction in demand-related review activity.

The combination of increasing supply and declining review-based demand suggests a shift toward a **more competitive, renter-favorable market**, where hosts may face greater pressure to attract bookings and maintain pricing. Rather than indiscriminately reducing prices, hosts should prioritize **strategic pricing, occupancy optimization, and differentiation** through distinctive amenities, property features, and clearly defined target audiences. These strategies may help preserve pricing power amid increasing competition, although their effectiveness requires further validation using listing-level performance data.

Market analysis should evaluate performance by neighborhood and room type to identify the most promising combinations for expansion. External events should also be investigated to provide context for the observed changes in supply and demand. However, additional evidence is needed to determine whether these events contributed to the trends and to what extent they influenced Airbnb market performance.

<table width="100%">
  <tr>
    <td width="50%" align="center" valign="center">
      <p align="center">
        <strong>Review-based demand indicators declined sharply in October 2024 compared with October 2023.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q2.1.png" width="100%">
    </td>
    <td width="50%" align="center" valign="center">
      <p align="center">
        <strong>Review-based supply indicators declined sharply in October 2024 compared with October 2023.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q2.2.png" width="100%">
    </td>
  </tr>
</table>

The review-based demand indicators for 2023 and 2024 followed similar trends from June through September, with demand levels remaining relatively consistent between the two periods. Similarly, the review-based supply indicators for 2024 were slightly higher than those for 2023 but followed a comparable seasonal pattern.

However, October 2024 recorded a sharp year-over-year decline in both indicators, with review-based demand decreasing by 89.52% and review-based supply decreasing by 73.49%. In the subsequent months, the 2024–2025 indicators remained below their corresponding 2023–2024 levels, suggesting a sustained reduction in review activity and in the number of listings identified as active under the study's criteria.

Hurricane Helene, which struck the region in late September 2024, provides a plausible explanation for the sharp October 2024 decline. Official tourism updates reported that October 2024 vacation-rental demand was down 28% year over year, while airport passenger traffic fell by approximately 53%. These independent indicators support the conclusion that the storm severely disrupted Asheville's tourism industry during that period. *Sources:* [*Explore Asheville*](https://marketing.exploreasheville.com/acton/media/43256/thcunov24) and [*Asheville Regional Airport reporting*](https://www.wfae.org/2024-12-13/passenger-traffic-at-asheville-airport-nearly-halved-in-wake-of-hurricane-helene).

<table>
  <tr>
    <td width="60%" valign="center">
      
  **Entire Home/Apartment properties in neighborhoods 28805 and 28804 exhibit negative review-based demand growth, while their supply growth rates remain below the 15% threshold for aggressive expansion.** This indicates declining review-based demand without evidence of aggressive supply growth under the established criteria. Hosts should protect profitability by setting cost-based minimum rates, encouraging longer stays through minimum-night requirements and targeted discounts, highlighting premium amenities, and using smart devices to reduce operating costs. Monitor conversion, occupancy, and contribution margin to assess performance.

**Entire Home/Apartment properties across the remaining neighborhoods face declining review-based demand and supply growth above 15%.** Neighborhood 28732 has the least negative demand growth (−10.62%), while 28704 has the highest supply growth (20.15%). Hosts should optimize ADR and RevPAL, differentiate listings, and adjust cleaning fees while maintaining profitability. Track RevPAL, occupancy, and contribution margin to evaluate results.
    </td>
    <td width="40%" align="center">
      <p align="center">
      <strong>Entire Home/Apartment demand is declining in 28805 and 28804, with supply growth below 15%.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q2.3.png" width="100%">
    </td>
  </tr>
</table>

<table>
  <tr>
    <td width="40%" align="center">
      <p align="center">
      <strong>Private Room demand is declining in 28732 and 28704, with 0% supply growth.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q2.4.png" width="100%">
    </td>
    <td width="60%" valign="center">

**Private Room properties in neighborhoods 28732 and 28704 exhibit negative review-based demand growth of −82.08% and −9.24%, respectively, while their review-based supply growth rates remain at 0%.** This indicates declining review-based demand, particularly in neighborhood 28732, without observed growth in the supply indicator, potentially putting pressure on occupancy and revenue. Hosts should adopt flexible pricing and minimum stays, address maintenance and guest concerns, and improve listing appeal. Monitor occupancy, RevPAL, and booking conversion.

**Private Room properties across the remaining neighborhoods face declining review-based demand alongside supply growth exceeding the 15% threshold for aggressive expansion.** Neighborhood 28804 has the steepest demand decline at −93.92%, while neighborhood 28801 has the highest supply growth at 43.36%. Hosts should optimize ADR, highlight distinctive amenities, and adjust cleaning fees to remain competitive while protecting profitability. Monitor RevPAL, occupancy, and contribution margin.
    </td>
  </tr>
</table>

<table width="100%">
  <tr>
    <td width="50%" align="center" valign="center">
      <p align="center">
        <strong>Hotel Rooms in 28803 face declining demand, while 28806 faces stagnant demand and rising supply, increasing competition.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q2.5.png" width="100%">
    </td>
    <td width="50%" align="center" valign="center">
      <p align="center">
        <strong>Shared Rooms in 28801 and 28806 show declining demand with stable supply, while 28804 experiences faster demand decline than supply.</strong>
      </p>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q2.6.png" width="100%">
    </td>
  </tr>
</table>

  - **Hotel Room properties in neighborhood 28803 exhibit a sharp decline in review-based demand growth of −152.23%, while review-based supply growth remains at 0%.** This suggests weakening demand without observed growth in the supply indicator, potentially putting pressure on occupancy and revenue. Hosts should investigate the decline, adopt flexible pricing and minimum-stay policies, address maintenance and guest-service issues, and highlight distinctive amenities to improve listing competitiveness.
  - **In contrast, neighborhood 28806 has 0% review-based demand growth versus 100% supply growth, suggesting increased competition.** Hosts should monitor RevPAL, occupancy, operating costs, and contribution margin over 12–24 months. To improve short-term performance, test dynamic pricing, promotional offers, and shorter minimum stays. If profitability continues to decline, consider long-term rentals for more stable cash flow. Evaluate each strategy based on booking conversion, RevPAL, and contribution margin.
  - **Shared Room properties in neighborhoods 28801 and 28806 exhibit negative review-based demand growth of −91.57% and −42.07%, respectively, while review-based supply growth remains at 0%.** This suggests weakening demand without observed growth in the supply indicator, potentially putting pressure on occupancy and revenue, particularly in neighborhood 28801. Hosts should investigate the demand decline, adopt flexible pricing and minimum-stay policies, address maintenance and guest-service issues, and highlight distinctive amenities to improve listing competitiveness. Monitor occupancy, RevPAL, and contribution margin to evaluate the effectiveness of these strategies.
  - **Shared Room properties in neighborhood 28804 show declining review-based demand (−42.07%) and supply (−13.10%), with demand falling faster.** Hosts should investigate demand trends, adjust pricing and minimum stays, improve guest services, and highlight unique amenities. Monitor occupancy, RevPAL, and contribution margin to assess performance.

### Host Analysis:
Asheville, North Carolina, has 2,163 active short-term rental listings in the dataset, while the median occupancy rate is 24.93%, substantially below the established 40% threshold. This suggests that the typical listing is not meeting the target occupancy benchmark, potentially indicating weak booking performance or seasonal demand. The top 10 hosts account for 13.03% of total listing revenue, indicating that revenue is distributed across a broader group of market participants rather than being overwhelmingly concentrated among the leading 10 hosts. This may suggest a relatively fragmented competitive landscape, although further analysis of host counts and individual revenue shares is needed to confirm this interpretation. Further analysis of demand trends, supply growth, pricing, and neighborhood-level performance is needed to determine whether market conditions support expansion.

<table width="100%" style="table-layout: fixed; border-collapse: collapse;">
  <tr>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>All neighborhoods with Entire Home/Apartment listings have median occupancy rates below the 40% benchmark.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.1.png" width="100%">
    </td>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Neighborhood 28715 has the fewest active listings, most of which are managed by independent hosts.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.5.png" width="100%">
    </td>
  </tr>
</table>

<p align="center">
  <img
    src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.9.png"
    width="50%"
    style="border: 2px solid #808080; padding: 5px;"
  >
</p>

All neighborhoods with Entire Home/Apartment listings have median occupancy below the 40% benchmark, indicating a market-wide occupancy shortfall. Top-host revenue shares are also below 40%, suggesting limited revenue concentration among leading hosts; however, this alone does not establish competitive intensity.
- **Neighborhood 28803:** Has 270 active listings and the highest median occupancy (30.14%). Independent hosts manage 49.63% of inventory, while top hosts account for 8.47% of revenue.
- **Neighborhood 28805:** Has 191 active listings, with 58.63% managed by independent hosts. Median occupancy is 29.32%, and top-host revenue share is 9.46%.
- **Neighborhood 28804:** Has 271 active listings, with 49.07% managed by independent hosts. Despite its larger inventory, median occupancy is only 23.56%, while top-host revenue share is 14.51%.
Overall, 28803 has the highest occupancy, while 28804 has the lowest. All three remain below the target, requiring further analysis of revenue potential, supply and demand trends, and seasonality risk to determine the most attractive expansion opportunity.

<table width="100%" style="table-layout: fixed; border-collapse: collapse;">
  <tr>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Private Rooms in neighborhoods 28732 and 28715 are tied for the lowest number of active listings.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.2.png" width="100%">
    </td>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Host composition reveals a potential difference in the competitive landscape of neighborhoods 28732 and 28715.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.6.png" width="100%">
    </td>
  </tr>
</table>

<p align="center">
  <img
    src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.10.png"
    width="50%"
    style="border: 2px solid #808080; padding: 5px;"
  >
</p>

**Private Rooms in neighborhoods 28732 and 28715 have the fewest active listings**, suggesting limited competition. However, 28732 has a median occupancy rate of 99.45%, compared with 35.62% in 28715, which falls below the 40% benchmark. **Neighborhood 28732 appears more promising for expansion**, combining limited inventory with exceptionally high occupancy. However, its small sample size may limit the reliability of this finding.

Host composition also differs: two of three hosts in 28732 are mid-scale (6–11 properties), while two of three in 28715 are small-scale (2–5 properties). Both neighborhoods have one independent host. This suggests that competitors in 28732 may have more experience managing multiple properties or greater operational capacity. Nevertheless, host portfolio size alone does not establish their financial resources or actual competitive advantage.

Neighborhood 28704 has 9 active Private Room listings, 8 managed by independent hosts and 1 by a small-scale host. Its median occupancy rate of 43.29% exceeds the 40% benchmark, **suggesting potential for market expansion** despite its limited inventory.

<table width="100%" style="table-layout: fixed; border-collapse: collapse;">
  <tr>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Neighborhoods 28806 and 28803 median occupancy rates differ substantially.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.3.png" width="100%">
    </td>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Hotel Room listings in Asheville are managed by mid-scale hosts.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.7.png" width="100%">
    </td>
  </tr>
</table>

<p align="center">
  <img
    src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.11.png"
    width="50%"
    style="border: 2px solid #808080; padding: 5px;"
  >
</p>

Hotel Room listings in neighborhoods 28806 and 28803 are both managed by two mid-scale hosts. However, their median occupancy rates differ substantially. Neighborhood 28806 has a median occupancy rate of 49.32%, exceeding the 40% benchmark by 9.32 percentage points, while neighborhood 28803 records only 1.52%, falling significantly below the target.

These findings suggest that **28806 is the more promising neighborhood for Hotel Room** investment based on occupancy performance, as its listings demonstrate substantially higher utilization despite a similar mid-scale host composition. 

<table width="100%" style="table-layout: fixed; border-collapse: collapse;">
  <tr>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Shared Room listings in neighborhood 28801 achieve highest median occupancy rate.</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.4.png" width="100%">
    </td>
    <td width="50%" align="center" valign="top" style="padding: 5px;">
      <strong>Neighborhood 28801 has two small-scale Shared Room hosts, while 28804 and 28806 each have three mid-scale hosts..</strong>
      <br><br>
      <img src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.8.png" width="100%">
    </td>
  </tr>
</table>

<p align="center">
  <img
    src="https://github.com/joshuabufi-analyst/Airbnb_Market_Expansion_Analysis/blob/main/photos/Q3.12.png"
    width="50%"
    style="border: 2px solid #808080; padding: 5px;"
  >
</p>

Shared Room listings in neighborhood 28801 are managed by two small-scale hosts and achieve 49.32% median occupancy, exceeding the 40% benchmark. In contrast, neighborhoods 28804 and 28806, each with three mid-scale hosts, record occupancy rates of only 1.92% and 2.19%, respectively.

**Neighborhood 28801 appears more promising for Shared Room investment** based on its stronger occupancy performance, although further analysis is needed to validate its revenue potential.

<h2 align="center" style="font-size: 40px;">
  Recommendations
</h2>
Based on the uncovered insights, here are actionable items that Airbnb can take away from our analysis.
