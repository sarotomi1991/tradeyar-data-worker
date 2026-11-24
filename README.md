# tradeyar-data-worker

The data worker of TradeYar. It fetches hours of market data from a free public source and stores them in the app's database, so a trade's replay chart has its data ready. It runs every 10 minutes on GitHub's free runners for public repositories, and the app can start it right after a trade is imported.

- The code in `dist/` is **built** from a private repository. It only contains the download, decode and store logic.
- No secret is in this repository. The database address and key are repository **Secrets** and are never printed.
- Workflows run only on a schedule or when started by the owner. There is no `pull_request` trigger, so a fork cannot read the secrets.
