# Bišu Dārzs — trīs HTML prototipi

Statiskas lapas. Nav WordPress, nav build soļa, nav atkarību — atver failu pārlūkā un tas strādā.

| Mape | Nosaukums | Lapas |
|---|---|---|
| `klinika/` | Klīnika | Animal Clinic + Veterinary Hospital + Pet Care Store |
| `kepa/` | Ķepa | Bennett's + PawCare |
| `skaidrs/` | Skaidrs | Neve + Bennett's + Pet Care Store |

Katrā mapē 6 lapas: `index`, `pakalpojumi`, `cenradis`, `klinika`, `faq`, `kontakti`. Ģenerators: `python3 _src/build.py` (saturs un CSS — `_src/`).

## Kā rediģēt

Katras lapas `<style>` ir `:root { ... }` bloks ar visiem mainīgajiem:

```css
--brand:#289CFF;   /* galvenā zilā — bisudarzs.lv */
--brand-d:#058EFF; /* tumšākā zilā — hover */
--navy:#093861;    /* galvene, kājene, virsraksti */
--r-md:14px;       /* stūru noapaļojums */
--fd / --fb        /* virsrakstu / teksta fonts */
```

Nomaini tos, un mainās visa lapa.

## Attēli un teksti

Viss `assets/img/` saturs ir lejupielādēts no **bisudarzs.lv** (2026-09-11) — klīnikas pašas
fotogrāfijas un logotips:

| Fails | No kurienes |
|---|---|
| `logo.png`, `logo-balts.png` | klīnikas logotips |
| `hero-klinika.jpg`, `hero-skaidrs.jpg` | ārste ar suni; ultraskaņas izmeklējums |
| `komanda-visi.jpg` | kolektīva foto |
| `zooveikals.jpg` | klīnikas zooveikals |
| `svc-*.jpg` (12) | terapija, USG, rentgens, laboratorija, aprīkojums u.c. |
| `team-*.jpg` (4) | darbinieku foto |
| `arch-*.jpg` (3) | suns, kaķis, truši |
| `brand-*.png` (4) | Hill's, Royal Canin, Specific, Virbac |

Teksti — no sadaļām *Par mums*, *Kolektīvs*, *Visi pakalpojumi*, *Ultrasonogrāfija*,
*Diagnostika*, *Zooveikals* un *Kontakti*.

## Kas vēl jāaizstāj

- **Komanda** — "Vārds Uzvārds" jāaizstāj ar īstiem vārdiem (fotogrāfijas jau ir īstas).
- **Atsauksmes** — teksts ir apzināti viettura; nevienu atsauksmi neizdomājām.
- **Karte** — kontaktu sadaļā jāieliek Google Maps iframe.
- **Purina ProPlan** — logotipa klīnikas lapā nebija, tāpēc rādām tekstā.

## Kas jau ir īsts

- Klīnikas sauklis: **Uzticiet savu mīluli profesionāļiem**.
- Struktūra no brīfa: 5 izvēlnes punkti, apakšizvēlnes zem *Pakalpojumi* (12) un *Par klīniku* (6).
- Darba laiks, trīs tālruņi, e-pasts, adrese un reģistrācijas numurs.
- 12 pakalpojumi ar cenām no klīnikas cenrāža; USG apraksts min īsto iekārtu (Mindray Vetus 7).
- "Kā mūs atrast" — klīnikas pašas apraksts un autobusu numuri.
- Poga **Pieteikt vizīti** ved uz kontaktu sadaļu.

## ⚠️ bisudarzs.lv ir uzlauzta

Vācot saturu, katrā lapā atradām iešpricētu svešu azartspēļu reklāmas tekstu ar ārējām saitēm
(zviedru, holandiešu, ungāru, slovāku, itāļu un vācu valodā). Prototipos tas ir pilnībā izmests.
Dzīvā lapa (WordPress 7.0.4 + qTranslate-X, abi sen neatjaunināti) ir jāsakārto atsevišķi.

## Pārbaudīts

- Nav horizontālās ritināšanas pie 500 / 820 / 1440 px.
- Telefonā izvēlne sakļaujas zem hamburgera, apakšizvēlnes atveras kā akordeons.
- `prefers-reduced-motion` izslēdz visu kustību.
