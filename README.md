# ⚽ 5° Memorial Silvano Maffeis — Tabellone Torneo

Applicazione web statica per la gestione e visualizzazione del **5° Memorial Silvano Maffeis**, torneo di calcio giovanile categoria **Esordienti 2° Anno (Under 13)**, organizzato da [Academy Elite Volpiano](https://www.academyelitevolpiano.it/).

---

## 📋 Descrizione

Un'unica pagina HTML (zero dipendenze, zero build tool) che funge da tabellone digitale del torneo. Progettata per essere consultata comodamente da smartphone durante le giornate di gara.

Le classifiche vengono **calcolate automaticamente** a partire dai risultati inseriti nell'HTML, senza bisogno di aggiornare manualmente i punteggi.

---

## 🗂️ Struttura del torneo

| Fase | Dettagli |
|---|---|
| **Gironi** | 6 gironi da 4 squadre (24 squadre totali) |
| **Playoff** | 6 e 7 Giugno 2026 — 2ª e 3ª classificata di ogni girone |
| **Finali** | 13 e 14 Giugno 2026 — 1ª classificata + vincenti playoff |
| **Fase Nazionale** | 20 e 21 Giugno 2026 — le 6 vincitrici delle finali |

Formato gare: **2 tempi da 25 minuti** su campo sintetico (Via Trento 104, Volpiano).

---

## 🚀 Funzionalità

- **Tab navigazione** — Gironi, Classifiche, Partite, Playoff & Finali
- **Classifiche dinamiche** — calcolate in JS al volo leggendo i risultati nel DOM
- **Risultati partite** — stati: giocata, da giocare (`vs`), rinviata
- **Design responsive** — ottimizzato per mobile
- **Nessuna dipendenza esterna** — solo Google Fonts e un logo remoto

---

## 🛠️ Stack tecnico

- **HTML5 / CSS3 / Vanilla JS** — nessun framework, nessun build step
- Font: [Exo 2](https://fonts.google.com/specimen/Exo+2), [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed), [Barlow](https://fonts.google.com/specimen/Barlow)
- Loghi: FIGC Settore Giovanile Scolastico + Academy Elite Volpiano

---

## 📦 Utilizzo

Basta aprire `index.html` in qualsiasi browser moderno — non è richiesto nessun server.

```bash
# Clona la repo
git clone https://github.com/tuo-username/memorial-maffeis.git

# Apri il file
open index.html
```

Per pubblicarlo online si può usare **GitHub Pages** (impostazione predefinita del branch `main`) oppure qualsiasi hosting statico.

---

## ✏️ Come aggiornare i risultati

I risultati si aggiornano modificando direttamente l'HTML nella sezione `#partite`.

**Partita da giocare** (classe `pending`):
```html
<div class="match-score pending">vs</div>
```

**Partita giocata** (inserire il risultato):
```html
<div class="match-score">2 - 1</div>
```

**Partita rinviata** (classe `rinv`):
```html
<div class="match-score rinv">RINV.</div>
```

Le classifiche si aggiornano automaticamente al cambio di tab.

---

## 📁 Struttura file

```
memorial-maffeis/
└── index.html      # Unico file — tutto il progetto è qui
```

---

## 🏆 Squadre partecipanti

| Girone A | Girone B | Girone C | Girone D | Girone E | Girone F |
|---|---|---|---|---|---|
| Volpiano Pianese | Chisola | Alpignano | Sisport | Lascaris | CBS |
| Vanchiglia | Rivarolese | Venaria | Lucento | Chieri | Cenisia |
| Cirié | Pozzomaina | STS | Pianezza | Borgaro | Mirafiori |
| PSG | Rebaudengo | Pro Collegno | Vinovo Sport Ev. | San Maurizio | Virtus Accademia |

---

## 📄 Licenza

Progetto ad uso interno — Academy Elite Volpiano © 2026
