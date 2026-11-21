# smd-app
smd-app is a Python command-line tool for tracking account balances and spending from a CSV transaction ledger. It uses decimal arithmetic for money and provides three reports:
- ledger balance shows the total balance for each account.
- ledger spending groups expenses by category and excludes transfers.
- ledger months shows the net change for each month in chronological order, including transfers.
From the project directory, run a report with uv:
- uv run ledger balance
- uv run ledger spending
- uv run ledger months

By default, the app reads data/transactions.csv. To use a different file, pass its path after the command:
- uv run ledger months path/to/transactions.csv

The CSV must have date, account, description, category, and amount columns. Use YYYY-MM-DD for dates, positive amounts for money coming in, and negative amounts for money going out. Label transfers with the category transfer.
