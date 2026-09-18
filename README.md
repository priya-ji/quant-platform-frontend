# Quant frontend

Vercel proxies `/api/*` to the Render backend through `vercel.json`.
The overview uses real Alpaca trades and user-selected symbols; requests run
sequentially every 15 seconds and pause if credentials are not configured.
The default research source is Alpaca, with a rolling two-year date range ending
yesterday. Backtest and validation results identify their source.

Configure ALPACA_API_KEY_ID, ALPACA_API_SECRET_KEY, and ALPACA_DATA_FEED in
Render's environment. No provider secrets belong in the frontend repository.
Claude additionally requires ANTHROPIC_API_KEY.

Synthetic sample mode is an explicit opt-in. Its simulated portfolio, P&L,
monitoring and forecast are never presented as a connected account in live mode.
An actual account or real-price paper-portfolio integration is still required
for live portfolio and forecast panels. Selecting Alpaca does not enable orders.
