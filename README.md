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



</body>
</html>
