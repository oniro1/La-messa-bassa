# La Messa Bassa · sito vetrina

Sito statico: `index.html` + `frames/` (piano sequenza, 242 WebP) + `models/` (piatti 3D glTF).
Librerie da CDN: GSAP 3.12.5 + ScrollTrigger, model-viewer 3.5.0. Nessun build.

## Pubblicare gratis su Render
1. Crea un repository GitHub e carica il contenuto di questa cartella (index.html in radice).
2. Su https://dashboard.render.com → **New → Static Site** → collega il repository.
3. Build command: vuoto · Publish directory: `.` → **Create Static Site**.
   (In alternativa **New → Blueprint**: Render legge `render.yaml`.)
4. Dominio: Settings → Custom Domains (es. lamessabassa.it), HTTPS automatico.

Ogni `git push` ripubblica il sito.

## Da completare con il cliente
- Orari di apertura (sezione "Dove siamo" e `openingHours` nel JSON-LD in testa al file)
- Partita IVA nel footer (obbligatoria per un sito commerciale)
- Foto dei piatti mancanti → nuovi modelli 3D in `models/` + una riga in `DISH_MODELS`
- La cartella `_preview/` serve solo ai test locali e si può eliminare.

## Provarlo in locale
`npx serve .` e apri http://localhost:3000 (aperto come file:// i modelli non si caricano).
