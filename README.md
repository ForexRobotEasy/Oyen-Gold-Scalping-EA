# Oyen Gold Scalping EA - ReadMe

### Developer: Forex Robot Easy Team
### Website: [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/oyen-gold-scalping-ea-review-low-deposit-high-profit-forex-software/)

This code is a sample implementation of the Oyen Gold Scalping EA, developed by the Forex Robot Easy Team. This code is not the official product, but it demonstrates how the EA can work as described.

## Description
The Oyen Gold Scalping EA is designed to trade the XAUUSD (Gold) symbol. It is a scalping strategy that aims to take advantage of short-term price movements in the gold market. The EA uses a custom indicator, called `CustomIndicator`, to generate trading signals based on trend direction and momentum.

## Installation
To use this code, follow these steps:

1. Include the necessary libraries: `Trade.mqh` and `CustomIndicator.mqh`.
2. Define the constants:
   - `SYMBOL`: The symbol to trade, set to `'XAUUSD'`.
   - `LOTS`: The lot size for each trade, set to `0.1`.
   - `STOP_LOSS`: The stop loss level in points, set to `100`.
   - `TRAILING_STEP`: The trailing stop step in points, set to `20`.
3. Create an instance of the custom indicator: `CustomIndicator sdea`.
4. Implement the following functions:
   - `OnInit()`: Initialize the custom indicator.
   - `OnDeinit(const int reason)`: Deinitialize the custom indicator.
   - `OnTick()`: Check for signals from the custom indicator and open trades based on trend direction and momentum.
   - `OnStart()`: Empty function, nothing to do here.

## Usage
The EA works as follows:

1. When a signal is generated by the custom indicator (`sdea.Signal()` returns `true`):
   - Get the trend direction and momentum from the custom indicator using `sdea.GetTrendDirection()` and `sdea.GetTrendMomentum()`.
2. If the trend momentum is equal to or greater than 0.5, proceed with opening a trade:
   - If the trend direction is upward (`TREND_UP`), open a buy trade using `OrderSend()` with appropriate parameters.
   - If the trend direction is downward (`TREND_DOWN`), open a sell trade using `OrderSend()` with appropriate parameters.
3. Set a trailing stop for the opened trade using `OrderSetTrailingStop()` with the trailing step defined in `TRAILING_STEP`.

## Disclaimer
Please note that Forex Robot Easy is not the official developer of the Oyen Gold Scalping EA. This code is a sample implementation provided to demonstrate how the EA can work based on the information available. For detailed reviews and trading results of the official product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/oyen-gold-scalping-ea-review-low-deposit-high-profit-forex-software/). To find the official developer of the Oyen Gold Scalping EA, please refer to the MQL5 platform.
