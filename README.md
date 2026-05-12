# LawHub — Web App (Vercel)

App web per la gestione dello studio legale.  
Deploy su Vercel in 2 minuti — zero configurazione, zero server.

## Deploy su Vercel

### Metodo 1 — Drag & Drop (più veloce)
1. Vai su https://vercel.com → "Add New Project"
2. Scegli "Deploy from file upload" o trascina questa cartella
3. Clicca Deploy → ottieni subito `lawhub-xxxx.vercel.app`

### Metodo 2 — Da GitHub (consigliato per aggiornamenti)
```bash
# 1. Crea repo GitHub con questi file
git init
git add .
git commit -m "LawHub v1.0"
git push origin main

# 2. Su vercel.com → Import Git Repository → seleziona il repo
# 3. Deploy automatico — si aggiorna ad ogni git push
```

### Metodo 3 — Vercel CLI
```bash
npm i -g vercel
vercel login
vercel --prod
```

## Struttura

```
lawhub-vercel/
├── index.html    ← tutta l'app (HTML + CSS + JS)
├── vercel.json   ← routing + headers di sicurezza + cache
└── README.md
```

## Note sui dati

I dati vengono salvati nel **localStorage** del browser:
- Persistono tra le sessioni sullo stesso browser/PC
- NON si sincronizzano tra dispositivi diversi
- Usa "Esporta → JSON" per fare backup manuali
- Per sincronizzazione multi-dispositivo servirebbe un backend

## Sezioni

- ⚖ **Pratiche** — tabella editabile, filtri, ordinamento
- 👤 **Clienti** — schede card, ricerca
- 📅 **Appuntamenti** — calendario + lista
- 🗄 **Backup** — snapshot locali, ripristino
- ⚙ **Account** — profilo studio

*LawHub Studio Legale · v1.0.0 · 2026*
