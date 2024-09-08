# Gopika_fods_assignment2
# insights obtained from each function output
1. Shape of the dataset (df.shape)
    Insight: The dataset contains 100 rows and 14 columns. This provides a quick overview of the dataset's size, indicating it's manageable for analysis and visualization.
2. Descriptive statistics (df.describe())
        Insight: This function offers a summary of numerical features:
Units Sold: The average units sold per transaction is 5,128, with a large range (from 1,000 to 9,925), indicating high variability in sales volumes.
Total Revenue: Revenue ranges significantly (from $4,870 to $5.99 million), showing that some sales are much larger than others.
Total Profit: The profit also varies widely, with a minimum of $1,258 and a maximum of $1.72 million, suggesting that certain products or regions are much more profitable.
3. Value counts (df['Region'].value_counts() and df['Item Type'].value_counts())
    Insight:
Regions: Sub-Saharan Africa is the dominant region in the dataset, contributing 36% of the transactions, followed by Europe. This reveals which regions are most frequently represented in the data, possibly indicating higher sales or market focus.
Item Type: Clothes, Cosmetics, and Office Supplies are the most sold items, suggesting they are key product lines for the business.
4. Correlation matrix (df.corr())
    Insight: The correlation matrix reveals relationships between numerical features:
Total Revenue correlates strongly with Units Sold and Unit Price, showing that both the number of units sold and the price per unit are critical factors driving revenue.
Total Profit correlates strongly with Total Revenue (0.90), indicating that revenue is a direct driver of profit.
5. Check for duplicate rows (df.duplicated().sum())
   Insight: There are no duplicate rows in the dataset. This confirms data integrity and suggests no cleaning is needed in terms of duplicate removal.
6. Converting date columns to datetime (pd.to_datetime())
    Insight: Converting the Order Date and Ship Date to datetime allows for easier date-based analysis, such as calculating shipping time, seasonal trends, or delays.
7. Unique values in categorical columns (df['Country'].nunique() and df['Item Type'].nunique())
   Insight:
 There are 76 unique countries and 12 different item types, indicating a diverse dataset both in terms of geographic coverage and product variety.
8. Grouping by Item Type and calculating total profit (df.groupby('Item Type')['Total Profit'].sum())
   Insight: The highest profit comes from Cosmetics (approx. $14.56 million), followed by Household products and Office Supplies, highlighting the most profitable product categories.
Fruits and Meat generate the least profit, suggesting lower demand or smaller margins for these items.
9. Total revenue by region (df.groupby('Region')['Total Revenue'].sum())
    Insight:
Sub-Saharan Africa is the leading region in terms of total revenue, generating $39.67 million, followed by Europe with $33.36 million.
North America generates the least revenue ($5.64 million), which may indicate less focus or smaller market size in that region.
10. Visualization insights:
Barplot for Total Profit by Item Type: Highlights Cosmetics as the most profitable item category, while Fruits and Meat lag in profitability.
Barplot for Total Revenue by Region: Shows that Sub-Saharan Africa and Europe are the largest contributors to revenue.
Distribution of Units Sold: Indicates that most transactions involve lower unit volumes, with a few large-volume outliers.
Boxplot for Total Profit: Displays outliers in total profit, where a few sales are significantly more profitable than the majority.
Correlation Heatmap: Visualizes strong relationships between revenue, profit, units sold, and unit price, reinforcing that higher-priced, high-volume sales lead to higher profitability.































