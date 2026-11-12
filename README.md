# Flat To Funded Copier

Server for the Flat To Funded Copier NinjaTrader 8 add-on. Plain Node, no npm dependencies.

- `server.js`: relay between the leader and followers, plus the licence side: one-time invite codes that lock to one computer, and revoke.
- `admin.html`: the control panel, served at `/admin`.

Runs on Railway (service `f2f-copier`) with a volume mounted at `/data` for `data.json`.

Environment: `DATA_DIR=/data`, `PORT=8080`, `POLL_MS=20000`, optional `LEADER_STALE_MS` (default 45000).

This is a separate product from `GRODT-BOT/trade-copier`. The two share no users, codes or data.
