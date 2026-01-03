
<body>

<h1>Airbnb Listings Analysis</h1>
<h3>Identifying Demand Drivers Beyond Price & Availability</h3>

<p>
This project analyzes Airbnb listing data to understand why certain listings
underperform despite having competitive prices and high ratings.
Rather than treating availability as a proxy for demand, the analysis focuses
on <strong>host behavior, booking constraints, and stay flexibility</strong>.
</p>

<hr>

<h2>Why This Project Matters</h2>

<p>
In many marketplace analyses, availability is incorrectly assumed to represent
demand. This project challenges that assumption and demonstrates that
<strong>host-controlled restrictions</strong> particularly minimum-night policies
and calendar blocking are major contributors to low booking performance.
</p>

<div class="highlight">
<strong>Key takeaway:</strong> Listings often underperform not because guests dislike them,
but because guests cannot book them.
</div>

<hr>

<h2>Business Questions Answered</h2>
<ul>
    <li>Is <code>availability_365</code> a reliable indicator of demand?</li>
    <li>Why do Brooklyn listings outperform Manhattan despite similar supply?</li>
    <li>How do minimum-night restrictions affect review volume?</li>
    <li>Are low-review listings driven by poor guest experience?</li>
</ul>

<hr>

<h2>Dataset Overview</h2>
<ul>
    <li>Multi-city Airbnb listings dataset (5 city groups)</li>
    <li>Each row represents a unique listing</li>
    <li>Host-level analysis using <code>host_id</code></li>
</ul>

<hr>

<h2>Project Workflow</h2>

<h3>1. Data Loading & Preparation</h3>
<ul>
    <li>Removed duplicate listings</li>
    <li>Handled missing values and invalid entries</li>
    <li>Corrected data types for numerical analysis</li>
    <li>Staged cleaned data for analysis</li>
</ul>

<h3>2. Data Cleaning & Feature Engineering</h3>
<ul>
    <li>Converted rating fields from string to float</li>
    <li>Flagged studio listings</li>
    <li>Created <strong>price per bedroom</strong> feature</li>
    <li>Handled extreme price outliers (capped at $1500)</li>
    <li>Derived stay categories from minimum-night rules</li>
</ul>

<h3>3. Exploratory Data Analysis (EDA)</h3>
<ul>
    <li>Host categorization (Casual, Small Business, Professional, Large Business)</li>
    <li>Availability vs price analysis</li>
    <li>Correlation checks and heatmaps</li>
    <li>Demand segmentation using reviews in the last 12 months</li>
</ul>

<hr>

<h2>Key Findings</h2>

<h3>1. Availability Is Not Demand</h3>
<ul>
    <li>No meaningful correlation between availability and price</li>
    <li>No meaningful correlation between availability and reviews</li>
    <li>Many listings with zero availability showed no recent activity</li>
</ul>

<div class="highlight">
<strong>Conclusion:</strong> Availability reflects host behavior more than guest demand.
</div>

<h3>2. Host Behavior Drives Underperformance</h3>
<ul>
    <li>Casual hosts make up ~60% of the dataset</li>
    <li>Casual hosts are more likely to block calendars</li>
    <li>81% of listings require monthly stays</li>
</ul>

<h3>3. Low Demand ≠ Poor Guest Experience</h3>
<ul>
    <li>Ratings are heavily skewed toward high scores</li>
    <li>Low-review listings are not low-rated</li>
    <li>Performance issues stem from accessibility, not quality</li>
</ul>

<hr>

<h2>Manhattan vs Brooklyn Analysis</h2>

<table class="table">
    <tr>
        <th>Metric</th>
        <th>Manhattan</th>
        <th>Brooklyn</th>
    </tr>
    <tr>
        <td>Supply</td>
        <td>High</td>
        <td>High</td>
    </tr>
    <tr>
        <td>High-review listings</td>
        <td>Lower</td>
        <td>Higher</td>
    </tr>
    <tr>
        <td>Weekend stay presence</td>
        <td>Lower</td>
        <td>Higher</td>
    </tr>
</table>

<p>
Despite similar supply, Brooklyn listings appear more frequently in the
high-demand group due to greater flexibility in minimum-night policies.
</p>

<hr>

<h2>Quantified Impact</h2>
<ul>
    <li><strong>~55%</strong> of Manhattan listings show signs of underperformance</li>
    <li><strong>~38%</strong> underperform due to restrictive minimum-night rules</li>
    <li><strong>~36%</strong> of Brooklyn listings show similar demand loss</li>
</ul>

<hr>

<h2>Recommendations</h2>

<h3>For Hosts</h3>
<ul>
    <li>Allow stays ≤ 7 nights to increase demand</li>
    <li>Open calendars at least on weekends</li>
    <li>High ratings alone do not guarantee bookings</li>
</ul>

<h3>For Platforms</h3>
<ul>
    <li>Do not treat availability as a demand metric</li>
    <li>Identify and flag inactive listings separately</li>
    <li>Educate hosts on the cost of restrictive booking rules</li>
</ul>

<hr>

<h2>Tools & Skills Demonstrated</h2>
<ul>
    <li>Python (Pandas, NumPy)</li>
    <li>Visualizations using Python (Matplotlib, Seaborn, Plotly Express) </li>
    <li>Data cleaning & feature engineering</li>
    <li>Exploratory Data Analysis (EDA)</li>
    <li>Marketplace & behavioral analytics</li>
    <li>Business-focused data storytelling</li>
</ul>

<hr>

<div class="footer">
<p>
This project demonstrates the ability to go beyond surface-level metrics,
challenge assumptions, and translate data into actionable business insights.
</p>
</div>

</body>
</html>
