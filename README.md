# Trading Behavior Analysis: Fear & Greed Index Impact

## Project Overview
This project analyzes the relationship between market sentiment (Fear & Greed Index) and trader behavior/performance in cryptocurrency markets. The analysis examines over 200,000 trades to identify actionable patterns and strategy recommendations.

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Installation

1. Clone or download this repository

2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Running the Analysis

**Option 1: Jupyter Notebook (Detailed Analysis)**

1. Ensure the following files are in the project directory:
   - `fear_greed_index.csv`
   - `historical_data.csv`
   - `analysis.ipynb`

2. Launch Jupyter Notebook:
```bash
jupyter notebook
```

3. Open `analysis.ipynb` and run all cells (Cell → Run All)

**Option 2: Streamlit Dashboard (Interactive Visualization)**

1. Run the Streamlit app:
```bash
streamlit run app.py
```

2. The dashboard will open in your browser automatically
3. Navigate through different sections using the sidebar

## Project Structure

```
.
├── README.md                          # This file
├── FINDINGS.md                        # Detailed analysis findings
├── analysis.ipynb                     # Main analysis notebook
├── fear_greed_index.csv              # Fear & Greed Index data
├── historical_data.csv               # Trading data
├── requirements.txt                  # Python dependencies
└── outputs/                          # Generated charts and data
    ├── performance_by_sentiment.png
    ├── behavior_by_sentiment.png
    ├── segment_analysis.png
    ├── correlation_heatmap.png
    ├── cumulative_pnl_timeline.png
    ├── segment_sentiment_performance.png
    ├── analysis_summary.csv
    ├── daily_metrics_processed.csv
    └── trader_segments.csv
```

## Analysis Components

### Part A: Data Preparation
- **Data Loading**: Loads and validates both datasets
- **Data Quality**: Documents missing values, duplicates, and data ranges
- **Timestamp Alignment**: Converts timestamps and aligns datasets by date
- **Metric Creation**:
  - Daily PnL per trader
  - Win rate
  - Average trade size
  - Leverage distribution
  - Number of trades per day
  - Long/short ratio
  - Drawdown proxy

### Part B: Analysis

#### 1. Performance Differences (Fear vs Greed)
Analyzes how trader performance varies across different market sentiment periods:
- Daily PnL comparison
- Win rate analysis
- Drawdown patterns
- Trade frequency changes

#### 2. Behavioral Changes
Examines how traders adjust their behavior based on sentiment:
- Trade frequency modifications
- Leverage adjustments
- Long/short bias shifts
- Position sizing changes

#### 3. Trader Segmentation
Identifies and analyzes three key trader segments:
- **High vs Low Leverage traders**
- **Frequent vs Infrequent traders**
- **Consistent Winners vs Inconsistent traders**

### Part C: Actionable Strategies
Provides data-driven strategy recommendations:
1. **Leverage Management Strategy**: When and how to adjust leverage based on sentiment
2. **Trade Frequency Strategy**: Optimal trading frequency for different market conditions

## Key Findings Summary

The analysis reveals:
1. **Sentiment Impact**: Clear performance differences between Fear and Greed periods
2. **Behavioral Adaptation**: Traders modify behavior based on market sentiment
3. **Segment Performance**: Different trader segments perform differently under various conditions
4. **Actionable Insights**: Specific recommendations for improving trading outcomes

For detailed findings, see `FINDINGS.md`.

## Output Files

### Charts
- `performance_by_sentiment.png`: PnL, win rate, drawdown, and trade count by sentiment
- `behavior_by_sentiment.png`: Trading behavior metrics across sentiment periods
- `segment_analysis.png`: Performance comparison across trader segments
- `correlation_heatmap.png`: Correlation between Fear/Greed index and trading metrics
- `cumulative_pnl_timeline.png`: Time series of cumulative PnL by sentiment
- `segment_sentiment_performance.png`: Combined segment and sentiment analysis

### Data Files
- `analysis_summary.csv`: High-level summary statistics
- `daily_metrics_processed.csv`: Daily metrics for all traders
- `trader_segments.csv`: Trader-level statistics and segment classifications

## Methodology

### Data Cleaning
- Timestamp conversion and standardization
- Date alignment between datasets
- Missing value handling
- Duplicate detection and removal

### Metric Calculation
- **Daily PnL**: Sum of closed PnL per trader per day
- **Win Rate**: Percentage of profitable trades
- **Leverage Proxy**: Position size relative to trader's average
- **Drawdown**: Decline from peak cumulative PnL
- **Long/Short Ratio**: Proportion of buy vs sell trades

### Statistical Analysis
- Descriptive statistics by sentiment groups
- Correlation analysis
- Segment comparison using median splits
- Time series analysis

## Reproducibility

All analysis steps are documented in the Jupyter notebook with:
- Clear code comments
- Intermediate outputs displayed
- Visualizations with proper labels
- Statistical summaries

To reproduce the analysis:
1. Follow setup instructions above
2. Run the notebook from start to finish
3. All outputs will be regenerated

## Requirements

See `requirements.txt` for exact package versions:
```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

## Contact & Questions

For questions about the analysis methodology or findings, please refer to the detailed documentation in `FINDINGS.md` or review the commented code in `analysis.ipynb`.

## License

This analysis is provided for evaluation purposes.
