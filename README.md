
## Taken from original project : https://github.com/eexwhyzee/NBA_knapsack
# NBA Lineup Optimizer for DraftKings

## Disclaimer
Please use this code at your own risk. This code is just for fun and entertainment purposes and should not be used unless you accept the risk of losing money.

## Overview 

With the NBA season coming up, I wanted to implement a simple [knapsack](https://en.wikipedia.org/wiki/Knapsack_problem) algorithm using python to optimize NBA lineups used for DraftKings. In daily fantasy sports, you are allotted a salary cap and the main objective is to create a lineup that will score the most fantasy points while staying at/below a salary cap, which is a great representation of the knapsack algorithm.

## Getting Started 

To get started, clone this repo and change directories:

```
git clone https://github.com/sappkevin/NBA_knapsack.git
cd NBA_knapsack/
```

## Usage

To use the optimizer, you must have an account with [DraftKings](https://www.draftkings.com/lobby), and download
the CSV file containing the player point projections along with their value. 

![](https://i.imgur.com/0K1hHIZ.png)

Once you have the CSV file on your local machine, you can run the optimizer using terminal:

```
python nba_lineup_knapsack.py -csv <PATH_TO_CSV>
or
python nba_lineup_knapsack.py (uses the default DKSalaries.csv file in the root folder -> NBA_knapsack/) 
```

where `<PATH_TO_CSV>` is the local machine file path location of the CSV file downloaded from DraftKings. 

![](https://i.imgur.com/xpiX8ns.png)

The output will be displated on your terminal, and it will contain an optimized lineup based on point projections
given the salary cap constraint. 

## Changes
-- Fixed bugs reported for original author on 01/19/2023 (ksapp)
-- Fixed bug where there were mulitple Centers generated lineup. Only 1 center is allowed to be added to DK lineup

## TODO
- Have script account for players that are listed as injured or questionable 
- Generate a CSV file and automatically import/upload to DK for custom lineups
- Have more algorithm options outside of Knapsack
- Automatically download CSV files from Draftkings using [Selenium](http://www.seleniumhq.org/).
- Implement player points projections using advanced analytics (USG%) and possibly player/team matchup data. 
