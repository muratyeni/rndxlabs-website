# rndxlabs-website

Marketing- en corporate website voor RNDX Labs. Statische HTML, gedeployed op Netlify.

## Structuur

```
index.html         NL homepage
en/                Engelse versie
assets/            CSS, JS, shared resources
fonts/             Custom fonts (lokaal, niet via CDN)
lab/               Prototypes en experimenten
demo/              Demo-pagina's
netlify.toml       Netlify config (redirects, headers)
```

## Lokaal draaien

```bash
# Simpele server
python3 -m http.server 8000

# of met Netlify CLI (voor redirects/headers testing)
netlify dev
```

## Deploy

Push naar `main` → Netlify bouwt en publiceert automatisch.

## Conventies

- NL en EN versies in sync houden (zelfde pagina-structuur)
- Semantic HTML, geen inline styles
- Fonts lokaal serveren vanuit `fonts/` — niet via Google Fonts
- Bestandsnamen kleine letters met streepjes
- `lab/` is prototype-zone (mag rommeliger zijn)

## Meer info

- `CLAUDE.md` — context voor Claude sessies
- `netlify.toml` — deploy-config (redirects, headers)

## Licentie

Private. Intellectueel eigendom van RNDX Labs B.V.
