# Torch Flow One

Statische Landingpage ohne JavaScript, Libraries, externe Fonts, Tracking oder Formulare.

## Branding vor Veröffentlichung

`assets/torch-original.png` enthält das vom Nutzer bereitgestellte originale Logo inklusive Hintergrund. Die Darstellung nutzt CSS `mix-blend-mode: lighten`, um den dunklen Bildhintergrund in die grüne Bühne einzublenden. Die Bilddatei selbst ist unverändert. Für einen späteren transparenten Export kann diese Datei ersetzt und die Blend-Einstellung entfernt werden.

GitHub: https://github.com/torchflowone (im bisherigen Gespräch bestätigt).
X: https://x.com/torchflowone (aus dem bisherigen Branding abgeleitet; vor Veröffentlichung prüfen).
Mail: hello@torchflow.one.

## Lokal ansehen

In diesem Ordner einen statischen Webserver starten, z. B. `python3 -m http.server 8080`, und http://localhost:8080 öffnen.

## GitHub Pages

1. Ein Repository unter `torchflowone` erstellen, zum Beispiel `torchflowone.github.io`.
2. Den Inhalt dieses Ordners einschließlich `.nojekyll` und `CNAME` in dessen Hauptverzeichnis übertragen.
3. Unter Settings → Pages Veröffentlichung vom Branch `main`, Ordner `/ (root)`, wählen.
4. Custom domain auf `torchflow.one` setzen. Die enthaltene CNAME-Datei verwendet dieselbe Domain.
5. Beim DNS-Anbieter die Domain gemäß der aktuellen offiziellen GitHub-Anleitung konfigurieren: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
6. HTTPS aktivieren, sobald das Zertifikat bereitsteht. Logo, Links und Darstellung auf Desktop/Mobile vor dem öffentlichen Teilen prüfen.

Für eine Projekt-URL sind alle Asset-Pfade relativ. Die Domain-Datei erst für das tatsächlich gewünschte Custom-Domain-Deployment übernehmen.

## Sicherheit und Zugänglichkeit

Restriktive Content Security Policy im HTML; keine Skripte, Verbindungen oder Formulare. GitHub Pages unterstützt keine frei konfigurierbaren HTTP-Sicherheitsheader; `frame-ancestors` lässt sich daher hier nicht zuverlässig über einen HTML-Meta-Tag setzen. Neue externe Tabs nutzen `noopener noreferrer`. Animationen respektieren `prefers-reduced-motion`. Logo-Echos sind dekorativ, Links per Tastatur erreichbar.

## 3D-Skulptur

Der Hero verwendet einen KI-generierten 3D-Bildentwurf (`assets/torch-sculpture.png`), keine Echtzeit-3D-Szene und kein Video. Ein inline SVG mit animiertem Displacement-Filter bewegt ausschließlich den zentralen oberen Strahlenbereich. Schale, Griff, Materialfarben und Seitenfackeln bleiben statisch. Bei reduzierter Bewegung wird der Bildfilter deaktiviert. Die Interpretation ist ein 3D-Entwurf des Original-Logos; das Original bleibt als Favicon erhalten.
