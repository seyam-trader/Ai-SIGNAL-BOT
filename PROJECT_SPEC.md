# A-to-Z Product Specification

## A. App
Android Kotlin application with a Home screen, signal panel, settings, paper-trading history, and authentication.

## B. Floating overlay
A small draggable AI button can be displayed above other apps after the user explicitly grants overlay permission. On tap, the app starts/uses an Android MediaProjection screen-capture session and analyzes the visible chart.

## C. Camera mode
A separate mode uses the phone camera to inspect a chart on another display. Camera permission is explicit. Frames should be processed transiently unless the user explicitly enables saving.

## D. Decision states
- BUY / UP
- SELL / DOWN
- WAIT
- NO ANALYSIS

WAIT/NO ANALYSIS must be used when evidence quality is insufficient.

## E. Indicators
Planned calculations:
- EMA/SMA
- RSI
- MACD
- Bollinger Bands
- ATR
- volume
- support/resistance
- candle structure
- volatility
- multi-timeframe confirmation when reliable data exists

## F. Time intervals
UI may offer 5s, 10s, 15s, 20s ... through 5 minutes. The engine must never fabricate unavailable market candles. The actual data provider determines supported resolution.

## G. Markets
Markets should come from a data-provider-backed list. Do not pretend OTC instruments are equivalent to exchange data. Each market needs a reliable source before analysis is enabled.

## H. Confidence
Confidence is a model score, not a probability guarantee. Display the data freshness and analysis timestamp.

## I. Performance
Record:
- signal
- timestamp
- instrument
- timeframe
- model version
- confidence
- outcome
- correct/incorrect
- streaks
- aggregate accuracy

## J. Risk controls
For paper testing:
- confidence threshold
- cooldown
- max signals
- consecutive-loss pause
- daily loss simulation limit
- stale-data protection

These controls do not guarantee profits.

## K. Login
Use server-side authentication. Never hardcode the admin password in the app.

## L. License/device authorization
Each account can be assigned authorized devices. The server can revoke a device or account.

## M. Admin
Admin-only actions:
- create/revoke user
- reset credentials
- authorize/revoke device
- enable/disable paper mode
- review usage

## N. Notifications/voice
Signal card can be spoken using Android TextToSpeech after the user enables it.

## O. Privacy
The app should process screen/camera input only after explicit user action and permissions. Avoid storing raw frames by default.

## P. Quality gates
Before considering any strategy for real-world use:
1. historical backtest
2. out-of-sample test
3. paper trading
4. forward test
5. review false signals and drawdown

There is no guarantee that a strategy that worked historically will work live.
