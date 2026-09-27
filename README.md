# Uber Trips Data Analysis

Exploratory Data Analysis on the NYC Uber Pickups dataset — univariate,
bivariate, multivariate, and temporal analysis of ride-hailing demand
patterns, with parallels to Uber, Ola, Rapido, and Lyft's real-world
demand-forecasting use case.

## Dataset

**Source:** [Uber Pickups in New York City](https://www.kaggle.com/datasets/fivethirtyeight/uber-pickups-in-new-york-city) (Kaggle, FiveThirtyEight)

1. Download `uber-raw-data-*.csv` (any month, or combine a few) from the link above.
2. Place the file(s) in the `data/` folder.
3. Or, if you have the Kaggle API set up:
   ```bash
   pip install kaggle
   kaggle datasets download -d fivethirtyeight/uber-pickups-in-new-york-city -p data --unzip
   ```

## Project structure

```
uber-trips-eda/
├── data/                       # raw CSVs go here (not committed — see .gitignore)
├── notebook/
│   └── uber_trips_eda.ipynb    # main analysis notebook
├── requirements.txt
└── README.md
```

## Analysis plan

1. **Load & clean** — parse `Date/Time` into a proper datetime, check for
   missing/duplicate rows.
2. **Univariate** — distribution of trips per day, per base/company.
3. **Bivariate** — trips vs. hour of day, trips vs. day of week.
4. **Multivariate** — hour × weekday × base, heatmaps of demand.
5. **Temporal** — rush-hour patterns, weekday vs. weekend trends, monthly
   seasonality if multiple months are combined.
6. **Insights** — 4-5 key findings written up at the end of the notebook,
   framed around what a company like Uber/Ola would do with them
   (surge pricing windows, driver allocation, etc.) — this is your viva
   talking track.

## Setup

```bash
pip install -r requirements.txt
jupyter notebook notebook/uber_trips_eda.ipynb
```
