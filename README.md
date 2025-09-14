# Football Transfer Market Dataset from 2016 Winter td

## Overview
Comprehensive football transfer market dataset containing 19,454 player transfers from major European leagues and worldwide, covering **2016-2025** transfer windows. The dataset includes detailed transfer information with standardized player nationalities, positions, clubs, leagues, and transfer fees.

## File

| File | Records | Years | Description |
|------|---------|-------|-------------|
| `all_transfers_master_final.csv` | 19,454 | 2016-2025 | Complete cleaned transfer dataset with standardized data |

## Quick Start

### Load Data Directly from GitHub

```python
import pandas as pd

# Load the transfer dataset directly from GitHub
transfers = pd.read_csv('https://raw.githubusercontent.com/vibedatascience/guardiancouk_football_transfers_data/refs/heads/main/guardian_football_transfers.csv')

```

## Data Source

Data sourced from [Guardian.co.uk](https://www.theguardian.com/football/transfers) transfer windows coverage:

### Transfer Window Sources
- **2025 Summer**: https://interactive.guim.co.uk/2024/07/transfers/men-summer-2025.json
- **2024/25 Winter**: https://interactive.guim.co.uk/2024/07/transfers/men-winter-2025.json
- **2024 Summer**: https://interactive.guim.co.uk/2024/07/transfers/men-summer-2024.json
- **2023/24 Winter**: https://interactive.guim.co.uk/2024/tw-men-winter-2024/transfersData.json
- **2023 Summer**: https://interactive.guim.co.uk/2023/tw-men-summer-2023/transfersData.json
- **2022/23 Winter**: https://interactive.guim.co.uk/2023/tw-men-winter-2023/transfersData.json
- **2022 Summer**: https://interactive.guim.co.uk/2022/tw-men-summer-2022/transfersData.json
- **2021/22 Winter**: https://interactive.guim.co.uk/2021/09/tw-men-winter-2022/transfersData.json
- **2021 Summer**: https://interactive.guim.co.uk/docsdata/1stnMrwQdpXwNubJelzAZDmzw9QqJhHJJ1mrjs3Bt9hQ.json
- **2020/21 Winter**: https://interactive.guim.co.uk/docsdata/1V_SpJ8gg6OR_Jj_M-0Wz5AL93MdtMCcHMc1d5-aVbME.json
- **2020 Summer**: https://interactive.guim.co.uk/docsdata-test/1Qpc2Szu2fhjn5HbwpcsE70UdM_UgvlNmd4R4oLAdQfk.json
- **2019/20 Winter**: https://interactive.guim.co.uk/docsdata-test/1jhha-Gzxgh8fN2J1ZU8pRUMQZv6L0NKKaaJDLPtHqGo.json
- **2019 Summer**: https://interactive.guim.co.uk/docsdata/1N0tDYC5soeRrgpbZkDWkrws_zd-GKVq45ODlZzG-EH4.json
- **2018/19 Winter**: https://interactive.guim.co.uk/docsdata-test/1xMtQLF7dWQcH_iuDWjoRWsHRgxx4RkaK05KSAYpTCjI.json
- **2018 Summer**: https://interactive.guim.co.uk/docsdata-test/1OK4iKZwounIniO0ZOL-rp_Q5AkPmts4LK1gicT6JtyU.json
- **2017/18 Winter**: https://interactive.guim.co.uk/docsdata-test/17FTsDrP87t4b7si8XTYt_N35yH0kN4Z7GqonaXHuwRw.json
- **2017 Summer**: https://interactive.guim.co.uk/docsdata-test/1YJQzO5Ngc6LSydUaidGNKQi6Zi3Ipi-Q3E59-v2fjgc.json
- **2016/17 Winter**: https://interactive.guim.co.uk/docsdata/10WnObzhC6lF1Ho_T_1imgLY4d60_aJsuxHuUuBsjN9s.json

## Coverage Details

### Leagues
- **Premier League** - English top division
- **La Liga** - Spanish top division  
- **Bundesliga** - German top division
- **Serie A** - Italian top division
- **Ligue 1** - French top division
- **Other** - All other leagues worldwide (58% of transfers)

### Time Period
- **Years**: 2016-2025 (9 years of data)
- **Transfer Windows**: Summer and Winter windows included
- **Records**: 19,454 unique transfer records

## Data Dictionary

### Player Information

| Column | Type | Description | Null % | Top 6 Values |
|--------|------|-------------|--------|--------------|
| `Player_name` | str | Full name of the player | 0.0% | João Pedro (11), Matheus Cunha (10), Jota (9), Danilo (9), Sandro (9), Paulinho (8) |
| `Nationality` | str | ISO 3-letter country code | 22.4% | ENG (1,566), FRA (1,265), ESP (1,017), BRA (975), ITA (862), POR (745) |
| `Player_position` | str | Standardized position | 11.8% | Midfielder (5,851), Defender (5,507), Forward (4,251), Goalkeeper (1,329), Winger (219) |

### Transfer Details

| Column | Type | Description | Null % | Top 6 Values |
|--------|------|-------------|--------|--------------|
| `Transfer_type` | str | Type of transfer | 0.0% | fee (8,455), Free (6,016), Loan (3,982), undisclosed fee (1,000) |
| `Price_numeric` | float | Transfer fee in currency units | 74.3% | To find paid transfers, filter for `Transfer_type == 'fee'` and `Price_numeric.notna()` |
| `Transfer_date` | str | Date of transfer | 4.6% | Various dates in DD-MM-YYYY format |
| `Year` | int | Year of transfer | 4.6% | 2019 (3,677), 2023 (2,871), 2022 (2,869), 2024 (2,863), 2018 (2,090), 2020 (1,557) |
| `Transfer_Window` | str | Transfer window | 8.0% | Summer 2019 (3,677), Summer 2023 (2,871), Summer 2022 (2,869), Summer 2024 (2,863), Summer 2018 (2,090) |

### Club Information

| Column | Type | Description | Null % | Top 6 Values |
|--------|------|-------------|--------|--------------|
| `Prev_club` | str | Previous/selling club | 0.0% | Free agent (1,557), Chelsea (193), Barcelona (169), Juventus (161), Real Madrid (152), Manchester City (143) |
| `New_club` | str | New/buying club | 0.0% | Unattached (1,557), Juventus (176), Chelsea (172), Barcelona (163), Wolves (152), Fulham (149) |
| `Previous_club_league` | str | League of previous club | 0.0% | Other (6,179), Premier League (4,159), Serie A (3,162), Bundesliga (1,996), Ligue 1 (1,975), La Liga (1,954) |
| `New_club_league` | str | League of new club | 0.0% | Other (11,278), Serie A (2,172), Premier League (1,745), La Liga (1,524), Ligue 1 (1,378), Bundesliga (1,357) |

### Metadata

| Column | Type | Description | Null % |
|--------|------|-------------|--------|
| `Timestamp` | str | Record timestamp | 0.0% |
| `Transfer_date_parsed` | datetime | Parsed transfer date | 4.6% |


  
## Data Quality Notes

1. **Price Data**: 74.3% of transfers have no price (free transfers, loans, or undisclosed fees)
2. **Nationality**: 22.4% missing nationality data - **primarily from 2016, 2017 and 2018 where nationality wasn't recorded - so be careful when looking at nationality trends here**
3. **Position**: 11.8% missing position data
4. **Special Cases**: 
   - "Free agent" appears as a club for unattached players (1,557 records)
   - "Unattached" appears as destination for released players (1,557 records)
   - "Retired" appears for players ending careers (34 retirements recorded)
   - Some clubs appear in "Other" category if outside top 5 leagues



## Key Statistics

### League Distribution

**Previous Club League** (Where players came from):
- Other: 31.8%
- Premier League: 21.4%
- Serie A: 16.3%
- Bundesliga: 10.3%
- Ligue 1: 10.2%
- La Liga: 10.1%

**New Club League** (Where players went to):
- Other: 58.0%
- Serie A: 11.2%
- Premier League: 9.0%
- La Liga: 7.8%
- Ligue 1: 7.1%
- Bundesliga: 7.0%

### Transfer Types
- Free transfers and loans included
- 74.3% of transfers have no recorded fee (free, loan, or undisclosed)
- Fee-based transfers include numeric values where available

## Usage Examples

### Filter for Paid Transfers
```python
# Get only transfers with disclosed fees
paid_transfers = transfers[(transfers['Transfer_type'] == 'fee') & (transfers['Price_numeric'].notna())]

```

### Filter by League
```python
# Get all Premier League arrivals
pl_transfers = transfers[transfers['New_club_league'] == 'Premier League']

# Get transfers between top 5 leagues
top5 = ['Premier League', 'La Liga', 'Bundesliga', 'Serie A', 'Ligue 1']
top5_transfers = transfers[
    (transfers['Previous_club_league'].isin(top5)) & 
    (transfers['New_club_league'].isin(top5))
]
```

### Analyze Transfer Fees
```python
# Get paid transfers only
paid_transfers = transfers[transfers['Price_numeric'].notna()]

# Average transfer fee by destination league
avg_fees = paid_transfers.groupby('New_club_league')['Price_numeric'].mean()
```

### Track Player Movements
```python
# Get all transfers for a specific player
player_history = transfers[transfers['Player_name'] == 'Cristiano Ronaldo']

# Find most active clubs
most_buying = transfers['New_club'].value_counts().head(10)
most_selling = transfers['Prev_club'].value_counts().head(10)
```



## File Format

- **Format**: CSV (Comma-Separated Values)
- **Encoding**: UTF-8
- **Size**: ~19,454 records × 14 columns
- **No index column**: Data saved without pandas index
