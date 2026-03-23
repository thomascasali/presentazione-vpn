# Presentazione VPN — Corso Sistemi e Reti

Presentazione interattiva sulle Virtual Private Network per il corso di Sistemi e Reti (ITIS).

**[Apri la presentazione](https://thomascasali.github.io/presentazione-vpn/)**

## Struttura

| Modulo | Titolo | Slide | File |
|--------|--------|-------|------|
| 1 | Fondamenti VPN | 11 | `modulo1-fondamenti-vpn.html` |
| 2 | IPsec in Dettaglio | 11 | `modulo2-ipsec.html` |
| 3 | VPN SSL/TLS e OpenVPN | 11 | `modulo3-openvpn.html` |
| 4 | WireGuard e VPN Moderne | 9 | `modulo4-wireguard.html` |
| 5 | Scenari Pratici e Lab | 8 | `modulo5-scenari-pratici.html` |
| 6 | Quiz e Riepilogo | 5 | `modulo6-quiz.html` |

**Totale: 55 slide**

## Simulatori interattivi

| Simulatore | Modulo | Descrizione |
|------------|--------|-------------|
| Incapsulamento VPN | M1 | Visualizza pacchetto prima/dopo crittografia VPN |
| Attacco e Difesa | M1 | Simula attacchi con/senza VPN attiva |
| IKE Handshake | M2 | Step-by-step della negoziazione IKE Phase 1 e 2 |
| AH vs ESP | M2 | Confronto visivo protezione AH e ESP in Transport/Tunnel |
| Generatore .ovpn | M3 | Genera configurazione OpenVPN client con parametri personalizzabili |
| TLS Handshake | M3 | Visualizzazione handshake TLS con mutual authentication |
| Confronto Performance | M4 | Confronto throughput, latenza, codice e complessità tra protocolli |
| Configuratore Scenario | M5 | Genera config WireGuard/OpenVPN/IPsec per scenari reali |
| Quiz 15 domande | M6 | Quiz interattivo con spiegazioni e punteggio |

## Stack tecnologico

- HTML5 + CSS3 (Grid, Flexbox, clamp(), media queries)
- React 18 via CDN
- Babel standalone per JSX
- SVG per diagrammi
- Google Fonts: Inter, JetBrains Mono, Space Grotesk
- Nessun bundler, nessun npm — file HTML standalone

## Navigazione

- **Freccia destra / Spazio**: slide successiva
- **Freccia sinistra**: slide precedente
- **ESC**: torna all'indice
