# Running Tests

## Prerequisites

None are needed to run the mock tests. To run against the live Apideck Accounting API, set the following environment variables:

- `IS_LIVE_SERVER` set to `true`
- `APIDECK_API_KEY` your secret API key
- `APIDECK_APP_ID` your Unify application ID
- `APIDECK_CONSUMER_ID` your consumer ID

## Test Environments

| Group | Target | Notes |
|---|---|---|
| `mock_tests` | local mock service on port 9090 | default |
| `live_tests` | Apideck Accounting API | requires `IS_LIVE_SERVER=true` and the variables above |

## Running Tests

```bash
bal test
```

To run a single group:

```bash
bal test --groups mock_tests
```

## Tests

The suite covers 25 operations against the mock service: listing, creating, reading, updating and deleting invoices, bills, customers and suppliers, plus listing and reading payments, ledger accounts, journal entries, tax rates and bank accounts.
