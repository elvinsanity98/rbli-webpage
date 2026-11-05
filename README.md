# Rural Bank of Liloy (ZN), Inc. — promotional webpage

A one-page promotional website for **Rural Bank of Liloy (ZN), Inc.** — *Always at your service.*

It presents the bank's three loan products (Agricultural, Microfinance, Commercial), the microfinance
insurance benefits, the basic requirements per loan, an "Apply now" form and the branch contact details,
all taken from the bank's 2023 brochure.

**Live site:** https://rbliloy.com/

## Files

```
index.html            the whole page (HTML + CSS + a little JavaScript, no build step)
assets/
  logo.png            logo mark (blue) · logo-white.png (for dark backgrounds) · logo-512.png
  photo-*.jpg         photos cropped from the brochure
  poly-dark.svg       low-poly background (hero, protection band)
  poly-light.svg      low-poly background (requirements band)
  og-image.png        1200×630 image shown when the link is shared (Facebook, Messenger…)
  favicon.ico, favicon-32.png, icon-192.png, apple-touch-icon.png
```

## Edit the content

Everything is in `index.html`. Search for the text you want to change, for example:

| To change…                     | Search for…                          |
| ------------------------------ | ------------------------------------ |
| Interest rates, terms, amounts | `class="rate"` or `class="specs"`    |
| Insurance benefit amounts      | `class="ledger"`                     |
| Requirements per loan          | `id="panel-agri"`, `panel-micro`, `panel-comm` |
| Branch addresses and numbers   | `class="branches"`                   |
| Email, Facebook                | `ruralbankofliloy@`, `facebook.com/rbliloy` |

Photos in `assets/` are cropped from the brochure and are small. Replace them with the original
photos (same file names) for sharper images.

## How the "Apply now" form works

The site is static, so the form does not store anything. On submit it opens the visitor's email app with a
ready-to-send message addressed to `ruralbankofliloy@gmail.com`. To change the recipient, edit the
`mailto:` address in the form and in the script at the bottom of `index.html`.

## Preview locally

```bash
python -m http.server 5173
```

Then open http://localhost:5173.

## Hosting and custom domain

Served with GitHub Pages from the `main` branch (root folder). The `CNAME` file contains `rbliloy.com`.

DNS for `rbliloy.com` (managed at Hostinger) must contain:

| Type  | Name  | Value                                                                  |
| ----- | ----- | ---------------------------------------------------------------------- |
| A     | `@`   | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` (four records) |
| CNAME | `www` | `elvinsanity98.github.io`                                              |

Do not remove the existing `MX` and `TXT` records: they belong to the domain's Titan email.
After DNS is set, open Settings → Pages in this repo and tick **Enforce HTTPS** once it becomes available.

---

Logo, photos and brand content © Rural Bank of Liloy (ZN), Inc. All rights reserved.
