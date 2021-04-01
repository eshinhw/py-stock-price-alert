# PyStockPriceAlert

## Introduction

As a stock investor, we want to buy stocks when they are cheap, but checking stock prices every day is quite time consuming and unproductive. We can use **PyStockPriceAlert** to set up alerts on the stocks we are interested in buying. It extracts a list of companies which stock prices are lower than our predetermined prices. All we need to do is buy the stocks in the list.

## Demonstration

![image](https://user-images.githubusercontent.com/41933169/113233938-51b7f400-926e-11eb-9df5-05551ce61d80.png)

When it first runs, there is no list. When you add a symbol and its alert price, two lists will be created.

![image](https://user-images.githubusercontent.com/41933169/113234102-9e033400-926e-11eb-9bba-79856a98c39b.png)

All expensive stocks which prices are higher than our alert prices are listed on WATCHLIST.

![image](https://user-images.githubusercontent.com/41933169/113234192-cb4fe200-926e-11eb-80a2-824836db2d20.png)

All cheap stocks which prices are cheaper than our alert prices are listed on BUYLIST. These are the stocks we should consider buying.

## Installation

There are three versions of the program.

- run app.py directly on CML if you have python installed.
- run executable called app.exe inside directory 'pyStockPriceAlert_oneDir' (running time is fast as all the required files are already decompressed)
- run executable called app.exe inside directory 'pyStockPriceAlert_oneFile' (it takes some time to execute as it has to decompress all the required files)

(Executable versions are not shared on GitHub, but you can create an executable with pyinstaller!)
```
pip install pyinstaller
One Directory: pyinstaller --onedir -w app.py
One File: pyinstaller --onefile -w app.py
```

I personally prefer to use oneDir version by creating a shortcut of the executable. If you move the original app.exe out of the directory it belongs, it's not going to run!

In terms of storing data, it automatically create a database called 'stocks.db' within the same directory.

## Improvements

- Currently, price data is updated based on daily prices. It would be helpful if we can retrieve real-time price data so that we can be informed during the market hours.
- To refresh the data, we have to hit 'REFRESH LISTS' to update the price data in our database. It would be great if it automatically run refresh every fixed interval.


