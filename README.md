# PeerPesa API Documentation

Source for the PeerPesa developer docs, live at [docs.peerpesa.co](https://docs.peerpesa.co).

PeerPesa is a stablecoin wallet and on/off-ramp for Africa. The PeerPesa API lets businesses and developers move between local fiat and digital assets, hold balances, and send payments across supported networks.

## What the API covers

- **Onramp and offramp:** convert fiat to crypto and crypto to fiat through mobile money and bank payouts.
- **Rates and quotes:** check rates, then lock a quote for 30 minutes with every fee shown up front.
- **Wallet operations:** balances, deposit wallets, withdraw, send, buy, swap, and recurring payments.
- **Records:** list orders, order details with on-chain transaction legs, and saved beneficiaries.
- **Network stats, fees, and webhooks:** HMAC-SHA256 signed event notifications.

### Supported currencies and assets

| Type | Supported |
| --- | --- |
| Fiat | KES, TZS, NGN, ZAR, ZMW |
| Stellar | XLM, USDC |
| Celo | CELO, USDT, USDC, cUSD |
| Bitcoin | Lightning addresses |

### Environments

| Environment | Base URL |
| --- | --- |
| Sandbox | `https://sandbox-api.peerpesa.co/v2` |
| Production | `https://api.peerpesa.co/v2` |

Complete KYC verification to get API keys. Requests authenticate with a public and secret key pair exchanged for a Bearer token.

## Repository layout

```text
.
├── docs.json                 # Site config and navigation
├── style.css                 # Custom styles (logo size, sidebar width)
├── index.mdx                 # Introduction
├── kyc-verification.mdx      # KYC before API access
├── authentication.mdx        # API keys and tokens
├── supported-currencies.mdx  # Fiat, assets, and networks
├── webhooks.mdx              # Webhook setup and signature verification
├── errors.mdx                # Error codes
├── pagination.mdx            # Pagination and filters
├── api-reference/            # Endpoint reference pages
└── logo/                     # Brand assets
```

## Local development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

From the repository root (where `docs.json` lives), run:

```bash
mint dev
```

Open `http://localhost:3000` to preview.

## Publishing

Changes pushed to the default branch deploy automatically to [docs.peerpesa.co](https://docs.peerpesa.co) through the Mintlify GitHub app.

## Troubleshooting

- Preview not starting: run `mint update` to get the latest CLI.
- Page shows a 404: make sure you are in the folder that contains `docs.json`, and that the page is listed in its navigation.

## Links

- Website: [peerpesa.co](https://peerpesa.co)
- Docs: [docs.peerpesa.co](https://docs.peerpesa.co)
- Support: [peerpesa.co/faqs](https://peerpesa.co/faqs)
- GitHub: [github.com/PeerPesa](https://github.com/PeerPesa)
