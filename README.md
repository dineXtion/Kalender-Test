# VR-Infotainment Kalender

Dieser Prototyp zeigt die Öffnungstage der VR-Infotainment Ausstellung 2025 samt Live-Kontingenten für Ticketbuchungen.

## Features

- Responsiver Monatskalender (Januar–Dezember 2025)
- Wochenend- und Feiertagslogik für geöffnete Tage
- Automatisches Laden der Ticketkontingente direkt von *ticket-regional.de*
- Farb- und Statuskennzeichnung für verfügbare, ausverkaufte und vergangene Termine
- Optionaler CORS-Proxy für Umgebungen, in denen der direkte Abruf blockiert wird

## Nutzung

1. Öffnen Sie `index.html` im Browser.
2. Navigieren Sie über die Pfeiltasten zwischen den Monaten.
3. Klicken Sie auf markierte Tage, um direkt zur Buchungswoche bei ticket-regional.de zu gelangen.
4. Die Ticketkontingente werden nach dem Laden des Kalenders automatisch ergänzt.

> **Hinweis:** Einige Browser blockieren Cross-Origin-Anfragen zu ticket-regional.de. Tragen Sie in `index.html` oben im Skript optional einen CORS-Proxy ein, z. B.:
>
> ```js
> const CORS_PROXY = "https://cors.isomorphic-git.org/";
> ```
>
> Der Proxy muss mit einem abschließenden Slash konfiguriert werden.

## Entwicklung

- Die Kalenderdaten (URL je Kalenderwoche, Feiertage, letzter Öffnungstag) werden im Skript (`index.html`) gepflegt.
- Ticketdaten werden einmal pro Kalenderwoche geladen und im Speicher gecacht.
- Das HTML/CSS/JS ist komplett statisch; ein beliebiger Webserver oder lokale Dateiansicht genügt.

Viel Erfolg beim Testen! 🎫
