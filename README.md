# weltanschauung.org

Die Website **weltanschauung.org** als statische Seite, ausgeliefert über
GitHub Pages.

## Woher der Inhalt stammt

Momentaufnahme der WordPress-Installation vom 2026-07-25, gezogen bevor die
Seite von Namecheap wegzieht. Sie ist **aufgeräumt, aber noch nicht neu
gestaltet**: Aufbau, Theme und Auszeichnung stammen unverändert aus WordPress.
Der Neubau der Gestaltung steht an.

13 Beiträge, 6 Rubrik- und Strukturseiten, dazu Kategorie-, Stichwort- und
Archivseiten.

## Was gegenüber der WordPress-Fassung entfernt wurde

- **824 Verweise** der Form `?p=<ID>` auf sprechende Pfade umgerechnet — die
  Hauptnavigation I.–V. zeigte dorthin, ein blosses Löschen hätte sie zerlegt
- 18 dadurch überflüssige `?p=`-Duplikatdateien
- `wp-json/` — 105 API-Stummel ohne Funktion in einer statischen Seite
- 611 tote `<link>`-Angaben im `<head>`: RSS-Feeds, oEmbed, RSD, `api.w.org`
- `?ver=`-Anhängsel aus 10 Asset-Dateinamen; solche Namen liefern statische
  Hoster unzuverlässig aus

Geprüft: 6264 lokale Verweise, alle auflösbar. Keine Datei trägt mehr ein `?`
im Namen.

## Lokal ansehen

```bash
python3 -m http.server 8732
# http://127.0.0.1:8732/
```

## Herkunft und Wiederherstellung

Gebaut aus dem originalgetreuen Spiegel im **privaten** Nachbarverzeichnis
`weltanschauung_org/inhalte/`, mit `inhalte/werkzeuge/entruempeln.py`. Dort
liegen auch die Texte als Rohdaten, die vollständige Mediathek und die
Skripte, mit denen alles geholt wurde. Dieses Repository enthält nur die
ausgelieferte Seite.

`.nojekyll` verhindert, dass GitHub die Dateien durch Jekyll schiebt.
