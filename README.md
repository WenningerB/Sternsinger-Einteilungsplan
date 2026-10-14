# Sternsingen Rain am Lech – GitHub Pages Vorlage

## Enthalten
- `index.html`, `style.css`, `app.js`: Web-App mit 10 Gebieten, Adresslisten, Kartenpunkten und manuell zeichnbaren farbigen Straßenlinien.
- Kartenhintergrund OpenStreetMap. Die Karte startet in Rain am Lech.
- Standortfunktion über HTTPS und Browser-Freigabe.
- JSON-Export/Import als einfache Sicherung.

## Wichtig vor dem echten Einsatz
Diese erste Version ist ein **bearbeitbarer Prototyp**. Die Straßenfarben wurden nicht automatisch aus dem Foto übernommen, weil das Foto keine präzisen Straßengeometrien liefert. Öffne die Verwaltung, wähle ein Gebiet und aktiviere „Straßenlinie zeichnen“. Klicke entlang der richtigen Straße, um die farbige Linie zu zeichnen. Für Hausmarkierungen: Adresse anlegen und anschließend im Verwaltungsmodus auf die richtige Kartenstelle klicken; der nächste Eintrag ohne Kartenpunkt wird dort platziert.

**Noch keine gemeinsame Online-Datenbank:** Aktuell speichert die App in `localStorage` des jeweiligen Browsers. Die Änderungen erscheinen daher nicht automatisch auf anderen Geräten. Für die öffentliche Nutzung muss eine Datenbank und eine sichere Admin-Anmeldung ergänzt werden (z. B. Supabase mit Row Level Security). Keine Passwörter oder geheimen Schlüssel in die GitHub-Dateien schreiben.

## Auf GitHub Pages veröffentlichen
1. Entpacke die ZIP-Datei.
2. Erstelle ein GitHub-Repository, z. B. `sternsingen-rain`.
3. Lade `index.html`, `style.css`, `app.js` und `README.md` ins Hauptverzeichnis hoch.
4. GitHub: **Settings → Pages → Deploy from a branch → main → /(root) → Save**.
5. Warte, bis GitHub die veröffentlichte URL anzeigt.

## Grenzen / Hinweise
- Das Straßenmaterial stammt von OpenStreetMap, nicht direkt vom BayernAtlas.
- Für BayernAtlas-Einbindung und exakte Gebietsgeometrien muss die passende Kartenfreigabe/Technik geprüft werden.
- Adresseingabe platziert den Marker nicht automatisch per Geocoding. Der Marker wird manuell auf die Karte gesetzt.
- Die „Verwaltung“-Schaltfläche ist in diesem Prototyp **keine Zugangssperre**. Vor Veröffentlichung muss Admin-Login/Berechtigung ergänzt werden, damit nur die verantwortliche Person Änderungen durchführen kann.
