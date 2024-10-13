<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>AirBnb Trends Analysis</h1>

<h2>Overview</h2>
<p>This study analyzes Airbnb listings in New York City, utilizing a dataset of 102,600 properties.</p>

<h2>Introduction</h2>
<p>Since its inception in 2008, Airbnb has transformed the travel landscape. This report focuses on New York City, where Airbnb has significantly impacted urban travel.</p>

<h3>Analysis includes:</h3>
<ul>
    <li>Data Preprocessing and Feature Engineering: Enhancing dataset quality for analysis.</li>
    <li>Exploratory Data Analysis (EDA): Identifying patterns in Airbnb offerings.</li>
    <li>Statistical Testing: Exploring relationships between location, price, and guest satisfaction.</li>
    <li>Data Visualization: Creating plots to illustrate trends.</li>
    <li>Dimensionality Reduction: Using Principal Component Analysis (PCA) for focused analysis.</li>
    <li>Outlier Detection: Ensuring data validity by identifying anomalies.</li>
    <li>Interactive Dashboard Creation: Building a Dash framework tool for real-time exploration.</li>
</ul>

<p>This report aims to connect Airbnb's operational data with New York City's economic and cultural context.</p>

<h2>Dataset Description</h2>
<p>This dataset, designed for exploring Airbnb listings in New York City, consists of 102,600 entries, each representing a unique accommodation. It includes both numerical variables, such as 'id', 'host_id', 'price', and 'number of reviews', which provide insight into listing popularity and pricing strategies, and categorical variables like 'neighbourhood group', 'instant_bookable', and 'room type', which help understand market segmentation and regulatory aspects.</p>

<p>Key dependent variables are 'price' and 'number of reviews', influenced by independent variables such as 'room type' and 'neighbourhood group'. Understanding these interactions is crucial for optimizing pricing, enhancing customer satisfaction, and aligning supply with demand in New York City's competitive hospitality landscape. This dataset serves as a valuable resource for businesses and policymakers alike, enabling deeper insights into Airbnb's impact on travel and urban economics.</p>

<h2>Data Cleaning and Feature Engineering</h2>
<p>The data cleaning process was meticulously conducted to ensure the dataset's integrity and readiness for analysis. Key steps included:</p>
<ul>
    <li>Addressing and removing null values to safeguard the dataset.</li>
    <li>Eliminating irrelevant columns such as 'license' and 'house_rules'.</li>
    <li>Removing duplicate records to maintain accuracy.</li>
    <li>Renaming columns for uniformity, converting to lowercase, and replacing spaces with underscores.</li>
    <li>Cleaning financial columns ('price' and 'service_fee') by removing non-numeric characters.</li>
</ul>

<p>Feature engineering introduced new metrics for deeper insights, including:</p>
<ul>
    <li>Converting 'last_review' to datetime format for temporal analysis.</li>
    <li>Calculating 'Monthly Revenue', 'Occupancy Rate', and 'Average Daily Rate (ADR)'.</li>
    <li>Creating 'Review Impact Score' and 'Seasonal Booking' categories.</li>
    <li>Developing metrics like 'Host Efficiency' and 'Host Activity Score' to assess host performance.</li>
    <li>Normalizing review data and creating a composite 'Performance Score' for holistic analysis.</li>
</ul>

<h2>Data Analysis and Testing</h2>
<p>The analysis involved several key steps to ensure data integrity and extract meaningful insights. Outlier detection was conducted on critical columns like "reviews per month" and "availability 365," identifying and removing extreme values to refine the dataset. This step was crucial for accurate representation and analysis. Principal Component Analysis (PCA) was then performed to reduce dimensionality, improving interpretability and maintaining 97% of the dataset's variance while addressing multicollinearity.</p>

<p>Additionally, normality tests using the Kolmogorov-Smirnov and D'Agostino's K-squared tests revealed that the "days_booked" feature significantly deviates from normal distribution, indicating potential challenges for parametric statistical methods. The Pearson correlation coefficient analysis further highlighted relationships among key metrics:</p>
<ul>
    <li>Strong positive correlation (0.94) between listing popularity and reviews count.</li>
    <li>Weak correlation (0.11) between listing popularity and occupancy rate.</li>
    <li>Moderate correlation (0.66) between occupancy rate and performance score.</li>
</ul>

<h2>Statistics</h2>
<p>The Kernel Density Estimate (KDE) analysis visualizes the distribution of key variables from the Airbnb dataset, including Host Activity Score, occupancy rate, number of reviews, and listing popularity. Key observations include:</p>
<ul>
    <li>Host Activity Score: Wide distribution with a mean of 23.96, indicating many hosts are less active, while a few are highly engaged (scores up to 1660).</li>
    <li>Occupancy Rate: Mean of 4.72, suggesting most listings have low occupancy, with extreme values indicating possible overbooking.</li>
    <li>Number of Reviews: Average of 32.28, with a positive skew and some listings receiving up to 1024 reviews.</li>
    <li>Listing Popularity: Mean of 2.54, again skewed towards lower values but with notable outliers.</li>
</ul>

<p>Descriptive statistics further reveal insights into the dataset's variables, such as an average price of $626, with a standard deviation of $331 indicating significant variability. Monthly revenue averages around $8,875, highlighting the wide performance range among listings. Metrics like review impact score and host efficiency also show high variability, indicating potential outliers and diverse host engagement levels.</p>

<h2>Data Visualizations</h2>

<p>This document summarizes the various data visualizations created to analyze Airbnb listings, focusing on trends in occupancy rates, review distributions, pricing, and more.</p>

<h2>1. Area Plot</h2>
<p><strong>Description</strong>: The area plot illustrates the average occupancy rate for Airbnb listings across different seasons. The y-axis indicates the occupancy rate, while the x-axis represents the four seasons.</p>
<ul>
    <li>Winter has the highest average occupancy rate (just over 5), likely due to the holiday season.</li>
    <li>Spring sees a slight decline to around 4.4, reflecting reduced travel.</li>
    <li>Summer's average rate is close to 4.9, marking the peak travel season.</li>
    <li>Autumn shows the lowest occupancy rate at approximately 4.1.</li>
</ul>

<h2>2. Violin Plot</h2>
<p><strong>Description</strong>: The violin plot visualizes the distribution of review rates across different room types, highlighting density at various values.</p>
<ul>
    <li>All room types show review rates between 1 and 5, with medians around 3.</li>
    <li>Shared rooms have the highest average review rate (3.30), followed by hotel rooms (3.54).</li>
    <li>The consistency in median values across room types indicates a similar pattern of guest satisfaction.</li>
</ul>

<h2>3. Joint Plot with KDE and Scatter Representation</h2>
<p><strong>Description</strong>: This plot combines a scatter plot and kernel density estimates (KDE) to explore the relationship between listing popularity and host response rate.</p>
<ul>
    <li>The average host response rate is approximately 75.33%, while listing popularity averages around 2.59.</li>
    <li>The standard deviation for response rates is higher, indicating more variation compared to listing popularity.</li>
</ul>

<h2>4. Rug Plot</h2>
<p><strong>Description</strong>: A rug plot displays the distribution of the Review Impact Score across listings using marks along an axis.</p>
<ul>
    <li>There is significant clustering near the origin, suggesting many listings have a low Review Impact Score.</li>
    <li>The distribution is right-skewed, indicating most listings do not have substantial review impact, with some outliers achieving high scores.</li>
</ul>

<h2>5. 3D Plot</h2>
<p><strong>Description</strong>: This 3D plot analyzes Airbnb prices in relation to host activity scores and the number of reviews.</p>
<ul>
    <li>There is a wide dispersion of prices across host activity scores.</li>
    <li>Higher host activity and review counts do not consistently correspond to higher prices.</li>
</ul>

<h2>6. Contour Plot</h2>
<p><strong>Description</strong>: The contour plot visualizes data density in a 3D space, showing Gaussian Kernel Density Estimates across price and number of reviews.</p>
<ul>
    <li>More affordable listings tend to have a consistent number of reviews.</li>
    <li>Higher-priced listings are less common and receive reviews less consistently.</li>
</ul>

<h2>7. Cluster Map</h2>
<p><strong>Description</strong>: A cluster map visualizes correlations between various metrics, using a heatmap combined with hierarchical clustering.</p>
<ul>
    <li>Monthly revenue shows a strong positive correlation with performance score (0.52).</li>
    <li>Occupancy rate correlates positively with monthly revenue (0.79).</li>
    <li>The host activity score shows little correlation with other metrics.</li>
</ul>

<h2>8. Hexbin Plot</h2>
<p><strong>Description</strong>: The hexbin plot depicts the relationship between price and review density using hexagonally-shaped bins.</p>
<ul>
    <li>Most data concentrates around the lower to mid-price range with moderate review densities.</li>
    <li>Isolated hexagons with warmer colors indicate outliers at certain price points.</li>
</ul>

<h2>9. Strip Plot</h2>
<p><strong>Description</strong>: The strip plot displays price distributions for different room types, differentiating based on host verification status.</p>
<ul>
    <li>Private rooms and entire homes/apartments are the most common.</li>
    <li>Verified and unverified hosts show similar price distributions across room types.</li>
</ul>

<h2>10. Swarm Plot</h2>
<p><strong>Description</strong>: The swarm plot organizes individual data points to show price distribution within each room category.</p>
<ul>
    <li>Entire homes and private rooms show a broad price range with a high concentration around the median.</li>
    <li>Shared rooms and hotel rooms have less price variation.</li>
</ul>

<h2>Subplots</h2>

<h3>11. Airbnb Pricing Trends Over Two Decades</h3>
<p><strong>Description</strong>: This line graph presents average pricing changes for Airbnb listings over several years.</p>
<ul>
    <li>Prices show notable fluctuations with significant peaks and valleys, indicating a volatile market.</li>
</ul>

<h3>12. Trend Analysis</h3>
<p><strong>Description</strong>: This subplot focuses on host efficiency by neighborhood and the evolution of review impact scores over time.</p>
<ul>
    <li>Manhattan hosts exhibit the highest efficiency.</li>
    <li>Review impact scores have generally increased, highlighting the growing importance of guest feedback.</li>
</ul>

<h3>13. Booking Features Distribution</h3>
<p><strong>Description</strong>: This subplot shows variances in booking preferences across different dimensions.</p>
<ul>
    <li>Summer bookings dominate, while instant bookable listings and cancellation policies are evenly distributed.</li>
</ul>

<h3>14. Neighborhood Group Dynamics</h3>
<p><strong>Description</strong>: The boxen plot provides a detailed view of Airbnb pricing across different neighborhood groups.</p>
<ul>
    <li>Certain neighborhoods, like Manhattan, have higher median prices and a broader price range, while the Bronx shows less variability.</li>
</ul>



</body>
</html>
