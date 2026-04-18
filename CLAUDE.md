# rndxlabs-website — Claude Context

Snel-startbestand voor Claude aan het begin van elke sessie.

## Wat is dit?
Marketing / corporate website voor RNDX Labs. Statische HTML, gedeployed op Netlify.

## Stack
- HTML5
- CSS (vanilla, in `assets/`)
- Eigen fonts in `fonts/`
- Meertalig via subpagina `/en/`
- Netlify voor hosting (`netlify.toml` config)
- `lab/` submap bevat prototypes / experimenten
- `demo/` bevat demo-pagina's

## Key files
```
index.html         — NL homepage
en/                — Engelse versie
assets/            — CSS, JS, shared resources
fonts/             — custom fonts
images/ (via assets) — beeldmateriaal
lab/               — experimenten/prototypes
demo/              — demo-pagina's
netlify.toml       — Netlify config (redirects, headers, build)
netlifyOLD.toml    — oude config, nog niet verwijderd
README.md          — projectbeschrijving
```

## Lokaal draaien
```bash
# Python simple server
python3 -m http.server 8000

# of Netlify CLI voor full fidelity (redirects, env vars)
netlify dev
```

## Deploy
Push naar main branch → Netlify bouwt en deployt automatisch.

## Conventies
- NL en EN versies moeten in sync blijven (zelfde pagina-structuur)
- Semantic HTML, geen inline styles
- Fonts lokaal serveren (in `fonts/`), niet via Google Fonts CDN
- Bestandsnamen kleine letters met streepjes
- `lab/` mag rommeliger zijn — is prototype-zone

## Let op
- `netlifyOLD.toml` kan waarschijnlijk weg — controleer voordat je verwijdert.
- `index.html` is groot (54KB) — overweeg sections op te splitsen in includes of partials bij verdere groei.
- Check de redirects in `netlify.toml` voordat je paden wijzigt.
