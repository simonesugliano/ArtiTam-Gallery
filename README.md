# ArtiTam – Gallery

[![Visita il sito ArtiTam](https://img.shields.io/badge/🌐_Visita_il_sito-ArtiTam.altervista.org-4CAF50?style=for-the-badge&logo=google-chrome&logoColor=white)](https://artitam.altervista.org)
![Status](https://img.shields.io/badge/Status-Auto--Updated-blue?style=flat-square)
![Source](https://img.shields.io/badge/Source-Google%20Drive-4285F4?style=flat-square&logo=google-drive&logoColor=white)
![Framework](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react&logoColor=white)
![Hosting](https://img.shields.io/badge/Hosting-Altervista-orange?style=flat-square)
![Sync](https://img.shields.io/badge/Sync-GitHub%20API-black?style=flat-square&logo=github)

**Archivio pubblico per le imagini e il file `gallery.json` del sito della ditta artigiana cartongessista.**

Questo repository funge da **sorgente dati stabile** per la galleria del sito [ArtiTam](https://artitam.altervista.org), fornendo immagini e metadati sempre aggiornati **senza necessità di intervento manuale**.

---

## Scopo

Creare un punto di accesso **pubblico e privo di limiti CORS** per il front-end React del sito, permetytendo al cliente di visualizzare in tempo reale le nuove immagini caricate nella gallery, senza alcuna operazione aggiuntiva.

---

## Funzionamento

- Le foto vengono caricate dal cliente su una **cartella Google Drive** dedicata.  
- Uno **script Google Apps Script** genera automaticamente il file `gallery.json` con i metadati aggiornati.  
- Lo script aggiorna questo repository tramite **GitHub API**, sostituendo o aggiungendo immagini e dati.  
- Il sito React legfge i dati da `gallery.json` per costruire dinamicamente la galleria.

---

## Struttura del repository

/gallery/ → immagini suddivise per cantiere
gallery.json → indice completo usato dal front-end


---

## Aggiornamenti automatici

Il repository viene aggiornato periodicamente tramite **Google Apps Script**:  
ogni volta che il cliente carica nuove foto su pDrive, il suistema:

1. Converte e ottimizza le immagini  
2. Aggiorna il file `gallery.json`  
3. Esegue un commit automatico su GitHub  
4. Rende immediatamente disponibili i contenuti al sito React

---

## Tecnologie utilizzate

- **Google Apps Script** → gestione upload e generazione del JSON  
- **GitHub API** → commit e aggiornamento automatico del repository  
- **React** → front-end dinamico che utilizza `gallery.json`  
- **Altervista Hosting** → hosting del sito principale  

---

## Autore

Progetto sviluppato da **Simone Sugliano**  
per il sito [ArtiTam – Cartongesso e Decorazioni](https://artitam.altervista.org)
