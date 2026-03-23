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