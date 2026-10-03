# Premiss

![Premiss](assets/premiss.png)

**Turn a trading idea into a strategy you can test and improve, directly in Claude.**

Describe your rules in plain English. Create custom Python strategies, run historical backtests across supported crypto, stock, and ETF markets, and understand the trades behind the results. Keep your code and research together in your private Premiss workspace, ready to refine and test again.

## What you can do

- **Build your own strategy.** Create custom indicators, entry and exit rules, position decisions, and risk controls using Premiss's Python strategy engine.
- **Explore supported markets.** Discover available symbols, timeframes, and historical coverage before running a test.
- **Backtest and compare.** Run a saved strategy alongside a matched buy-and-hold baseline. Inspect recorded returns, drawdowns, assumptions, and limitations.
- **Read the evidence.** Retrieve the code actually tested, individual trades, and equity-curve data, including additional pages when needed.
- **Improve saved research.** Read an existing strategy, revise its code and rules, and retain private research notes in the same workspace.

## Try it

- “Build and backtest a strategy from my trading idea.”
- “Find my saved strategies and help me improve one.”
- “Compare my latest backtest with buy and hold and explain the drawdowns.”

Claude asks for material missing choices, such as a market or historical period. Backtests run asynchronously; an accepted request is followed by a completed report when the results are ready.

## Connect your account

A [Premiss account](https://app.premissai.com) is required. Connect Premiss through Claude, sign in on the Premiss website, then select a workspace and the permissions you want to grant. Your password is entered on Premiss, never in a conversation.

For a custom remote connection, use:

```text
https://app.premissai.com/api/mcp/claude
```

Choose OAuth authentication and Claude's published identity where offered. Editing existing strategies requires edit permission. Reading paper reports requires separate paper-read permission. You can review or revoke access in [Premiss connected accounts](https://app.premissai.com/integrations/connections).

This release supports OAuth connections from hosted Claude and Claude Code. A personal installation is available before public directory approval; this repository does not claim that approval has been granted.

## Historical research and account boundaries

Available markets, history, and timeframes match the Premiss app. There are no plugin-only daily backtest or history caps. The app's code validation, sandbox, and active-run protections apply. Custom code uses Premiss's strategy package format rather than a general-purpose server shell.

Backtests currently use 10,000 simulated starting capital, 10 basis points of fees, 1 basis point of slippage, and next-bar-open fills on closed candles. Compare results only when the report marks the baseline comparable. Short simulations do not model every live-market cost or risk; inspect the assumptions returned with each report.

Historical results are not forecasts or guarantees. The connection cannot place live orders, operate bots, expose exchange credentials, change subscriptions, or publish research. It can access only the selected workspace and granted research permissions.

## Privacy and support

Premiss processes the strategy code, research requests, notes, and run results needed to perform the actions you request. Saved strategies and notes remain in your Premiss workspace. Account data is accessed through the declared Premiss MCP server under your selected permissions. See the [privacy policy](https://premissai.com/legal/privacy) and [terms of service](https://premissai.com/legal/terms) for the service's data handling and terms.

- [Get support](https://app.premissai.com/support)
- [Connection instructions](https://app.premissai.com/integrations)
- [Premiss website](https://premissai.com)
- Publisher: LoraLabs · founders@loralabs.co

## Package

This repository contains the Claude plugin manifest, remote MCP configuration, research skill, and brand asset. The plugin files are provided under the ISC license in LICENSE. The hosted Premiss service is governed by its terms of service.
