# SITEG – Sito Italiano di Epigrafia Greca

Sito statico costruito con [Jekyll](https://jekyllrb.com) e pubblicato gratis con GitHub Pages.

## Come aggiungere una news

1. Su GitHub apri la cartella `_posts` e clicca **Add file → Create new file**.
2. Chiama il file `AAAA-MM-GG-titolo-breve.md`, per esempio `2026-11-05-seminario-padova.md`.
3. Incolla e completa:

```
---
title: "Titolo della news"
sottotitolo: "Luogo, date"
categories: [news]
---

Testo della notizia. Per un link: [testo del link](https://indirizzo.it).
```

4. Clicca **Commit changes**. Dopo circa un minuto la news è online.

Per un resoconto usa `categories: [resoconti]` e aggiungi la riga `autore: "Nome Cognome"`.

Per allegare una locandina: carica il PDF nella cartella `assets/file/` e nel testo scrivi `[Locandina](/assets/file/nome-file.pdf)`.

## Struttura

| Cosa | Dove |
|---|---|
| News e resoconti | `_posts/` |
| Pagine (Chi siamo, Corsi, Link…) | `pagine/` |
| Voci del menu | `_data/menu.yml` |
| Indirizzo, telefono, email del piede | `_config.yml` |
| Colori e caratteri | `assets/css/stile.css` |

## Pubblicazione

Nel repository: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`**.

Per usare il dominio `www.siteg.it`: in **Settings → Pages → Custom domain** inserisci `www.siteg.it`, poi presso il registrar del dominio crea un record `CNAME` da `www` verso `NOMEACCOUNT.github.io`. Infine in `_config.yml` imposta `url: "https://www.siteg.it"`. I vecchi indirizzi (`/index.php/...`) delle pagine migrate reindirizzano già alle nuove.

## Da completare

- Migrare il testo completo delle news più vecchie (ora rimandano al sito attuale) e l'archivio dal 2009 al 2025.
- Sostituire la sintesi delle condizioni di utilizzo con il testo ufficiale.
- Aggiornare corsi e link (molti risalgono al 2009).
- Decidere come sostituire l'area riservata (vedi la pagina Partecipa).

## Anteprima sul proprio computer (facoltativo)

```
bundle install
bundle exec jekyll serve
```
poi apri http://localhost:4000
