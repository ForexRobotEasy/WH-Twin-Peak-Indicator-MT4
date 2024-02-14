# WH Twin Peak Indicator MT4

This code is an implementation of the WH Twin Peak Indicator for MetaTrader 4 (MT4) platform. The indicator is designed to analyze the market's high and low points and generate trading signals when new peaks or lows are reached.

## Developer's Site

The developer's site for this indicator is [forexroboteasy.com](https://forexroboteasy.com).

## Development Name

This code is developed by the Forex Robot Easy Team.

## Libraries Used

The code imports two necessary libraries:
- Trade.mqh: This library provides functions for trading operations.
- Indicators.mqh: This library provides functions for indicator calculations.

## Constant Variables

The code defines two constant variables:
- PEAK_THRESHOLD: This variable represents the threshold value to determine if a peak is reached.
- SIGNAL_BUFFER_SIZE: This variable represents the size of the buffer to store peak signals.

## Global Variables

The code defines two global variables:
- peakBuffer: This array is used to store peak signals in the buffer.
- peakBufferCount: This counter variable keeps track of the number of signals in the buffer.

## Custom Indicator Class

The code defines a custom indicator class called WH_Twin_Peak_Indicator, which inherits from the CIndicator class. This class is responsible for analyzing the market's high and low points and generating trading signals.

### Constructor

The constructor initializes the highestHigh and lowestLow variables to 0.

### AnalyzeMarketPoints()

This function analyzes the market's high and low points by retrieving the current high and low values using the iHigh() and iLow() functions. It then compares these values with the previous highest high and lowest low values. If a new peak or low is reached, it calls the corresponding functions to generate a signal.

### GeneratePeakSignal()

This function generates a signal when a new peak is reached. It checks if the peakBuffer has space to store the signal. If it does, it adds the peak value to the buffer and increments the peakBufferCount. If the buffer is full, it sends a buy signal using the trade.Buy() function, clears the buffer, and resets the counter.

### GenerateLowSignal()

This function generates a signal when a new low is reached. It follows the same logic as the GeneratePeakSignal() function but sends a sell signal using the trade.Sell() function.

## Expert Advisor Functions

### OnInit()

This function is called when the expert advisor is initialized. It creates an instance of the WH_Twin_Peak_Indicator class.

### OnTick()

This function is called on every tick of the market. It calls the AnalyzeMarketPoints() function of the WH_Twin_Peak_Indicator to analyze the market's high and low points.

### OnDeinit()

This function is called when the expert advisor is deinitialized. It performs any necessary cleanup.

## Product Description

The WH Twin Peak Indicator MT4 is a powerful tool for analyzing the market's high and low points. It utilizes a unique algorithm to identify new peaks and lows, and generates trading signals based on these points. The indicator is designed to work on the MetaTrader 4 platform.

Key Features:
- Analyzes the market's high and low points.
- Generates trading signals when new peaks or lows are reached.
- Easy to use and implement in any trading strategy.
- Provides reliable and accurate signals for informed trading decisions.

Please note that ForexRobotEasy is not the official developer of this product. We are only showcasing the sample code that can work as described in the product. For detailed reviews and trading results of this product, visit the [official developer's site](https://forexroboteasy.com/forex-robot-review/wh-twin-peak-indicator-mt4-comprehensive-review-real-results/). To find the official developer of this product, please use the MQL5 platform.
