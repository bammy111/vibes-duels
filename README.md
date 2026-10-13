# Vibe Duels — 1v1 Skill-Game Wager Prototype

An iMessage-GamePigeon-style arcade where two players stake an amount, play a quick skill game, and the winner is paid from an escrow pool minus a **5% platform fee**.

> ⚠️ **Prototype / simulation only.** Wallets, escrow and payouts run in the browser. **No real money moves.** The opponent "Chidi O." is a local AI.

## What's inside

| Path | What it is |
|---|---|
| `index.html` | The full app: wallet, stake flow (₦500–₦100,000), challenge link, match lobby, escrow ledger, 5% rake settlement, 21-game catalogue |
| `games/` | A standalone page for each playable game, each with its own demo wallet and "Ledger Update" screen |

## Playable games

**Arcade & physics:** 8-Ball Pool · 9-Ball Pool · Darts 501 · Cup Pong · Basketball · Archery · Mini Golf · Knockout · Tanks
**Board & strategy:** Chess · Checkers (Draughts) · Mancala · Reversi · Four in a Row · Dots & Boxes · Gomoku · Ludo
**Cards:** Whot! · Crazy 8s

(Not yet built: Word Games, 20 Questions — they appear in the catalogue and use a "pick a winner" simulation.)

## How a match works

1. Pick a game and set a stake (₦500–₦100,000).
2. Funds are locked in the simulated escrow and a challenge link is generated.
3. The opponent joins (simulated), both stakes sit in the pool.
4. Play the game vs. Chidi O.
5. The winner receives `pool − 5%`. A draw refunds both stakes with no fee. Every step is written to the ledger.

Example: ₦1,000 stake each → ₦2,000 pool → ₦100 platform fee → **₦1,900 payout**.

## Run it

Open `index.html` in a browser (or any file in `games/`). It needs internet access because React and Tailwind are loaded from public CDNs. To host it free, enable **GitHub Pages** (Settings → Pages → deploy from `main`).

## Tech

Single-file HTML · React 18 (UMD) · Tailwind (CDN) · HTML5 Canvas / SVG · no backend, no build step

## Roadmap to production

- Server-authoritative game logic and a real escrow ledger (never trust the client with results)
- Real payments (e.g. Paystack / Flutterwave) and KYC
- Matchmaking, real shareable challenge links, anti-cheat
- Proper licensing and compliance for real-money gaming in your market
- Word Games and 20 Questions

## Disclaimer

This repository is a design/engineering prototype. It does not process payments and is not a licensed gambling or betting product.
