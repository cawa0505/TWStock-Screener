# Taiwan Stock Market Screener (Search and Filter Stocks)
This repository is inspired by [finlab Blog](https://www.finlab.tw/).

According to statistics, 80% of the people in the world don't like their job. If you are one of them, you should know how to manage your finances. For whom are beginners, here are some guides you should read before you investigate your money in the stock market.

## Disclaimers
This is only my personal research. I DO NOT recommend you to use it as your trading strategy, and I CAN NOT guarantee you any feasibility. You should make your own judgement and take it only as a reference. GOOD LUCK!


## ToDo-List
- [x] Crawl monthly revenue from TWSE
- [x] Crawl seansonal financial reports from TWSE
- [x] Support six stock screener methods based on monthly revenue
- [x] Score and sort stock screener results according to revenue increment
- [x] Add more stock screener methods based on financial reports
- [ ] Crawl ROE, ROA, EPS
- [ ] Backtest
- [ ] ...


## Getting Started
Implemented and tested on Ubuntu 18.04 with Python 3.6.

1. Clone this repo
```bash
$ git clone https://github.com/ch-lai/TWStock-Screener.git
```
The folder should look something like the following:
```bash
$ cd TWStock-Screener

├─ data
│  ├─ monthly
│  └─ seasonal
├─ README.md
├─ main.py
├─ crawl_report.py
├─ stock_screener.py
├─ 2019_9_19_stock_list_month.txt
├─ 2019_9_19_stock_list_season.txt
└─ requirements.txt
```


2. Install Python dependencies
```bash
$ pip3 install -r requirements.txt
```

3. Run the scripts
```bash
$ python main.py
```

4. You can also select screener methods based on your preference
```bash
> stock_screener.py

# Select multiple screener methods based on monthly revenue
Select_screener(self, 
                _MoM_growth=True,
                _YoY_growth=True,
                _Total_YoY_growth=True,
                _Highest_revenue=True,
                _LongShortTerm_growth=True,
                _Trend_growth=True)

# Select multiple screener methods based on financial reports
Select_screener(self, 
                _GPM_growth=True,
                _OPM_growth=True,
                _NPM_growth=True)
```


## Viewing Results
All results should be saved in `2019_9_19_stock_list_month.txt`. Here you can see Stock_ID and its corresponding Stock_Name. The more the ranking, the more recommended.
```bash
# 2019_9_15_stock_list.txt

3557 嘉威
5607 遠雄港
3052 夆典
1229 聯華實業
3229 晟鈦
...
```


## Report Issue
- Issues: https://github.com/ch-lai/TWStock-Screener/issues

## LICENSE
Copyright (c) 2019 [Chao-Hsiang Lai](https://github.com/ch-lai)