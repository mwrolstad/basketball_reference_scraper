# Baseball-Reference Scraper
## br_scraper

An easy tool to scrape the game and preview data from baseball-reference.com

* Simply provide the date variables to get game stats and data
  * `year`
  * `month`
  * `year`
* Otherwise provide no date info to get the game previews for that day

### Use as a command line:

```cmd
python3 src/pfr_scraper/__init__.py --year 2022 --month 11 --day 5
```

### Build package and import:

```cmd
pip install poetry
poetry build 
pip install dist/br_scraper-0.1.1.tar.gz
```

Once the pacakge is install locally, you can now run this script:

```python
from br_scraper import GameScraper
import json
game_scraper = GameScraper()
stats = game_scraper.scrape_day(year=2022, month=11, day=5)
print(json.dumps(stats[0], indent=2))
{
  "game_date": "20221105",
  "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
  "away_team": "Philadelphia Phillies",
  "home_team": "Philadelphia Phillies",
  "away_abrv": "PHI",
  "home_abrv": "PHI",
  "pitcher_stats": [
    {
      "Pitching": "Zack Wheeler",
      "IP": 5.1,
      "H": 3,
      "R": 2,
      "ER": 2,
      "BB": 1,
      "SO": 5,
      "HR": 0,
      "ERA": 2.78,
      "BF": 20,
      "Pit": 70,
      "Str": 49,
      "Ctct": 29,
      "StS": 7,
      "StL": 13,
      "GB": 9,
      "FB": 4,
      "LD": 2,
      "Unk": 0,
      "GSc": 58.0,
      "IR": NaN,
      "IS": NaN,
      "WPA": 0.154,
      "aLI": 1.21,
      "cWPA": 5.87,
      "acLI": 93.41,
      "RE24": 1.7,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Pitching": "Jose Alvarado",
      "IP": 0.1,
      "H": 1,
      "R": 2,
      "ER": 2,
      "BB": 1,
      "SO": 1,
      "HR": 1,
      "ERA": 5.56,
      "BF": 3,
      "Pit": 18,
      "Str": 9,
      "Ctct": 7,
      "StS": 1,
      "StL": 1,
      "GB": 0,
      "FB": 1,
      "LD": 0,
      "Unk": 0,
      "GSc": NaN,
      "IR": 2.0,
      "IS": 2.0,
      "WPA": -0.339,
      "aLI": 1.27,
      "cWPA": -14.63,
      "acLI": 98.33,
      "RE24": -2.1,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Pitching": "Seranthony Dominguez",
      "IP": 0.1,
      "H": 1,
      "R": 0,
      "ER": 0,
      "BB": 0,
      "SO": 0,
      "HR": 0,
      "ERA": 1.69,
      "BF": 2,
      "Pit": 9,
      "Str": 6,
      "Ctct": 3,
      "StS": 3,
      "StL": 0,
      "GB": 1,
      "FB": 1,
      "LD": 1,
      "Unk": 0,
      "GSc": NaN,
      "IR": 1.0,
      "IS": 1.0,
      "WPA": -0.057,
      "aLI": 0.49,
      "cWPA": -2.45,
      "acLI": 37.94,
      "RE24": -0.7,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Pitching": "Zach Eflin",
      "IP": 1.0,
      "H": 1,
      "R": 0,
      "ER": 0,
      "BB": 0,
      "SO": 2,
      "HR": 0,
      "ERA": 3.38,
      "BF": 4,
      "Pit": 18,
      "Str": 13,
      "Ctct": 6,
      "StS": 5,
      "StL": 2,
      "GB": 0,
      "FB": 2,
      "LD": 1,
      "Unk": 0,
      "GSc": NaN,
      "IR": 0.0,
      "IS": 0.0,
      "WPA": 0.011,
      "aLI": 0.2,
      "cWPA": 0.49,
      "acLI": 15.1,
      "RE24": 0.5,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Pitching": "David Robertson",
      "IP": 1.0,
      "H": 1,
      "R": 0,
      "ER": 0,
      "BB": 0,
      "SO": 1,
      "HR": 0,
      "ERA": 1.17,
      "BF": 3,
      "Pit": 15,
      "Str": 10,
      "Ctct": 7,
      "StS": 2,
      "StL": 1,
      "GB": 0,
      "FB": 2,
      "LD": 1,
      "Unk": 0,
      "GSc": NaN,
      "IR": 0.0,
      "IS": 0.0,
      "WPA": 0.006,
      "aLI": 0.05,
      "cWPA": 0.25,
      "acLI": 3.87,
      "RE24": 0.5,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Pitching": "Framber Valdez",
      "IP": 6,
      "H": 2,
      "R": 1,
      "ER": 1,
      "BB": 2,
      "SO": 9,
      "HR": 1,
      "ERA": 1.44,
      "BF": 22,
      "Pit": 93,
      "Str": 57,
      "Ctct": 30,
      "StS": 6,
      "StL": 21,
      "GB": 6,
      "FB": 4,
      "LD": 2,
      "Unk": 0,
      "GSc": 71.0,
      "IR": NaN,
      "IS": NaN,
      "WPA": 0.16,
      "aLI": 0.89,
      "cWPA": 6.14,
      "acLI": 68.66,
      "RE24": 1.9,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Pitching": "Hector Neris",
      "IP": 1,
      "H": 0,
      "R": 0,
      "ER": 0,
      "BB": 0,
      "SO": 2,
      "HR": 0,
      "ERA": 1.5,
      "BF": 3,
      "Pit": 10,
      "Str": 9,
      "Ctct": 3,
      "StS": 4,
      "StL": 2,
      "GB": 0,
      "FB": 1,
      "LD": 0,
      "Unk": 0,
      "GSc": NaN,
      "IR": 0.0,
      "IS": 0.0,
      "WPA": 0.044,
      "aLI": 0.59,
      "cWPA": 1.9,
      "acLI": 45.42,
      "RE24": 0.5,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Pitching": "Bryan Abreu",
      "IP": 1,
      "H": 0,
      "R": 0,
      "ER": 0,
      "BB": 0,
      "SO": 1,
      "HR": 0,
      "ERA": 0.0,
      "BF": 3,
      "Pit": 10,
      "Str": 7,
      "Ctct": 4,
      "StS": 1,
      "StL": 2,
      "GB": 0,
      "FB": 2,
      "LD": 1,
      "Unk": 0,
      "GSc": NaN,
      "IR": 0.0,
      "IS": 0.0,
      "WPA": 0.04,
      "aLI": 0.53,
      "cWPA": 1.73,
      "acLI": 41.04,
      "RE24": 0.5,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Pitching": "Ryan Pressly",
      "IP": 1,
      "H": 1,
      "R": 0,
      "ER": 0,
      "BB": 0,
      "SO": 0,
      "HR": 0,
      "ERA": 0.0,
      "BF": 4,
      "Pit": 7,
      "Str": 6,
      "Ctct": 6,
      "StS": 0,
      "StL": 0,
      "GB": 0,
      "FB": 4,
      "LD": 1,
      "Unk": 0,
      "GSc": NaN,
      "IR": 0.0,
      "IS": 0.0,
      "WPA": 0.031,
      "aLI": 0.59,
      "cWPA": 1.34,
      "acLI": 46.07,
      "RE24": 0.5,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    }
  ],
  "hitter_stats": [
    {
      "Batting": "Kyle Schwarber",
      "AB": 3.0,
      "R": 1.0,
      "H": 1.0,
      "RBI": 1.0,
      "BB": 1.0,
      "SO": 2.0,
      "PA": 4.0,
      "BA": 0.218,
      "OBP": 0.392,
      "SLG": 0.545,
      "OPS": 0.937,
      "Pit": 20.0,
      "Str": 11.0,
      "WPA": 0.173,
      "aLI": 0.86,
      "WPA+": 0.204,
      "WPA-": -0.031,
      "cWPA": 8.8,
      "acLI": 66.58,
      "RE24": 1.1,
      "PO": 3.0,
      "A": 1.0,
      "Details": "HR",
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Rhys Hoskins",
      "AB": 4.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 4.0,
      "BA": 0.159,
      "OBP": 0.205,
      "SLG": 0.435,
      "OPS": 0.64,
      "Pit": 15.0,
      "Str": 9.0,
      "WPA": -0.132,
      "aLI": 0.96,
      "WPA+": 0.0,
      "WPA-": -0.132,
      "cWPA": -6.1,
      "acLI": 74.33,
      "RE24": -1.4,
      "PO": 7.0,
      "A": 0.0,
      "Details": "GDP",
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "J.T. Realmuto",
      "AB": 3.0,
      "R": 0.0,
      "H": 1.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 4.0,
      "BA": 0.215,
      "OBP": 0.292,
      "SLG": 0.369,
      "OPS": 0.661,
      "Pit": 13.0,
      "Str": 8.0,
      "WPA": 0.004,
      "aLI": 0.48,
      "WPA+": 0.033,
      "WPA-": -0.029,
      "cWPA": 0.07,
      "acLI": 37.55,
      "RE24": 0.1,
      "PO": 9.0,
      "A": 0.0,
      "Details": "HBP",
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Bryce Harper",
      "AB": 4.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 2.0,
      "PA": 4.0,
      "BA": 0.349,
      "OBP": 0.414,
      "SLG": 0.746,
      "OPS": 1.16,
      "Pit": 11.0,
      "Str": 8.0,
      "WPA": -0.084,
      "aLI": 0.81,
      "WPA+": 0.0,
      "WPA-": -0.084,
      "cWPA": -3.69,
      "acLI": 62.91,
      "RE24": -0.8,
      "PO": NaN,
      "A": NaN,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Nick Castellanos",
      "AB": 4.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 2.0,
      "PA": 4.0,
      "BA": 0.185,
      "OBP": 0.232,
      "SLG": 0.246,
      "OPS": 0.478,
      "Pit": 20.0,
      "Str": 15.0,
      "WPA": -0.076,
      "aLI": 0.74,
      "WPA+": 0.0,
      "WPA-": -0.076,
      "cWPA": -3.27,
      "acLI": 57.3,
      "RE24": -0.8,
      "PO": 0.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Alec Bohm",
      "AB": 3.0,
      "R": 0.0,
      "H": 1.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 3.0,
      "BA": 0.224,
      "OBP": 0.292,
      "SLG": 0.362,
      "OPS": 0.654,
      "Pit": 6.0,
      "Str": 6.0,
      "WPA": -0.001,
      "aLI": 0.58,
      "WPA+": 0.026,
      "WPA-": -0.027,
      "cWPA": -0.03,
      "acLI": 44.65,
      "RE24": 0.0,
      "PO": 0.0,
      "A": 2.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Jean Segura",
      "AB": 3.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 2.0,
      "PA": 3.0,
      "BA": 0.214,
      "OBP": 0.25,
      "SLG": 0.25,
      "OPS": 0.5,
      "Pit": 12.0,
      "Str": 9.0,
      "WPA": -0.067,
      "aLI": 0.91,
      "WPA+": 0.0,
      "WPA-": -0.067,
      "cWPA": -2.89,
      "acLI": 70.2,
      "RE24": -0.6,
      "PO": 4.0,
      "A": 4.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Matt Vierling",
      "AB": 1.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 1.0,
      "SO": 0.0,
      "PA": 2.0,
      "BA": 0.154,
      "OBP": 0.214,
      "SLG": 0.231,
      "OPS": 0.445,
      "Pit": 9.0,
      "Str": 2.0,
      "WPA": 0.0,
      "aLI": 0.85,
      "WPA+": 0.021,
      "WPA-": -0.021,
      "cWPA": -0.01,
      "acLI": 65.81,
      "RE24": 0.1,
      "PO": 0.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Bryson Stott",
      "AB": 1.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 0.0,
      "PA": 1.0,
      "BA": 0.136,
      "OBP": 0.255,
      "SLG": 0.227,
      "OPS": 0.482,
      "Pit": 2.0,
      "Str": 2.0,
      "WPA": -0.021,
      "aLI": 0.84,
      "WPA+": 0.0,
      "WPA-": -0.021,
      "cWPA": -0.92,
      "acLI": 65.04,
      "RE24": -0.2,
      "PO": 0.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Edmundo Sosa",
      "AB": 2.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 2.0,
      "BA": 0.25,
      "OBP": 0.3,
      "SLG": 0.375,
      "OPS": 0.675,
      "Pit": 8.0,
      "Str": 7.0,
      "WPA": -0.059,
      "aLI": 1.16,
      "WPA+": 0.0,
      "WPA-": -0.059,
      "cWPA": -2.53,
      "acLI": 89.42,
      "RE24": -0.5,
      "PO": 1.0,
      "A": 3.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Brandon Marsh",
      "AB": 1.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 0.0,
      "PA": 1.0,
      "BA": 0.179,
      "OBP": 0.273,
      "SLG": 0.41,
      "OPS": 0.683,
      "Pit": 4.0,
      "Str": 2.0,
      "WPA": -0.013,
      "aLI": 0.51,
      "WPA+": 0.0,
      "WPA-": -0.013,
      "cWPA": -0.54,
      "acLI": 39.49,
      "RE24": -0.2,
      "PO": 0.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "away",
      "game_date": "20221105"
    },
    {
      "Batting": "Jose Altuve",
      "AB": 4.0,
      "R": 1.0,
      "H": 1.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 2.0,
      "PA": 4.0,
      "BA": 0.19,
      "OBP": 0.242,
      "SLG": 0.241,
      "OPS": 0.483,
      "Pit": 18.0,
      "Str": 11.0,
      "WPA": -0.113,
      "aLI": 1.24,
      "WPA+": 0.006,
      "WPA-": -0.118,
      "cWPA": -5.26,
      "acLI": 96.01,
      "RE24": -0.7,
      "PO": 2.0,
      "A": 3.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Jeremy Pena",
      "AB": 4.0,
      "R": 1.0,
      "H": 2.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 4.0,
      "BA": 0.345,
      "OBP": 0.367,
      "SLG": 0.638,
      "OPS": 1.005,
      "Pit": 8.0,
      "Str": 6.0,
      "WPA": 0.136,
      "aLI": 1.03,
      "WPA+": 0.159,
      "WPA-": -0.023,
      "cWPA": 6.58,
      "acLI": 79.55,
      "RE24": 0.6,
      "PO": 0.0,
      "A": 1.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Yordan Alvarez",
      "AB": 4.0,
      "R": 1.0,
      "H": 1.0,
      "RBI": 3.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 4.0,
      "BA": 0.192,
      "OBP": 0.311,
      "SLG": 0.423,
      "OPS": 0.735,
      "Pit": 11.0,
      "Str": 8.0,
      "WPA": 0.282,
      "aLI": 1.41,
      "WPA+": 0.335,
      "WPA-": -0.053,
      "cWPA": 12.16,
      "acLI": 109.36,
      "RE24": 1.4,
      "PO": 2.0,
      "A": 0.0,
      "Details": "HR",
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Alex Bregman",
      "AB": 3.0,
      "R": 1.0,
      "H": 1.0,
      "RBI": 0.0,
      "BB": 1.0,
      "SO": 1.0,
      "PA": 4.0,
      "BA": 0.294,
      "OBP": 0.379,
      "SLG": 0.569,
      "OPS": 0.948,
      "Pit": 19.0,
      "Str": 12.0,
      "WPA": -0.035,
      "aLI": 0.67,
      "WPA+": 0.024,
      "WPA-": -0.059,
      "cWPA": -1.5,
      "acLI": 51.88,
      "RE24": -0.3,
      "PO": 1.0,
      "A": 3.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Kyle Tucker",
      "AB": 3.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 1.0,
      "SO": 1.0,
      "PA": 4.0,
      "BA": 0.204,
      "OBP": 0.298,
      "SLG": 0.408,
      "OPS": 0.706,
      "Pit": 23.0,
      "Str": 15.0,
      "WPA": -0.023,
      "aLI": 0.6,
      "WPA+": 0.026,
      "WPA-": -0.048,
      "cWPA": -0.99,
      "acLI": 46.45,
      "RE24": -0.4,
      "PO": 4.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Christian Vazquez",
      "AB": 3.0,
      "R": 0.0,
      "H": 1.0,
      "RBI": 1.0,
      "BB": 0.0,
      "SO": 0.0,
      "PA": 3.0,
      "BA": 0.235,
      "OBP": 0.316,
      "SLG": 0.235,
      "OPS": 0.551,
      "Pit": 10.0,
      "Str": 8.0,
      "WPA": -0.018,
      "aLI": 1.03,
      "WPA+": 0.064,
      "WPA-": -0.082,
      "cWPA": -0.77,
      "acLI": 80.01,
      "RE24": 0.2,
      "PO": NaN,
      "A": NaN,
      "Details": "GDP",
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Trey Mancini",
      "AB": 3.0,
      "R": 0.0,
      "H": 1.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 1.0,
      "PA": 3.0,
      "BA": 0.048,
      "OBP": 0.125,
      "SLG": 0.048,
      "OPS": 0.173,
      "Pit": 16.0,
      "Str": 11.0,
      "WPA": 0.011,
      "aLI": 0.71,
      "WPA+": 0.04,
      "WPA-": -0.029,
      "cWPA": 0.49,
      "acLI": 54.71,
      "RE24": 0.0,
      "PO": 6.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Chas McCormick",
      "AB": 3.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 2.0,
      "PA": 3.0,
      "BA": 0.231,
      "OBP": 0.333,
      "SLG": 0.385,
      "OPS": 0.718,
      "Pit": 15.0,
      "Str": 10.0,
      "WPA": -0.057,
      "aLI": 0.8,
      "WPA+": 0.0,
      "WPA-": -0.057,
      "cWPA": -2.45,
      "acLI": 61.94,
      "RE24": -0.7,
      "PO": 0.0,
      "A": 0.0,
      "Details": NaN,
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    },
    {
      "Batting": "Martin Maldonado",
      "AB": 2.0,
      "R": 0.0,
      "H": 0.0,
      "RBI": 0.0,
      "BB": 0.0,
      "SO": 0.0,
      "PA": 3.0,
      "BA": 0.207,
      "OBP": 0.303,
      "SLG": 0.241,
      "OPS": 0.544,
      "Pit": 10.0,
      "Str": 6.0,
      "WPA": 0.041,
      "aLI": 1.01,
      "WPA+": 0.064,
      "WPA-": -0.023,
      "cWPA": 2.21,
      "acLI": 78.2,
      "RE24": 0.0,
      "PO": 12.0,
      "A": 0.0,
      "Details": "HBP",
      "team": "PHI",
      "game_url": "https://www.baseball-reference.com/boxes/HOU/HOU202211050.shtml",
      "home_away": "home",
      "game_date": "20221105"
    }
  ]
}
```
