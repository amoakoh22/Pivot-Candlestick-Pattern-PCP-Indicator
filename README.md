# 📈 Pivot Candlestick Pattern (PCP) Indicator — by Samuel Amoakoh

A custom TradingView indicator that detects unique three-bar candlestick formations around pivot zones to enhance market timing and trend analysis. The PCP logic is inspired by geometric symmetry—particularly the triangle—and the analytical insights of Anna Coulling.

## 🔍 What Is PCP?

The **Pivot Candlestick Pattern (PCP)** is a three-bar formation where the middle candle acts as a pivot:
- **Bullish PCP**: Middle bar has a lower high and low than its neighbors
- **Bearish PCP**: Middle bar has a higher high and low than its neighbors

These patterns often signal short-term reversals or continuation setups when confirmed by price action.

## 🧠 Core Logic

```pine
// Bullish PCP: middle bar has lower high and low than bars before and after
isBullishPCP = high[1] < high[0] and high[1] < high[2] and low[1] < low[0] and low[1] < low[2]

// Bearish PCP: middle bar has higher high and low than bars before and after
isBearishPCP = high[1] > high[0] and high[1] > high[2] and low[1] > low[0] and low[1] > low[2]
```

Signals are confirmed on the bar immediately following the pattern.

## 🎨 Visual Features

- Customizable label colors and text for bullish/bearish PCPs
- Tooltip includes price level for quick reference
- Labels plotted directly on chart for intuitive pattern tracking

## 🔔 Alerts

Enable alerts for:
- Bullish PCP detection
- Bearish PCP detection

Alerts are triggered once per bar when a new pattern is confirmed.

## ⚙️ Settings

- Toggle alerts for bullish/bearish signals
- Customize label colors, text, and positioning
- Adjust visual styling to suit your chart theme

## 📌 Usage Tips

- Works best on timeframes H1 and above
- Combine with volume or trend indicators for confirmation
- Use triangle logic to anticipate breakout zones near PCP clusters

## 🛠️ Installation

1. Copy the Pine Script code into TradingView’s Pine Editor
2. Add the script to your chart
3. Configure settings via the indicator panel

## 📬 Author

Developed by **Samuel Amoakoh**, a technical founder and financial engineering candidate passionate about blending geometric insight with market structure.
