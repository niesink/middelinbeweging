# Middel in Beweging – Website (Jekyll)

Deze repository bevat de broncode voor de GitHub Pages site van de aerobicslessen.

## Structuur & Componenten

| Onderdeel | Bestand(en) om te bewerken | Uitleg |
|-----------|----------------------------|--------|
| WhatsApp link | `_config.yml` (`whatsapp_number`) | Nummer zonder `+` invullen. |
| Muziek / Songs | `_data/songs.yml` | Lijst met nummers. |
| Lesrooster | `_data/schedule.yml` | Weeks > sessions (dag, tijd, locatie). |
| Testimonials | `_data/testimonials.yml` | Leden quotes. |
| Prijzen | `_data/prices.yml` | Product, bedrag, omschrijving. |
| Social links | `_data/social.yml` | Platform + URL. |
| Algemene voorwaarden | `terms/index.md` | Juridische tekst aanpassen. |
| Uitleg pagina | `uitleg/index.md` | Uitgebreidere omschrijving. |
| Korte uitleg blok | `_includes/explanation.html` of tekst op homepage | Voor snelle introductie. |
| Google Calendar embed | `_config.yml` (`calendar_embed_url`) | Laat leeg om te verbergen. |
| Kleuren | `_config.yml` (`brand_color`, `secondary_color`) + `assets/css/style.scss` | Huisstijl aanpassen. |

## Homepage opbouw
In `index.html` (met front matter) worden componenten samengevoegd via `{% include ... %}`. Aanpassen van content doe je dus meestal in `_data/*.yml` of de markdown pagina's.

## Workflow via GitHub Web
1. Ga naar de gewenste file.
2. Klik op potlood (Edit).
3. Pas aan en commit direct op `main` (of maak een branch & pull request als je review wilt).
4. GitHub Pages bouwt automatisch (kan enkele minuten duren).

## Data Formats
Voorbeeld `songs.yml`:
```yml
songs:
  - title: "Levitating"
    artist: "Dua Lipa"
    bpm: 103
```
Voorbeeld `schedule.yml`:
```yml
weeks:
  - week: 45
    sessions:
      - day: "Maandag"
        time: "19:00 - 20:00"
        location: "Sporthal Noord"
```

## Styling
Custom SCSS in `assets/css/style.scss`. Jekyll (GitHub Pages) compileert dit naar `/assets/css/style.css` zolang er front matter bovenaan staat.

## Veelvoorkomende Wijzigingen
- Nieuw liedje? Voeg item toe aan `songs.yml`.
- Nieuwe week rooster? Voeg object toe aan `weeks` in `schedule.yml`.
- Prijs aanpassen? Wijzig `amount` in `prices.yml`.
- Citaat verwijderen? Verwijder het blok uit `testimonials.yml`.

## Toekomstige Verbeteringen
- Automatische BPM weergave via API.
- Meertaligheid (EN/NL) met i18n plugin.
- Formulier voor proefles inschrijving.

## Problemen?
Open een Issue of stuur een WhatsApp bericht via de homepage.
