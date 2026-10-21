# passtheglass-site

De website van [Pass the Glass](https://apps.apple.com/nl/app/pass-the-glass/id6819401169): https://passtheglass.app,
via GitHub Pages. Het domein staat bij Cloudflare (DNS only, geen proxy).

- `index.html` en `en/`: de app-pagina. `privacy/` en `en/privacy/`: het privacybeleid.
- `wijnbox/` en `en/wine-box/`: de wijnbox als dienst van QURK voor wijnhandels (NL en EN), met een voorbeeld-QR-code. `voorbeeld.txt`/`example.txt` en de etiketten blijven staan: de QR-code verwijst ernaar.
- `style.css`: de kleuren van de app, licht en donker.

De QR-codes (`voorbeeld-qr.png`, `example-qr.png`) wijzen naar het adres van de voorbeeldbestanden. Bij een ander
domein moeten ze opnieuw gemaakt worden.
- `box/<naam>/`: één pagina per wijnbox, het adres in de QR-code. Bevat de box (verborgen, voor de app) en toont per
  toestel iets anders: iPhone → App Store, andere telefoon → straks de webapp, computer → QR-code. `noindex`.
  `box/voorbeeld/` is de voorbeeldbox; `qr.png` ernaast wijst naar de pagina zelf.
- `.well-known/apple-app-site-association`: koppelt `/box/*` aan de app (Universal Links, vanaf app 1.6).
