# Presentazione VPN - Corso Sistemi e Reti

## Stack Tecnologico
- HTML5 + CSS3 (CSS Grid, Flexbox, clamp(), media queries)
- React 18 via CDN (unpkg.com)
- Babel standalone per transpilazione JSX
- SVG per diagrammi e visualizzazioni
- Google Fonts: Inter, JetBrains Mono, Space Grotesk
- NESSUN bundler, NESSUN npm, NESSUN framework aggiuntivo. Solo file HTML standalone.

## Architettura
- `index.html`: pagina principale con indice dei moduli (card cliccabili)
- `modulo1-*.html`, `modulo2-*.html`, ecc.: un file HTML per modulo
- Ogni file HTML è completamente standalone (include React, Babel, CSS inline)
- I componenti React sono definiti dentro un tag `<script type="text/babel">` nel file HTML

## Design System
Tema scuro con questi colori (definiti come oggetto `colors` in ogni file):
```js
const colors = {
  bg: '#0a0e17', bgCard: '#111827', bgLight: '#1e293b',
  accent: '#00d4aa',      // colore primario (verde acqua)
  accentAlt: '#0ea5e9',   // colore secondario (blu)
  text: '#f1f5f9', textDim: '#94a3b8', textMuted: '#64748b',
  border: '#334155',
  success: '#22c55e', danger: '#ef4444', warn: '#f59e0b',
  info: '#0ea5e9', purple: '#a78bfa', cyan: '#22d3ee'
};

NOTA: il colore accent può variare per modulo per differenziare visivamente.

Componenti Riutilizzabili (da definire in ogni file)
Code({ children, title }): blocco codice con syntax highlighting
Box({ type, title, children }): callout info/warn/danger/tip/success
Table({ headers, rows }): tabella stilizzata
Glow({ children, color }): card con bordo luminoso gradient
Responsive Design - CRITICO
Il target primario è una digital board 2400x1600 e deve funzionare anche su mobile.

Container principale:
maxWidth: '2200px', width: '94%', margin: '0 auto'
Media queries obbligatorie in ogni file:
max-width: 1024px: font-size 15px
max-width: 768px: font-size 14px, grid 1fr, svg responsive, pre wrap
max-width: 480px: font-size 13px, bottoni full-width
min-width: 1600px: font-size 18px, h1 52px, h2 34px
min-width: 2000px: font-size 20px, h1 60px, h2 38px
min-width: 2400px: font-size 22px, h1 68px, h2 44px
Testo responsivo: usare SEMPRE clamp()
fontSize: 'clamp(14px, 1.3vw, 18px)'  /* testo normale */
fontSize: 'clamp(12px, 1.1vw, 15px)'  /* testo piccolo */
fontSize: 'clamp(16px, 1.5vw, 22px)'  /* titoli sezione */
SVG responsivi: usare SEMPRE viewBox
<svg viewBox="0 0 600 200" style={{ width: '100%', maxWidth: '700px' }}>
Navigazione
Freccia destra / Spazio: slide successiva
Freccia sinistra: slide precedente
ESC: torna all'indice
Barra superiore fissa: nome modulo + contatore slide + progress bar
Barra inferiore fissa: bottoni navigazione + link modulo precedente/successivo
Simulatori Interattivi
Ogni modulo deve avere almeno 1-2 simulatori interattivi con:

Input chiari con label
Feedback visivo immediato (colori, animazioni)
Scenari preconfigurati per test rapidi
Spiegazione di cosa fa il simulatore prima degli input
Struttura Slide
Ogni modulo segue questa struttura:

Slide titolo (centrata, con icona, nome modulo, titolo, sottotitolo)
Slide concetti teorici (con diagrammi SVG e box informativi)
Slide esempi pratici (con blocchi Code e scenari)
Slide simulatori interattivi
Slide best practices/riepilogo
Link GitHub Pages
https://thomascasali.github.io/presentazione-vpn/