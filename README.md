## Stock_Trade_Backtesting_Model
A simple trade back-testing model using Python

### Problem Framing Backgroud

Backtesting is a key component of effective trading-system development. It is accomplished by reconstructing, with historical data, trades that would have occurred in the past using rules defined by a given strategy. The result offers statistics to gauge the effectiveness of the strategy. The underlying theory is that any strategy that worked well in the past is likely to work well in the future, and conversely, any strategy that performed poorly in the past is likely to perform poorly in the future. 

There are serveral important rules for backtesting. For example, first, takeing into account the broad market trends in the time frame a given strategy was tested. Second, exposure is a double-edged sword. Increased exposure can lead to higher profits or higher losses, while decreased exposure means lower profits or lower losses. Third, taking into account the universe in which backtesting occurred. For example, if a broad market system is tested with a universe consisting of tech stocks, it may fail to do well in different sectors. As a general rule, if a strategy is targeted toward a specific genre of stock, limit the universe to that genre; in all other cases, maintain a large universe for testing purposes. However, in this code, we are only trying to build a simple backtesting model to walkthrough the whole process. We are using the Apple stock as our data. 

### Problem Solution Provided
In short summary, our strategy is we will use moving average to generate the trade signal. If the short term moving average of the adjusted close price is higher the long term moving average of the adjusted close price, we are going to generate a buy singal; if short term moving average is lower than the long-term moving average then we are going to sell, the signal will be negative one;

#### Environment Configeration and Library

(1) Windows 10, Python3, Jupyter Notebook

(2) Numpy, Pandas, Matplotlib, pandas_datareader, xlrd(for exacting data from Execel file)

### Building Steps

(1) Import data and libraries

(2) Create Strategy class


    1) initiate instances for trading condition, trading price, closing price, long-term win and short-term win iterm.
    
    
    2) create methods for short-term moving average of the stock price, long-term moving average, trend day, previous trend day and the            difference of the two trend days.
    
    
    3) define Global Variables and assign value for them 
    

(3) Create Signal class

    
    1) create method for trade signal
    
    
    2) create method for order

(4) Create Profortlio class
    
    1) initiate original investment cash amount, long and short term share lots planing to buy and contract size
    
    2) define cash delta
    
    3) define ending account balance
    
    4) define trading ending position

(5) Analyze winning and lost and plot
    
### Things need to be better

(1) Only taking stock price moving average into account is quite limited for practical usages.

(2) Need to compare with the results got from other models
