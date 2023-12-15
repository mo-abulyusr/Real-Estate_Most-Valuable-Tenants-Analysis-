# Real Estate - Most Valuable Tenant Identification Project

# Business & Project Objective
The primary goal is to identify and understand the characteristics of the company's 'most valuable tenants'. 
This understanding is crucial for optimizing tenant retention strategies, enhancing marketing efforts, 
and driving strategic investments in property upgrades or expansions.

# Instructions
1. Define what a "valuable tenant" means.
2. Based on the definition of a "valuable" tenant, analyze the dataset to identify which factors make a tenant valuable.
3. Based on the factors that make a tenant "valuable," provide recommendations for possible actions from the findings.
4. Suggest additional features which could be strong predictors of a "valuable" tenant.

# Approach & Results
My primary objective was to identify the "most valuable tenants" to better understand and segment my renter population. Initially, I created a list of desired qualities that would define my ideal tenant. These characteristics included being a long-term tenant, paying market rate rent, showing a high level of care to the property, adhering to rules, utilizing low concessions, maintaining a high income to rent ratio, and choosing high safety properties.

Using the characteristics I had identified, I began sifting through the variables in the dataset. My goal was to either find existing variables that fulfilled these needs or to use the existing variables to create new ones that met these specific requirements.

To achieve my objective of identifying the 'most valuable tenants', I developed an index - a composite score designed to identify 'most valuable tenants' based on specific criteria that aligned with my definition of a valuable tenant. I formulated this index by aggregating the various tenant-related variables that I created, which I believed were indicative of a tenant's value. I constructed the index by penalizing qualities that didn't align with my values for a tenant and rewarding behaviors that I thought were valuable.

This index successfully identified 24,742 renters out of the 150,000 total in my dataset as 'most valuable tenants', which corresponded to approximately the top 85% percentile of my tenants based on their index scores. 

While I also experimented with a k-means clustering algorithm to find a distinct segment of my tenant population exhibiting behaviors aligned with my definition of a valuable tenant, this approach didn’t yield satisfactory results.

The index-based approach proved to be effective and robust enough to apply to both newer and older tenants.

# 1. Characteristics Of A Valuable Tenant
Based on my experience with renting, my growing interest in owning a multifamily home, and the extensive research I've conducted on the subject, coupled with stories I've heard from multifamily property owners, I've found that the most valuable tenants typically exhibit most of the following behaviors.

1. **Longterm Tenant**
   + Provides a steady stream of income and reduces turnover costs associated with finding new renters.
   + Tenants with longer lease terms are beneficial for these reasons.


2. **Pays Market Rate or Greater** 
    + Rent close to or above market rate avoids lost opportunity costs, particularly in high occupancy markets where finding a tenant is easier.


3. **High Level of Care to the Property** 
    + Minimal wear and tear or damages help in reducing maintenance and repair expenses.
    + Allowing pets can potentially increase property damage.
    + Older tenants are often more mature and likely to maintain cleanliness and avoid causing damages.
    + A higher number of occupants than beds can increase the probability of more damages to the property.


4. **Rule Adherence** 
    + Tenants who respect property rules and guidelines help in reducing conflicts within a living complex and ensure a harmonious environment.
    + A low complaint rate is indicative of tenants who rarely cause disturbances or receive complaints from neighbors.
    

5. **Low Concession Utilization**
    + Concessions are incentives for renting but can negatively impact profitability.


6. **High Income to Rent Ratio**
    + Tenants with a higher income to rent ratio are more likely to consistently pay rent on time.
    + This ratio is a good proxy for assessing the likelihood of timely rent payments.


7. **High Property Safety Index Choice**
    + Preference for properties with high safety indexes suggests that tenants are likely to be stable and community-oriented.


# 2. Descriptive Analysis & Data Transformation

I worked with 15 key variables in my dataset: MoveInDate, MoveOutDate, Rent, sub_asking_rent, County, SqFt, Beds, pet, primary_age_at_move_in, total_of_occupants, Concession, yearly_adjusted_income, INDUSTRY, and property_safety_index. These were crucial for my analysis.

Despite the potential for more extensive transformations and the creation of additional variables for a deeper analysis of my renters, time constraints have constrained my exploration. Nonetheless, the variables I've established are expected to be quite insightful. These include:

1. **tenure**: Reflecting the length of a tenant's stay.
2. **resident_status**: Distinguishing whether a tenant is current or a past renter.
3. **long_term_tenant**: Indicating tenants with extended lease periods.
4. **rent_market_comparison**: Comparing a tenant's rent payments to the market rate in their area.
5. **care_proxy_score**: A score designed to assess how well a tenant is likely to take care of the property.
6. **meaningful_concession_received**: Identifying whether a tenant has received significant rental concessions.
7. **income_rent_category**: The ratio of a tenant's income to their rent.
8. **property_safety_index**: Evaluating the safety levels of the properties selected by tenants.

The newly created variables will be instrumental in the next phase of identifying the 'most valuable tenants' population.

I recognize a significant opportunity to enhance the understanding of tenants by incorporating additional data sources, which would provide clearer insights than the approximate proxies I've been using.

If possible, stakeholders should consider incorporating additional variables that could further clarify my understanding of tenants. These might include the number of maintenance requests a tenant has made, the total cost incurred by a company due to a tenant's repairs or maintenance, the number of warnings a tenant has received from management, details on the timeliness and consistency of rent payments, credit scores, and the count of any infractions. Such data could significantly enhance my profiling of tenants and provide a more detailed picture.

# 3. Solution: Index

I started creating an index to help determine who my 'most valuable tenants' are, based on the variables I created. These variables serve as effective proxies for tenant behaviors that are critical to solving the problem at hand. This index is designed to systematically assess and score each tenant based on these key behaviors, allowing me to identify and understand the most valuable segments of my renter population.

The index I created has successfully identified 24,742 tenants as our 'most valuable tenants'. These tenants typically boast a higher income-to-rent ratio, suggesting they handle rent payments more effortlessly and have a lower likelihood of missing payments. They usually maintain their apartments well, evidenced by lower care_proxy_scores, which in turn keeps maintenance costs low. Often, these tenants pay rent that is close to market rates, maximizing company revenue and avoiding the opportunity cost associated with renting to long-term tenants at lower rates. Speaking of which, their tendency to be long-term tenants reduces expenses related to finding new tenants between leases. Living in properties with high safety index scores may reflect a more community-oriented mindset. Moreover, they receive fewer concessions, benefiting the company by maximizing potential revenue. A notable aspect is their annual income, which is nearly twice that of other renters, coupled with a tendency to be older. These characteristics impeccably match our definition of 'the most valuable tenants'.
