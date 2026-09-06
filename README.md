# AI Chart Signal Bot — A-to-Z Starter

This repository is a complete development scaffold for an Android chart-analysis assistant.

Core modes:
1. Floating AI overlay: user-authorized Android screen capture of the visible chart.
2. Camera mode: user-authorized camera analysis of a chart displayed on another screen.
3. Signal engine: BUY / SELL / WAIT with confidence and reasons.
4. Validation: backtest and paper-trading records.
5. Authentication: server-side account/license/device authorization scaffold.
6. Admin controls: revoke/rotate credentials and device authorization.

IMPORTANT:
- This project does not place or automate real-money trades.
- No model can guarantee 100% accuracy or guaranteed profit.
- Do not put passwords, API keys, exchange secrets, or private tokens in the APK or GitHub.
- A copied APK cannot be made literally impossible to copy; server-side authorization reduces unauthorized use.
- Camera/screen capture requires explicit Android user permissions.


## Real-market data starter
This version includes a public live-market data example for BTC/USDT using Binance's public REST candle endpoint.
It calculates EMA(9), EMA(21), and RSI(14) locally and displays a simple bullish/bearish/neutral analysis.
It does **not** execute real-money orders. For production trading, use an official broker/exchange API,
store credentials server-side, add authentication/rate limiting, and test with a demo account first.
