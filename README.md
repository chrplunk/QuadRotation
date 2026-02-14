# Quad Rotation - 4 Stochastics Overlay

A TradingView Pine Script indicator that uses four synchronized stochastic oscillators to identify trading signals and market momentum through pattern recognition and divergence detection.

## Overview

The Quad Rotation indicator combines four stochastic oscillators with different periods to create a multi-timeframe momentum analysis tool. Each stochastic uses unique parameters to capture different aspects of price action, providing a comprehensive view of market momentum at various scales.

## Key Features

### Four Stochastics with Configurable Parameters

- **Stochastic 1** (%K: 9, %D: 3, yellow) - Fast momentum indicator
- **Stochastic 2** (%K: 14, %D: 3, orange) - Standard momentum indicator  
- **Stochastic 3** (%K: 40, %D: 4, gray) - Intermediate momentum indicator
- **Stochastic 4** (%K: 60, %D: 10, white) - Slow momentum indicator with smoothing

### Background Coloring

- **Green Background**: Triggered when multiple stochastics are oversold (below 20) and sloping upward
- **Red Background**: Triggered when multiple stochastics are overbought (above 80) and sloping downward
- Configurable sensitivity via the "Min # of Stochastics for BG Coloring" setting (1-4)

### Divergence Detection

Automatically identifies bullish and bearish divergences for each stochastic:
- **Bullish Divergence**: Price makes a lower low while stochastic makes a higher low
- **Bearish Divergence**: Price makes a higher high while stochastic makes a lower high
- Customizable divergence line colors and width
- Option to match divergence line colors to their corresponding stochastic

### ABCD Pattern Recognition

- Detects trend continuation patterns after minor price corrections
- Tracks when Stochastic 4 stays above 90 (long bias) or below 10 (short bias)
- Adjustable sensitivity with separate settings for long and short positions

## Settings

### Critical Parameters

**Min # of Stochastics for BG Coloring** (Default: 4)
- Controls the threshold for background coloring
- Setting to 4 requires all stochastics to align for signal confirmation
- Lower values increase sensitivity but may produce false signals

**Bars Since Above 90 / Below 10** (Default: 5)
- Controls ABCD pattern sensitivity
- Lower values increase sensitivity and false positives
- Acts as a "shield" preventing reversal signals until Stochastic 4 retraces

### Divergence Settings

- **Left/Right Bars for Divergence Pivot** (Default: 5) - Number of bars to scan for divergence pivots
- **Match Divergence Lines to Stochastic Color** - Checkbox to auto-match divergence colors
- **Custom Divergence Colors** - Separate red/green color options when not matching stochastic colors
- **Toggle Divergence Detection** - Enable/disable divergence identification per stochastic

## Trading Applications

### Overbought/Oversold Identification
- White horizontal lines at 20 (oversold) and 80 (overbought) levels
- Shaded blue zone between 20 and 80 shows the neutral range

### Momentum Confirmation
- Multiple stochastics sloping in the same direction confirms momentum strength
- Sloping inward (converging) indicates weakening momentum

### Divergence Trading
- Divergences between price and stochastic can signal potential reversals
- More reliable when confirmed across multiple stochastics

### Trend Continuation
- ABCD patterns identify opportunities after minor corrections within established trends
- Look for reversal candles or sharp angle changes in fast stochastics as early entry signals

## Notes

- Authored by Christopher Plunkett (March 13, 2025)
- Built for TradingView Pine Script v6
- Works as a non-overlay indicator below the price chart
- Default settings optimized for general use; adjust based on your trading style

## Tips for Best Results

- Start with the default minimum stochastic count of 4 for higher confirmation
- Reduce sensitivity gradually if missing entries
- Monitor Stochastic 1 and 2 for early direction changes
- Use Stochastic 4 as a "confirmation smoother" for trend strength
- Watch for stochastic angles greater than 10 degrees for sharp directional moves
- Use parabolic SAR or moving average distance for additional entry timing confirmation

---

**Version**: 6 (TradingView Pine Script)  
**License**: Check original source for licensing terms
