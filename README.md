# Gamma Bilder-Archiv

Bild-Sammlung extrahiert aus 484 Gamma-Decks (gamma.app), aufbereitet als durchsuchbare Stock-Bibliothek.

## Zahlen

- **7.733 kuratierte Bilder** aus 484 Decks
- 1.039 erkannte Mehrfach-Verwendungen (Theme-Hintergründe) auf 38 Unikate dedupliziert und ausgeschlossen
- 170 Klein-Icons/Logos (<400px) ausgeschlossen
- Quelle: JPEG-Bildobjekte (`/DCTDecode`), direkt aus den PDF-Exports der Decks extrahiert

## Struktur dieses Repos

- `katalog.csv` / `katalog.json` — vollständiger Katalog: Dateiname, Kategorie, Deck-Titel, `gamma_id` + `gamma_url` (Rückverfolgung zum Original-Deck), Breite/Höhe, Aspect Ratio, Dateigröße, MD5, Tags
- Die Bilder selbst liegen **nicht** im Git-Repo (zu groß), sondern als ZIP pro Kategorie unter [Releases](../../releases) — ein ZIP pro Kategorie, siehe Tabelle unten

## Kategorien

| Kategorie | Bilder | Größe |
|---|---|---|
| 01-Katholisch-Liturgie | 1.453 | 163 MB |
| 02-FinTech-Trading | 1.781 | 176 MB |
| 03-Recht-Beratung | 8 | 1 MB |
| 04-Chatbots-Bots-Apps | 370 | 51 MB |
| 05-Coding-Webentwicklung | 700 | 54 MB |
| 06-Reisen-Freizeit-Tanzen | 276 | 29 MB |
| 07-Bildung-Webinare-Kurse | 770 | 54 MB |
| 08-Medizin-Wissenschaft | 87 | 7 MB |
| 09-Pflege-Betreuung | 94 | 9 MB |
| 10-Geschichten-Gedichte | 92 | 9 MB |
| 11-KI-Business-Consulting | 729 | 63 MB |
| 12-KI-Tools-Sonstige | 743 | 73 MB |
| 13-Sonstiges | 630 | 61 MB |

## Dateinamen-Schema

```
{laufende_nr}_{kategorie}_{deck-titel-slug}_{bild-index-im-deck}.jpg
00001_katholisch-liturgie_carlo-acutis-heiliger-des-internets_001.jpg
```

## Wichtiger Hinweis zu den Tags

Die Tags im Katalog sind aus dem **Deck-Titel und der Kategorie** abgeleitet (Keyword-Extraktion), **keine** Bildinhalts-Analyse (kein Vision-Tagging). Ein Bild getaggt mit `katholisch;liturgie` zeigt nicht zwangsläufig religiöse Motive — es stammt lediglich aus einem so betitelten/kategorisierten Deck. Enthält auch Theme-Hintergründe/Stock-Fotos neben eigentlichem KI-generiertem Content, da die Quelle (KI vs. Stock vs. Web-Suche) im PDF-Export nicht markiert ist.

## Nutzung

1. Passendes Kategorie-ZIP aus den [Releases](../../releases) laden
2. `katalog.csv`/`.json` zum Filtern/Suchen nach Kategorie, Deck-Titel, Tags oder Maßen nutzen
3. Über `gamma_url` lässt sich jedes Bild auf das Original-Deck zurückverfolgen
