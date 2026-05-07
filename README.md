# Technographic Analysis Italy

Technographic market intelligence project focused on Italian B2B web technology signals.
This repository cleans, profiles, and visualizes a real technographic dataset to answer a practical question:

Which technologies are most visible in Italy, how fast are mentions changing over time, and what does infrastructure posture (behind firewall vs public-facing) look like?

## Executive Summary

The dataset contains 308 technology observations across 17 website domains and 236 unique technologies.
Results show a broad and fragmented stack distribution (high diversity, low concentration), with a late-period activity surge in August and September 2024.

Key outcomes:

- 82.14% of detected technologies are behind firewalls, indicating a strong enterprise/internal systems footprint.
- Observations increase from 115 in August to 129 in September (+12.17% month-over-month).
- The top 10 technologies account for only 17.53% of all observations, confirming a long-tail landscape rather than a winner-takes-all market.

## Project Storyline

This analysis follows a three-step narrative:

1. Data reliability and preparation
2. Pattern discovery (technology leaders and infrastructure posture)
3. Comparative trend interpretation (month-to-month movement and latest-period behavior)

The result is a business-oriented view of the Italian technographic environment, useful for market mapping, sales prioritization, and ecosystem monitoring.

## Verified Metrics (Real Project Values)

All values below are computed from `Cleaned_Technographic_Data_Italy.csv` in this repository.

### Dataset Scope

- Total records: 308
- Total columns: 11
- Unique technologies: 236
- Unique website domains: 17
- Time coverage (`Last Seen At`): 2024-06-06 to 2024-09-06
- Missing `Ticker` values after cleaning: 0

### Technology Concentration

Top technologies by frequency:

| Rank | Technology | Count | Share of Total |
|---|---|---:|---:|
| 1 | X-Content-Type-Options | 14 | 4.55% |
| 2 | HTML | 8 | 2.60% |
| 3 | Microsoft Intune | 6 | 1.95% |
| 4 | PyTorch | 6 | 1.95% |
| 5 | Prometheus | 4 | 1.30% |
| 6 | Spring Boot | 4 | 1.30% |
| 7 | SAP S/4HANA Finance | 3 | 0.97% |
| 8 | RabbitMQ | 3 | 0.97% |
| 9 | Spring Framework | 3 | 0.97% |
| 10 | DB2 | 3 | 0.97% |

Comparison insight:

- Top 1 technology share: 4.55%
- Combined Top 10 share: 17.53%

Interpretation: market technology presence is highly distributed, with many niche/low-frequency technologies contributing to the total profile.

### Infrastructure Posture (Firewall Comparison)

| Behind Firewall | Count | Share |
|---|---:|---:|
| True | 253 | 82.14% |
| False | 55 | 17.86% |

Interpretation: the dataset is strongly weighted toward enterprise or non-public deployment footprints.

### Time-Series Comparison (Installations / Mentions)

Monthly counts from `Last Seen At`:

| Month | Count |
|---|---:|
| 2024-06 | 38 |
| 2024-07 | 26 |
| 2024-08 | 115 |
| 2024-09 | 129 |

Comparative highlights:

- Minimum month: July 2024 (26)
- Maximum month: September 2024 (129)
- August to September change: +14 observations (+12.17%)
- June to July: contraction (-31.58%), followed by strong rebound in August (+342.31% vs July)

Interpretation: the trend suggests a late-period acceleration in observed technology signals, likely due to expanded visibility, monitoring coverage, or real adoption momentum.

### Latest Period Snapshot (September 2024)

- Total observations in latest month: 129
- Top technologies in latest month:
	- HTML (8)
	- PyTorch (6)
	- Prometheus (4)
	- RabbitMQ (3)
	- DB2 (3)

Interpretation: modern AI/ML and observability components (for example, PyTorch and Prometheus) appear alongside foundational web and enterprise stack technologies.

## Visual Outputs

Generated charts are saved in the `plots/` folder:

- `tech_mentions_over_time.png`
- `top_10_technologies.png`
- `behind_firewall_distribution.png`
- `trend_top_technology.png`
- `top_companies.png`

## Repository Structure

- `ItalyB2B.py`: data processing and visualization script
- `Cleaned_Technographic_Data_Italy.csv`: cleaned dataset used for analysis
- `plots/`: exported visualizations
- `README.md`: project documentation

## Methodology

The analysis workflow in `ItalyB2B.py` includes:

1. Loading and basic profiling of technographic data
2. Handling missing `Ticker` values
3. Datetime normalization for `First Seen At` and `Last Seen At`
4. Feature extraction (year/month)
5. Aggregation for trend and category comparisons
6. Visualization export for reporting

## Reproducibility

From the project root:

```bash
python -m pip install pandas matplotlib seaborn
python ItalyB2B.py
```

Note: `ItalyB2B.py` currently contains a local absolute input path for the raw source file. To run end-to-end on another machine, update `file_path` in the script to a valid local CSV path.

## Business Use Cases

- B2B sales and account prioritization based on tech stack signals
- Partner ecosystem and competitive intelligence mapping
- Security posture segmentation (public-facing vs internal technologies)
- Trend tracking for modern stack adoption in the Italian market

## License

This project is distributed under the terms defined in `LICENSE`.
