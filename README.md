# TradingView Strategies from Unholy Grails

This repository contains Pine Script implementations of trading strategies outlined in the book "Unholy Grails" by Nick Radge. These strategies are designed to be used on the TradingView platform and focus on systematic trading approaches.

## Strategies Included

### 1. Turtle Soup Strategy
A mean reversion strategy that trades against false breakouts of the 20-day high/low. The strategy:
- Identifies potential false breakouts
- Uses ATR-based stop loss and take profit levels
- Includes customizable lookback periods and risk parameters

**Detailed Explanation:**
- The strategy looks for false breakouts of the 20-day high/low levels
- When price breaks below the 20-day low and then closes above it, it generates a long signal
- When price breaks above the 20-day high and then closes below it, it generates a short signal
- Stop loss and take profit levels are based on ATR to adapt to market volatility
- Best used in ranging markets where false breakouts are common
- Recommended timeframe: 1H to 4H

### 2. Donchian Channel Breakout
A trend-following strategy based on Donchian Channels that:
- Identifies breakouts from established price channels
- Uses a middle line for additional confirmation
- Implements ATR-based position sizing and risk management

**Detailed Explanation:**
- Uses Donchian Channels to identify price ranges and potential breakouts
- Upper channel: highest high of the period
- Lower channel: lowest low of the period
- Middle line: average of upper and lower channels
- Long entry when price breaks above the upper channel
- Short entry when price breaks below the lower channel
- Best used in trending markets with clear directional moves
- Recommended timeframe: 4H to Daily

### 3. Volatility Breakout Strategy
A strategy that combines volatility expansion with Bollinger Bands to:
- Identify significant market moves
- Trade breakouts during periods of expanding volatility
- Use multiple confirmation signals for trade entries

**Detailed Explanation:**
- Uses Bollinger Bands to identify volatility expansion
- Monitors volume for confirmation of breakouts
- Long entry when price breaks above upper band with increasing volume
- Short entry when price breaks below lower band with increasing volume
- Stop loss and take profit based on ATR for volatility adjustment
- Best used in markets with clear volatility cycles
- Recommended timeframe: 1H to 4H

### 4. Moving Average Crossover
A classic trend-following strategy that:
- Uses fast and slow moving averages
- Generates signals on crossovers
- Includes customizable MA periods

**Detailed Explanation:**
- Uses two moving averages (default: 10 and 20 periods)
- Long entry when fast MA crosses above slow MA
- Short entry when fast MA crosses below slow MA
- ATR-based stop loss and take profit for risk management
- Best used in trending markets
- Recommended timeframe: 1H to Daily

### 5. RSI Divergence
A mean reversion strategy that:
- Identifies divergences between price and RSI
- Uses overbought/oversold levels
- Includes customizable RSI parameters

**Detailed Explanation:**
- Looks for divergences between price action and RSI
- Bullish divergence: price makes lower lows while RSI makes higher lows
- Bearish divergence: price makes higher highs while RSI makes lower highs
- Uses overbought (70) and oversold (30) levels for additional confirmation
- Best used in ranging markets with clear support/resistance levels
- Recommended timeframe: 1H to 4H

### 6. MACD Strategy
A trend-following strategy that:
- Uses MACD crossovers for signals
- Includes customizable MACD parameters
- Implements ATR-based risk management

**Detailed Explanation:**
- Uses standard MACD settings (12, 26, 9)
- Long entry on MACD line crossing above signal line
- Short entry on MACD line crossing below signal line
- Histogram can be used for additional confirmation
- Best used in trending markets with clear momentum
- Recommended timeframe: 1H to Daily

### 7. Stochastic Oscillator
A momentum strategy that:
- Uses stochastic crossovers
- Includes customizable overbought/oversold levels
- Implements ATR-based position sizing

**Detailed Explanation:**
- Uses %K and %D lines for signal generation
- Long entry when %K crosses above %D in oversold territory
- Short entry when %K crosses below %D in overbought territory
- Standard overbought (80) and oversold (20) levels
- Best used in ranging markets with clear momentum shifts
- Recommended timeframe: 1H to 4H

### 8. Bollinger Band Breakout
A volatility-based strategy that:
- Trades breakouts from Bollinger Bands
- Uses customizable band parameters
- Includes ATR-based risk management

**Detailed Explanation:**
- Uses standard 20-period Bollinger Bands
- Long entry on breakout above upper band
- Short entry on breakout below lower band
- Middle band can be used as additional confirmation
- Best used in markets with clear volatility patterns
- Recommended timeframe: 1H to 4H

### 9. ADX Trend
A trend strength strategy that:
- Uses ADX for trend confirmation
- Includes customizable ADX threshold
- Implements ATR-based position sizing

**Detailed Explanation:**
- Uses ADX to measure trend strength
- Long entry when ADX > threshold and price above 20-period SMA
- Short entry when ADX > threshold and price below 20-period SMA
- Higher ADX indicates stronger trend
- Best used in strong trending markets
- Recommended timeframe: 4H to Daily

### 10. Volume Profile
A volume-based strategy that:
- Uses volume profile for price levels
- Includes volume threshold parameters
- Implements ATR-based risk management

**Detailed Explanation:**
- Identifies key price levels based on volume distribution
- Long entry on breakout above high-volume price level
- Short entry on breakout below high-volume price level
- Uses volume threshold to confirm significant moves
- Best used in markets with clear volume patterns
- Recommended timeframe: 1H to 4H

### 11. Ichimoku Cloud
A comprehensive trend strategy that:
- Uses multiple Ichimoku components
- Includes customizable periods
- Implements ATR-based position sizing

**Detailed Explanation:**
- Uses Tenkan-sen (9), Kijun-sen (26), and Senkou Span A/B
- Long entry when price above cloud and Tenkan-sen > Kijun-sen
- Short entry when price below cloud and Tenkan-sen < Kijun-sen
- Cloud thickness indicates trend strength
- Best used in trending markets
- Recommended timeframe: 4H to Daily

### 12. Parabolic SAR
A trend-following strategy that:
- Uses Parabolic SAR for trend direction
- Includes customizable acceleration and maximum
- Implements ATR-based risk management

**Detailed Explanation:**
- Uses Parabolic SAR to identify trend direction
- Long entry when price crosses above SAR
- Short entry when price crosses below SAR
- Acceleration and maximum parameters control sensitivity
- Best used in trending markets
- Recommended timeframe: 1H to Daily

### 13. Williams %R
A momentum strategy that:
- Uses Williams %R for overbought/oversold
- Includes customizable levels
- Implements ATR-based position sizing

**Detailed Explanation:**
- Uses Williams %R to identify overbought/oversold conditions
- Long entry when %R crosses above oversold (-80)
- Short entry when %R crosses below overbought (-20)
- Divergences can be used for additional confirmation
- Best used in ranging markets
- Recommended timeframe: 1H to 4H

## Getting Started

1. Clone this repository
2. Open TradingView and create a new Pine Script
3. Copy the contents of any strategy file from the `strategies` directory
4. Paste the code into the Pine Script editor
5. Click "Add to Chart" to apply the strategy

## Strategy Parameters

Each strategy includes customizable parameters that can be adjusted through the TradingView interface:

- `ATR Period`: Period for Average True Range calculation (default: 14)
- `ATR Multiplier`: Multiplier for take profit levels (default: 2.0)
- `Stop Loss Multiplier`: Multiplier for stop loss levels (default: 3.0)
- Additional strategy-specific parameters as described in each file

## Risk Management

All strategies include built-in risk management features:
- Position sizing based on account equity
- ATR-based stop loss levels
- Take profit targets
- Volatility-adjusted position sizing

## Usage Notes

- These strategies work best on liquid markets with good volatility
- Recommended timeframes: 1H to 4H for most strategies
- Test thoroughly on historical data before live trading
- Consider market conditions when selecting which strategy to use

## Disclaimer

This software and all trading strategies contained herein are for educational and research purposes only. The author and contributors:

1. Make no representations or warranties about the accuracy, completeness, or suitability of these strategies for any particular purpose
2. Are not liable for any direct, indirect, incidental, special, consequential, or exemplary damages resulting from the use of these strategies
3. Do not guarantee any specific trading results or profits
4. Are not responsible for any trading losses incurred by users of these strategies

Trading involves substantial risk of loss and is not suitable for all investors. Past performance is not indicative of future results. Before using any of these strategies:

- Conduct your own research and due diligence
- Test thoroughly on historical data
- Start with small position sizes
- Never risk more than you can afford to lose
- Consider consulting with a financial advisor

By using these strategies, you acknowledge that you are solely responsible for your trading decisions and any resulting profits or losses.

## License

MIT License - feel free to use and modify these strategies as needed.

## Contributing

Feel free to submit issues and enhancement requests! 