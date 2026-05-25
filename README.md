# Excel Hotels & Resorts — Wedding Landing Page

Destination wedding landing page for Excel Hotels & Resorts.
**Five private resorts** across Jim Corbett and Bhimtal, Uttarakhand.

---

## 📁 Folder structure (IMPORTANT — upload everything together)

```
/  (web root)
├── index.html                       ← Landing page (editable, ~96 KB)
├── privacy-policy.html              ← Privacy policy
├── cancellation-refund-policy.html  ← Cancellation & refund policy
└── images/                          ← ALL images live here (24 files)
    ├── hero-banner.jpg
    ├── destination-forest.jpg
    ├── destination-riverside.jpg
    ├── destination-lakeside.jpg
    ├── resort-1-banyan-retreat.jpg
    ├── resort-2-excel-corbett.jpg
    ├── resort-3-la-parle.jpg
    ├── resort-4-mango-bloom.jpg
    ├── resort-5-excel-bhimtal.jpg
    ├── logo-banyan-retreat.jpg
    ├── logo-excel-corbett.jpg
    ├── logo-la-parle.jpg
    ├── logo-mango-bloom.jpg
    ├── logo-excel-bhimtal.jpg
    ├── logo-excel-header.webp
    ├── gallery-1-haldi-laughing.jpg
    ├── gallery-2-pheras.jpg
    ├── gallery-3-smoke-entry.jpg
    ├── gallery-4-bride-entrance.jpg
    ├── gallery-5-sangeet.jpg
    ├── prewedding-1.jpg
    ├── prewedding-2.jpg
    ├── photobreak-collection.jpg
    └── og-image.webp                ← social-share preview image
```

**The `images/` folder MUST sit beside `index.html`.** All image paths are relative (e.g. `images/hero-banner.jpg`), so the structure must be preserved on the server.

---

## ✏️ Editing the page (for developers)

`index.html` is now plain, readable HTML — all images are external files, so the
code is fully editable. To find what you need:

- **Headlines / body text** — search for the text directly in `index.html`
- **Resort cards** — search for `<!-- Resort 1 -->` … `<!-- Resort 5 -->`
- **Section markers** — search for the section comments like `<!-- ══ GALLERY` or `<!-- ══ RESORT SHOWCASE`
- **CSS** — all styling is in one `<style>` block in `<head>`
- **JavaScript** — all behaviour is in one `<script>` block before `</body>`

To swap an image, just replace the file in `images/` (keep the same filename), or
change the `src="images/..."` path in the HTML.

---

## Quick Deploy

### GitHub Pages

1. Create a new public GitHub repository.
2. Upload `index.html`, `privacy-policy.html`, `cancellation-refund-policy.html`, and the **entire `images/` folder** to the repo root (preserve folder structure).
3. **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** / root → **Save**.
4. Live at `https://yourusername.github.io/repository-name/` in ~60 seconds.

### Web hosting / cPanel / FTP

1. Upload all files + the `images/` folder to your web root (e.g. `public_html/`), preserving the folder structure.
2. Visit `https://excelhotelandresort.com/index.html` to verify.

### Custom Domain (GitHub Pages)

1. **Settings → Pages → Custom domain** — enter your domain.
2. Add a CNAME record in DNS pointing to `yourusername.github.io`.
3. Tick **Enforce HTTPS**.

---

## SEO / social notes

- **og:image** is set to `https://www.excelhotelandresort.com/images/og-image.webp`.
  If you deploy to a different domain, update that absolute URL in the `<head>` of
  each HTML file so social-share previews work.
- All page text is real, indexable HTML (not image-based) — Google can crawl it fully.

---

## Integrations already wired in

- **Google Tag Manager:** container `GTM-KPPRDSJS` (head script + body noscript on every page)
- **Neodove CRM:** the "Get a Call Back" form POSTs leads to the Neodove integration endpoint, and pushes a `lead_submission` event to the GTM dataLayer
- **Contact:** Phone `+91 92113 01990` · Email `wedding@excelhotelandresort.com`

---

## To change contact details later

Search-and-replace across `index.html`, `privacy-policy.html`, `cancellation-refund-policy.html`:

- Phone display: `+91 92113 01990` → your new number
- Phone link: `tel:+919211301990` → `tel:+91XXXXXXXXXX`
- WhatsApp: `wa.me/919211301990` → `wa.me/91XXXXXXXXXX`
- Email: `wedding@excelhotelandresort.com` → your new email

No build step required.

---

## Built by

Alcor Getaways · May 2026
