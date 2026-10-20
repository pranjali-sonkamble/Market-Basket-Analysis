# Market Basket Analysis using Apriori

## Project Overview

This project analyzes grocery transaction data to identify products that are purchased together. Using Python and the Apriori algorithm, it discovers frequent itemsets and association rules that can inform cross-selling analysis and retail decision-making. A Power BI dashboard is used to visualize product popularity and frequent itemsets.

## Objectives

- Clean and prepare grocery item-level data.
- Group items into member-date transactions.
- Mine frequent itemsets using the Apriori algorithm.
- Evaluate association rules using support, confidence, and lift.
- Visualize product and itemset insights in Power BI.

## Technology Stack

- **Python**
- **Pandas** for data preparation
- **Apriori algorithm** for frequent itemset mining
- **Association rule metrics:** support, confidence, and lift
- **Microsoft Power BI** for visualization

## Dataset Preparation

The reported analysis used the following data-preparation figures:

| Metric | Result |
| --- | ---: |
| Raw grocery item records | 38,765 |
| Duplicate rows removed | 759 |
| Transactions after grouping by member and date | 14,963 |
| Minimum support threshold | 0.003 |

Duplicate item rows were removed, then items were grouped by member and date to form baskets for association rule mining.

## Methodology

1. **Load and clean data** — read the grocery dataset and remove duplicate rows.
2. **Construct transaction baskets** — group items by member and transaction date.
3. **Find frequent itemsets** — run Apriori with a minimum support threshold of 0.003.
4. **Generate association rules** — evaluate relationships between items using support, confidence, and lift.
5. **Visualize results** — explore product popularity and frequent itemsets in Power BI.

## Key Finding

The highest-lift rule reported in this analysis was **Bottled beer → Sausage**.

| Metric | Result |
| --- | ---: |
| Antecedent | Bottled beer |
| Consequent | Sausage |
| Lift | 1.222 |
| Confidence | 7.37% |
| Support | 0.334% |

A lift of 1.222 indicates a positive association: sausage appeared in baskets containing bottled beer at about 1.222 times its overall rate. However, the confidence of 7.37% is relatively low, so this is a modest association rather than a strong standalone recommendation. The rule can be used as a starting point for further cross-selling analysis.

## Power BI Dashboard

The Power BI dashboard is intended to show top-selling products and frequent-itemset insights.

Open the project’s `.pbix` file in **Power BI Desktop** to interact with the dashboard. Add dashboard screenshots to this README once they have been committed to the repository.

## Project Structure

The following is the intended repository layout. Add the project assets to these paths (or update this section to match their actual filenames):

```text
Market-Basket-Analysis/
├── README.md
├── main.py
├── groceries.csv
├── frequent_itemsets.csv
├── association_rules.csv
└── market basket.pbix
```

## How to Run

1. Install Python.
2. Place the source dataset at the path expected by `main.py`.
3. Install the dependencies used by the script. For example, if the implementation uses Pandas and `mlxtend`:

   ```bash
   pip install pandas mlxtend
   ```

4. Run the analysis:

   ```bash
   python main.py
   ```

5. Review the generated frequent itemsets and association rules.
6. Open the Power BI `.pbix` file in Power BI Desktop.

> **Note:** Confirm dependencies and file paths against `main.py` before running. The repository currently starts with this README; upload the Python script, dataset, generated CSV files, and Power BI file to make the project runnable from GitHub.

## Skills Demonstrated

- Data cleaning and preprocessing
- Transaction aggregation
- Exploratory data analysis
- Apriori frequent itemset mining
- Association rule evaluation and interpretation
- Support, confidence, and lift
- Power BI dashboarding
- Translating analytical results into business insights

## Conclusion

This project demonstrates how grocery transaction records can be transformed into product-association insights. The resulting itemsets, rules, and dashboard provide a foundation for understanding purchase patterns and investigating cross-selling opportunities.
