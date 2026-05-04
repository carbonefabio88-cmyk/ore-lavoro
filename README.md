# Ore Lavoro — PWA

Tracker ore lavorative con sincronizzazione automatica su Google Drive.

---

## Installazione sul telefono Android

### Netlify Drop (più semplice)
1. Vai su https://app.netlify.com/drop
2. Trascina la cartella `pwa-ore` nella pagina
3. Ottieni un link tipo `https://random-name.netlify.app`
4. Apri il link con Brave su Android → Menu → **Installa app**

---

## Sync automatico Google Drive — Setup Client ID

### Step 1 — Crea il Client ID (gratuito)
1. Vai su https://console.cloud.google.com/
2. Nuovo progetto → es. "OreLavoro"
3. API e servizi → Libreria → cerca "Google Drive API" → Abilita
4. API e servizi → Credenziali → Crea credenziali → ID client OAuth
5. Tipo: Applicazione web · Nome: OreLavoro PWA
6. Origini JavaScript autorizzate: aggiungi il tuo URL Netlify/GitHub
7. Crea → copia l'ID client (xxxxx.apps.googleusercontent.com)

### Step 2 — Inserisci nell'app
1. App → ⚙ → sezione GOOGLE DRIVE
2. "▸ Imposta Client ID" → incolla → Salva

### Step 3 — Connetti
1. Tocca **Connetti** → accedi con Google
2. Da ora ogni timbratura salva `ore-lavoro-backup.json` su Drive (sovrascrittura)

> Il token OAuth dura ~1 ora. Alla scadenza l'app avvisa e basta riconnettersi.
> I dati locali sono sempre al sicuro indipendentemente da Drive.

---

## Funzionalità
- 4 click: entrata → pausa → rientro → uscita
- Arrotondamento a 15 min (entrata per eccesso, uscita per difetto)
- Lun–Ven 8h ordinarie · Sabato tutto straordinario
- Banca ore totale · Storico per mese · Modifica registrazioni
- Export JSON / Excel · Sync Drive automatico
- Notifica serale · Tema chiaro/scuro · Funziona offline
