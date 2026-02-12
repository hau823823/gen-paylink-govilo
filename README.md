# Govilo To Go

A Claude Code skill that uploads digital files to [Govilo](https://govilo.xyz/) and returns a payment-protected unlock link.

## Installation

```bash
npx skills add hau823823/govilo-to-go
```

Add to your project `.env`:

```env
GOVILO_API_KEY=your-api-key-here
SELLER_ADDRESS=0xYourWalletAddress
```

## Usage

Tell Claude what you want to sell:

```
"Upload my-ebook.pdf to Govilo, title 'Go Patterns eBook', price $5 USDC"
```

```
"Package the ./assets folder and create a Govilo link for 2.50 USDC"
```