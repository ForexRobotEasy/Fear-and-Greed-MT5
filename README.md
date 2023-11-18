# Fear and Greed Indicator ReadMe

## Description
Fear and Greed is a custom indicator developed by the Forex Robot Easy Team. It is designed to calculate fear and greed levels in the market based on the input parameters provided. The indicator also identifies potential pivot key zones.

For detailed reviews and trading results of this product, please visit the [Fear and Greed MT5 Review](https://forexroboteasy.com/forex-robot-review/fear-and-greed-mt5-review-reliable-forex-trading-aid/) on the Forex Robot Easy website.

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Input Parameters
- `FastPeriod` (default = 14): The fast period for calculating fear and greed levels.
- `SlowPeriod` (default = 28): The slow period for calculating fear and greed levels.
- `PivotPeriod` (default = 10): The period for identifying potential pivot key zones.

## Indicator Buffers
The indicator uses three buffers to store the calculated values:
1. `fearLevel`: The fear level calculated using the fast period.
2. `greedLevel`: The greed level calculated using the slow period.
3. `pivotLevel`: The pivot key zone level calculated using the pivot period.

## Indicator Settings
The indicator line labels and styles are set using the following settings:
- `PlotIndexSetString`: Sets the labels for the indicator lines.
- `SetIndexStyle`: Sets the line styles for the indicator lines.
- `SetIndexColor`: Sets the line colors for the indicator lines.
- `SetIndexDrawBegin`: Sets the drawing beginning point for the indicator lines.
- `SetIndexShift`: Sets the shift for the indicator lines.
- `SetIndexEmptyValue`: Sets the empty values for the indicator lines.

## Indicator Calculation
The indicator calculation is performed in the `OnCalculate` function. It calculates the fear and greed levels for each bar in the chart based on the input parameters and the high and low prices of the bars.

The fear and greed levels are calculated as follows:
1. The highest high and lowest low for the given periods are calculated.
2. The fear and greed levels are then calculated using the formula: fearLevel = (Close - lowMin) / (highMax - lowMin) and greedLevel = 1 - fearLevel.
3. The pivot key zone level is also calculated using the formula: pivotLevel = sum(Close) / PivotPeriod.

## Usage
To use the Fear and Greed indicator, follow these steps:
1. Copy the indicator code into your MetaEditor.
2. Compile the code to generate the indicator file.
3. Attach the indicator to a chart in MetaTrader 5.
4. Adjust the input parameters as desired.
5. The fear and greed levels and the pivot key zone level will be displayed as lines on the chart.

## License and Disclaimer
This code is copyrighted by forexroboteasy.com. For the official developer and licensing information of this product, please refer to MQL5.

ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. Please use this code at your own risk and discretion.
