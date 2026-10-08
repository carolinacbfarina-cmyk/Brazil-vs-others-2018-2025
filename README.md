# Brazil vs. emerging peers: was it just the pandemic?

A common argument says Brazil's economic and social indicators got worse between 2019 and 2022 because of the pandemic. Every country went through the same pandemic, though. This project compares Brazil with 7 similar emerging economies to see how much of Brazil's performance the pandemic alone can explain.

## Approach

- **Peer group:** 8 middle-income emerging economies: Brazil, Mexico, Colombia, Peru, South Africa, Indonesia, Thailand and India. Turkey was in the first version and was replaced by Thailand, because its inflation above 70% a year distorted the comparison.
- **Periods:** 2018 → 2022 (pandemic, Bolsonaro government) and 2022 → 2025 (after the pandemic, Lula government).
- **Indicators:**
  - GDP growth and inflation, compounded over each period.
  - Unemployment, undernourishment and food insecurity, measured as the change from the base year to the worst year of each period, in percentage points ("people per 100"). Relative change is kept in the summary table for reference only, since it exaggerates changes in countries that start from low levels.
- **Ranking:** in each indicator, countries are ranked from best (1st) to worst.

## Data

All data comes from the [World Bank](https://data.worldbank.org) and is downloaded directly in the notebook with [`wbgapi`](https://pypi.org/project/wbgapi/).

| Indicator | Code |
|---|---|
| GDP growth (annual %) | [`NY.GDP.MKTP.KD.ZG`](https://data.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG) |
| Inflation, consumer prices (annual %) | [`FP.CPI.TOTL.ZG`](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG) |
| Unemployment (% of labor force, ILO estimate) | [`SL.UEM.TOTL.ZS`](https://data.worldbank.org/indicator/SL.UEM.TOTL.ZS) |
| Prevalence of undernourishment (% of population, UN Hunger Map) | [`SN.ITK.DEFC.ZS`](https://data.worldbank.org/indicator/SN.ITK.DEFC.ZS) |
| Moderate or severe food insecurity (% of population) | [`SN.ITK.MSFI.ZS`](https://data.worldbank.org/indicator/SN.ITK.MSFI.ZS) |

## Main results for Brazil

| Indicator | 2018 → 2022 | 2022 → 2025 |
|---|---|---|
| GDP growth (cumulative) | +5.7% (5th of 8) | +9.2% (3rd of 8) |
| Inflation (cumulative) | 26.7% (8th of 8) | 14.6% (6th of 8) |
| Unemployment (base → worst year) | 12.3% → 13.7% (5th of 8) | 9.2% → 7.9% (1st of 8) |
| Food insecurity (base → worst year) | 14.2% → 22.1% (7th of 7) | 18.4% → 13.5% (1st of 7) |

During the pandemic, Brazil had the highest inflation and the largest rise in food insecurity in the group. After it, Brazil ranked first in unemployment and food insecurity, and third in growth.

## Limitations

- This is a comparison between countries, so it shows relative performance and does not prove causes on its own.
- 2026 data is not available yet. Undernourishment and food insecurity are only available up to 2023.
- India has no food insecurity data. Undernourishment below 2.5% is published as 2.5, so changes from that floor may be understated.

## How to run

Open `brasil_vs_emergentes.ipynb` in Google Colab and run all cells. The notebook downloads the data, builds the summary table and saves the charts (rankings, before/after charts and a summary panel) as PNG files.
