# Yamb

Yamb tablica za bilježenje rezultata — ručni unos rezultata, više igrača i odabir kolona. Radi kao PWA (može se "instalirati" na početni zaslon i koristiti offline).

## Datoteke

| Datoteka | Opis |
|---|---|
| `index.html` | Cijela aplikacija (HTML + CSS + JS u jednoj datoteci) |
| `manifest.json` | PWA manifest (ime, boje, ikone) |
| `sw.js` | Service worker za offline rad i caching |
| `icon-32.png` | Favicon |
| `icon-180.png` | Apple touch ikona |
| `icon-192.png` | PWA ikona |
| `icon-512.png` | PWA ikona |
| `icon-maskable-512.png` | Maskable ikona (Android adaptive) |

Sve putanje su relativne, pa aplikacija radi i na korijenskoj domeni i na pod-putanji (npr. `korisnik.github.io/yamb/`).

## Objava na GitHub Pages

1. Napravi novi repozitorij na GitHubu (npr. `yamb`).
2. Dodaj sve gornje datoteke u korijen repozitorija (ne u podmapu).
3. Commit i push.
4. U repozitoriju idi na **Settings → Pages**.
5. Pod **Build and deployment → Source** odaberi **Deploy from a branch**.
6. Za **Branch** odaberi `main` (ili `master`) i mapu `/ (root)`, pa **Save**.
7. Nakon minutu-dvije aplikacija je dostupna na `https://KORISNIK.github.io/yamb/`.

> Bitno: glavna datoteka mora se zvati `index.html` da bi se otvorila automatski.

## Instalacija na telefon (PWA)

- **Android (Chrome):** otvori stranicu → izbornik (⋮) → "Dodaj na početni zaslon".
- **iPhone (Safari):** otvori stranicu → Podijeli → "Dodaj na početni zaslon".

Nakon instalacije radi i bez interneta.

## Napomena o ažuriranju

Service worker koristi cache pod imenom `yamb-v1`. Kad napraviš izmjene u aplikaciji, promijeni broj verzije u `sw.js` (npr. `yamb-v2`) da bi se korisnicima osvježio sadržaj.
