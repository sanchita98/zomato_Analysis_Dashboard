🍽️ Zomato Data Analysis – Power BI Dashboard
📁 Project Overview
This Power BI project analyzes customer behavior, food preferences, restaurant performance, and sales trends using Zomato data. The dashboard is built to derive business insights like top-performing cities, weekly trends, user retention, and cuisine preferences through rich interactive visuals and DAX measures.

🧾 Dataset Description
The data model includes five interconnected tables:

food: Contains food category and cuisine details.

menu: Details about item types (veg/non-veg/others).

orders: Includes order date, user ID, and sales metrics.

restaurant: Holds restaurant ratings and locations.

users: Contains demographic data like age and gender.

These tables were cleaned and merged using relationships and joins inside Power BI's Model view.

![image](https://github.com/user-attachments/assets/b9e69f3e-28db-4d4e-8f11-ea289253bfca) 

📈 Dashboard Features & Visuals

 🌆 Top Performing Cities (Top N Sales)
Visual: Dynamic Bar Chart with Slicer

DAX Setup:
rank_table = DATATABLE("sort", INTEGER, "type", STRING, "NO", INTEGER, {
  {0, "Default", 0},
  {1, "TOP 5", 5},
  {2, "TOP10", 10},
  {3, "TOP20", 20},
  {4, "TOP50", 100}
})
Used in a slicer to filter top cities dynamically.

Insight: Tirupati and Baner-Pune dominate sales.

Action: Expand service coverage in high-performing cities.

Overview Dashboard Highlights
Section	Description
Sales Overview	Shows total Sales Amount (986.6M), Quantity (2.4M), Orders (150.3K), and Ratings (148.5K).
Yearly Sales Trend	Line chart showing sales growth in 2018–2019, then a drop in 2020.
Food Type Sales	Displays Veg (156.2K), Non-Veg (139.9K), and Other sales with ratings.
Top 10 Cities by Quantity	Interactive bar chart with dynamic Top N slicer (Top 5/10/20/50).
Weekly Order Pattern	Shows that Fridays and Saturdays are peak order days; Sunday is lowest.

💡 Key Insights
Veg Sales Lead: With 156.2K in quantity, veg items top food orders, confirming a strong vegetarian preference.

Electronic City dominates city-wise demand with 0.36M orders—3x more than the next best.

Sales peaked in 2019, reflecting strong platform momentum before a 2020 drop.

Fridays are most active, followed by Saturday. Sunday and Monday see a drop in engagement.

Other food category also shows notable sales with 14.2K and a high rating—signals niche interest.

🚀 Business Growth Suggestions
Capitalize on Veg Trends: Introduce more veg-focused combos or chef specials.

Geo-target Top Cities: Push exclusive offers in Electronic City, Old Gurgaon, and Gorakhpur to maintain momentum.

Mid-week Marketing Push: Create campaigns to boost orders on Sunday–Monday (e.g., “Lazy Sunday Meals” or “Monday Mood Busters”).

Promote High-Rating ‘Other’ Food Types: Use them to differentiate and attract niche audiences.

Expand in Growth Regions: Analyze upcoming cities from the Top 50 slicer and partner with local vendors.

🧑‍💼 User Analysis Dashboard

![image](https://github.com/user-attachments/assets/4583be63-a922-4e31-a369-0b6ea64ff519)

 🧑‍🤝‍🧑 User Demographics & Count
DAX:
user_count = DISTINCTCOUNT(users[user])
active_user = DISTINCTCOUNT(orders[user_id])

✨ Dashboard Highlights
Section	Description
Active Users	Displays total of 77.9K users currently active.
Rating Given	Over 148.5K total ratings submitted by users.
User Gains/Losses	11.6K gained customers and 33K lost users, broken down by gender.
Total Orders	300.6K orders by 100K total users.
Users by Age	Majority of users are aged 20–30, with a spike at age 22 (18.8K).

💡 Key Insights
Retention Challenge: A net loss of over 21.4K users, especially males (18.9K lost).

Peak Engagement: Age 22 is the most engaged, followed by 21 and 23.

User Base: A large chunk of users are in their 20s, indicating a young, mobile-driven audience.

Ratings per User: With 148.5K ratings and 100K users, users show high engagement post-order.

🚀 Recommendations for Growth
Retention Campaigns for Male Users

Design email/push notifications targeting male churn segment.

Offer “Welcome Back” discounts and loyalty rewards.

Age-Specific Promotions

Tailor offers to ages 20–25, using trendy food combos, student discounts, or wallet cashback.

Referral Programs

Encourage highly active young users (ages 21–23) to refer friends.

Reward with coupons or free delivery.

Surveys & Feedback Collection

Ask users who stop ordering why (especially males).

Use feedback loops to improve app flow or pricing perception.

Push Notifications Based on Ratings

Encourage repeat orders by using previous high ratings to recommend new restaurants.

![image](https://github.com/user-attachments/assets/06816b39-1bac-4d19-9244-3622df8b5120)


🌍 City Performance Dashboard

✨ Dashboard Highlights
Section	Description
Top Restaurants by Rating	Domino’s (442), Pizza Hut (322), and KFC (309) lead in customer reviews.
Sales by City	Cities like Tirupati, Electronic City, and Baner-Pune top in revenue.
Rating by City	Bikaner, Noida-1, and Indirapuram show the most feedback from users.
User by City	Highest user concentration in Bikaner, BTM-Bangalore, and Indiranagar.
City-Wise Breakdown Table	Shows total sales, lost users, gained users, and orders across major cities.

💡 Key Insights
Domino’s Pizza is the most rated restaurant with over 440+ reviews.

Tirupati leads sales with ₹43M+, followed by Electronic City and Baner-Pune.

Bikaner has high user count (1.7K) but relatively low order volume, indicating under-conversion.

BTM and Indiranagar (Bangalore) are highly engaged in both user count and feedback.

Some cities like GOTA and Sirsa show very low order numbers despite notable user base.

🚀 Business Growth Recommendations
Target Underperforming High-User Cities

Cities like Bikaner and GOTA have a large user base but low order rates.

Use localized offers, restaurant onboarding, and geo-specific discounts.

Leverage High-Rated Chains

Partner further with Domino’s, Pizza Hut, and KFC to create loyalty programs.

Use their success in one city as a playbook for others.

Boost Activity in Silent Cities

Cities with high drop-off (e.g., Sirsa, Malviya Nagar) need retention focus.

Run “We miss you!” campaigns or re-engagement ads.

Replicate Success from Tirupati

Identify what works in Tirupati—delivery model, restaurants, pricing—and apply to cities with similar demographics.

Gather City-Specific Feedback

For cities with high losses (e.g., Rohini, Delhi), send short surveys post uninstalls or inactive periods to understand friction points.


