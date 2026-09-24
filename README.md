# jbg-og

Open Graph / X share cards for the **Jack Beatnic Gallery**.

This is **not** the website, **not** mint media, and **not** gallery thumbs.

| Repo | Role |
|------|------|
| `jackbeatnic.github.io` | WWW — gallery app + one homepage card (`assets/og-preview.jpg`) |
| `jb-nft-assets` | on-chain / mint originals + meta |
| `jbg-present` | thumbs + View WebP |
| `jbg-og` | this repo — 1200×630 JPEG share cards |

## Live

https://jackbeatnic.github.io/jbg-og/{collection-slug}-{token_id}.jpg

Example: https://jackbeatnic.github.io/jbg-og/avalanche-nature-stories-1496.jpg

## Rules

- JPEG only, **1200×630**, branded card (artwork tile + title + price).
- Never commit these files into `jackbeatnic.github.io` (`assets/og/` is gitignored; Pages ~1 GB limit).
- Generator: `~/jb_nft/www/generuj_og_preview.py` writes here (`JB_NFT_OG_DIR`).

## Generate (from gallery tree)

```bash
cd ~/jb_nft/www
python3 generuj_og_preview.py --nft-only --skip-existing --kolekcja avalanche_nature_stories --token 1496
cd ~/jb_nft/jbg-og
git add -A && git commit -m "og: avalanche-nature-stories 1496" && git push
```
