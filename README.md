# Govilo To Go

A Claude Code skill that uploads digital files to [Govilo](https://govilo.xyz/) and returns a payment-protected unlock link.

## Installation

```bash
npx skills add hau823823/gen-paylink-govilo
```

Create a dedicated env file (e.g. `.env.govilo`) with your credentials:

```env
GOVILO_API_KEY=sk_live_xxx
SELLER_ADDRESS=0xYourWalletAddress
```

> Don't have these yet? See the [Setup Guide](skills/gen-paylink-govilo/references/setup-guide.md) for step-by-step registration and wallet setup.

## Usage

Tell Claude what you want to sell:

```
"Upload my-ebook.pdf to Govilo, title 'Go Patterns eBook', price $5 USDC"
```

```
"Package the ./assets folder and create a Govilo link for 2.50 USDC"
```

Claude will ask for the required info (title, price, description) if not provided, then handle the rest automatically.

## Input Options

The `--input` flag accepts:

- A single `.zip` file
- A folder (contents are auto-zipped)
- One or more individual files (auto-packaged)

### Limits

- Max ZIP size: **20 MB**
- Max files per ZIP: **20**

## Requirements

- [uv](https://docs.astral.sh/uv/) (Python package runner)
- Python >= 3.11
- `GOVILO_API_KEY` — Bot API key from [govilo.xyz](https://govilo.xyz/)
- `SELLER_ADDRESS` — EVM wallet address on **Base chain** (or pass via `--address`)
