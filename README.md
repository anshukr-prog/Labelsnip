# LabelSnip

Browser-based shipping-label tool for **RABDATOR** (Flipkart / Meesho / Amazon).
Upload an invoice/label PDF and it auto-processes per marketplace — everything runs
in the browser, nothing is uploaded to any server.

## What it does

| Tab | Output |
|-----|--------|
| **Flipkart** | Auto-crops each label to just the shipping label (detects the dashed cut line), trims to the border box with a thin even margin, sorted by product |
| **Meesho** | Full label page, sorted by product |
| **Amazon** | Full invoice page, sorted by product |
| **Custom** | Manual crop-to-4×6 or full-page + thank-you note |

- Sorts pages by SKU so the same products print together
- **Print** (4×6 thermal or A4) or **Save as PDF**
- **Refresh** resets for a new file; switching tabs starts fresh

## Deploy

Pure static site — just `index.html`. On Vercel: import the repo, no build command,
output directory = root. It serves `index.html` directly.

## Run locally

```bash
python3 -m http.server 8099
# open http://localhost:8099
```
