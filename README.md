# Investimenti PWA — prima versione

## Cosa include
- Portafoglio manuale: quantità, prezzo medio, prezzo attuale, categoria e peso obiettivo.
- PAC manuale: importo o quantità mensile per strumento e budget.
- Ribilanciamento: confronto dei pesi e simulazione di ripartizione del prossimo versamento, senza vendite automatiche.
- Simulatore FIRE: rendimento nominale, inflazione, versamenti mensili, spesa obiettivo e tasso di prelievo.
- Salvataggio locale nel browser, backup JSON e importazione, export CSV.
- Interfaccia responsive e service worker per l'uso offline dopo il primo caricamento.

## Installazione su iPhone (consigliata: GitHub Pages)
Una PWA deve essere pubblicata su un indirizzo HTTPS (oppure eseguita su localhost). Aprire direttamente `index.html` da File non consente l'installazione PWA completa su iPhone.

1. Scarica ed estrai lo ZIP.
2. Crea un repository GitHub, ad esempio `investimenti-pwa`.
3. Carica nella radice del repository i file `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png` e `icon-512.png`.
4. In GitHub apri **Settings → Pages**.
5. In **Build and deployment**, scegli **Deploy from a branch**, seleziona `main` e `/ (root)`, quindi salva.
6. Attendi la pubblicazione e apri l'URL HTTPS fornito da GitHub Pages in Safari sull'iPhone.
7. Tocca **Condividi → Aggiungi alla schermata Home → Aggiungi**.
8. Avvia l'app dalla nuova icona. Aprila una volta con connessione per memorizzare le risorse offline.

## Dati e privacy
- I dati vengono salvati nel `localStorage` del browser sul dispositivo: non sono sincronizzati automaticamente con altri dispositivi.
- Esporta un backup JSON dalla dashboard prima di cancellare dati del browser o cambiare dispositivo.
- Non inserire credenziali bancarie. L'app non è collegata a Fineco e non importa quotazioni in tempo reale.
- Se pubblichi il repository come pubblico, il codice sarà visibile; i dati inseriti nell'app non vengono pubblicati dal codice, perché restano nel browser locale.

## Note sulla prima versione
- I prezzi sono inseriti manualmente in euro. Se uno strumento è quotato in USD, converti tu il prezzo in EUR prima di inserirlo.
- Il calcolo FIRE è una simulazione semplificata e non include fiscalità, commissioni, volatilità o pensione pubblica.
- Non è consulenza finanziaria e non invia ordini al broker.
