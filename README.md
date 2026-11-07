# Reisefieber – Rechtstexte

Die öffentlichen Seiten zur iPhone-App **Reisefieber – Reise-Countdown**:
Datenschutzerklärung, Impressum und Support.

Apple verlangt in App Store Connect eine öffentlich erreichbare
Datenschutz-URL und eine Support-URL. Diese Seiten erfüllen das.

## Nicht von Hand bearbeiten

Die HTML-Dateien werden **erzeugt**, nicht geschrieben. Einzige Quelle ist
`Reisefieber/Views/Legal/LegalTexts.swift` im App-Projekt – damit stehen in
der App und im Web garantiert dieselben Texte.

Nach jeder Änderung am Rechtstext in der App:

```bash
cd ios
python3 werkzeuge/rechtstexte-export.py
cd web && git add -A && git commit -m "Rechtstexte aktualisiert" && git push
```

Eine Änderung direkt an den HTML-Dateien geht beim nächsten Export verloren.

## Inhalt

| Datei | Zweck |
|---|---|
| `index.html` | Startseite mit Verweisen |
| `datenschutz.html` | Datenschutzerklärung – **URL für App Store Connect** |
| `impressum.html` | Impressum nach § 5 DDG |
| `support.html` | Hilfe und Kontakt – **URL für App Store Connect** |
| `.nojekyll` | schaltet die Jekyll-Verarbeitung von GitHub Pages ab |

## Warum nur diese Seiten im Repository liegen

Dieses Repository ist öffentlich, weil GitHub Pages das im Gratis-Tarif
verlangt. Es enthält **bewusst nicht** den Quellcode der App und **nicht**
das Bildmaterial: Die Titelbilder und der Markenauftritt gehören dem
Reisebüro, und was hier liegt, ist für jeden abrufbar.
