# Pizzeria Montalto — Website

Single-Page Website für **Pizzeria Montalto** in Frankfurt am Main.
Eine `index.html`, keine Build-Tools, keine Dependencies — direkt deploybar auf GitHub Pages.

## Was drin ist

- Dunkles, editorial-italienisches Design (Fraunces + Manrope von Google Fonts)
- Hero mit Steinofen-Stimmung
- Über-uns-Sektion mit Stats
- **Komplette Speisekarte** mit Tab-Filter (Pizza · Le Bianche · Pasta · Insalate · Dolci & Drinks)
- Service-Strip (Vor Ort · Abholung · Lieferung · Vegane Optionen)
- Bestell-CTA mit Telefon-Buttons
- Kontakt-Sektion mit eingebetteter OpenStreetMap
- Schema.org Restaurant-Markup für SEO
- Mobile-Menu, scroll-reveal Animationen, sticky Tab-Navigation

## Hosting auf GitHub Pages — Schritt für Schritt

1. **Repository erstellen** auf GitHub (z. B. `pizzeria-montalto` oder `montalto-website`). Public.
2. **`index.html` hochladen** ins Repo-Root (per Web-UI „Add file → Upload files" oder per Git push).
3. Im Repo: **Settings → Pages**.
4. Unter **Source** → **Deploy from a branch**.
5. **Branch:** `main` · **Folder:** `/ (root)` → **Save**.
6. ~1 Minute warten. Die Seite ist dann unter
   `https://<dein-github-name>.github.io/<repo-name>/` erreichbar.

### Eigene Domain anhängen (optional, z. B. `pizzeria-montalto.de`)

1. Bei deinem Domain-Provider einen **CNAME-Eintrag** auf
   `<dein-github-name>.github.io` setzen
   (für Apex-Domain: A-Records auf GitHub's IPs — siehe GitHub-Docs).
2. Eine Datei namens `CNAME` (ohne Endung) ins Repo legen mit nur diesem Inhalt:
   ```
   pizzeria-montalto.de
   ```
3. Unter **Settings → Pages → Custom domain** eintragen und **Enforce HTTPS** anhaken.

## Anpassungen

- **Bilder austauschen:** Die Hero- und About-Bilder sind aktuell von Unsplash (Platzhalter).
  Echte Fotos vom Restaurant ins Repo legen und in `index.html` die `src=`-URLs ersetzen.
  Suche im File nach `images.unsplash.com` — da sind die zwei Stellen.
- **Geschäftliche E-Mail nachtragen:** Sobald die offizielle Mail-Adresse steht, im Footer und
  ggf. im Schema.org-Block ergänzen. Aktuell ist als Kontakt nur Telefon hinterlegt.
- **Öffnungszeiten:** Falls bekannt, im `<script type="application/ld+json">` und in der
  Kontakt-Sektion ergänzen (Suche nach `Service`).
- **Impressum & Datenschutz:** Aktuell sind das Placeholder-Links (Alert).
  Pflicht in Deutschland — also unbedingt eigene `impressum.html` und `datenschutz.html`
  anlegen und die Links in `index.html` darauf umbiegen.

## Technische Hinweise

- Keine Cookies, kein Tracking, kein JS-Framework.
- OpenStreetMap-iframe statt Google Maps (kein API-Key nötig, kein Tracking).
- Mobile-responsive ab 360 px Breite.
- Lighthouse-freundlich: lazy-loading Bilder, preconnect zu Fonts, semantic HTML.
