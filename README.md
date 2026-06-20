# pieter-vandenkeybus.be

Persoonlijke website van Pieter Van den Keybus — UX- & CX-consultant uit Antwerpen.
Statische single-page site (HTML/CSS), te deployen via GitHub Pages of Vercel.

## Bestanden
- `index.html` — de volledige pagina (inline CSS, geen build nodig)
- `robots.txt` — verwijst naar de sitemap
- `sitemap.xml` — één URL (homepage), hreflang nl-BE

## Deploy
**GitHub Pages:** repo → Settings → Pages → branch `main`, map `/root`. Custom domain `pieter-vandenkeybus.be` instellen, "Enforce HTTPS" aanzetten.
**Vercel:** import repo → framework "Other" → custom domain toevoegen.

## SEO-checklist na deploy
1. Domein koppelen en HTTPS forceren.
2. Property aanmaken in Google Search Console voor `pieter-vandenkeybus.be`.
3. `sitemap.xml` indienen in Search Console.
4. `lastmod` in sitemap.xml updaten bij elke inhoudelijke wijziging.

## Waarom dit geen "duplicate content"-probleem geeft
Google bestraft twee eigen sites niet; het filtert hooguit bijna-identieke pagina's.
Daarom is hier alles bewust onderscheidend gehouden t.o.v. pieter-van-den-keybus.be:
- eigen `canonical` (`https://pieter-vandenkeybus.be/`) — wijst naar zichzelf, niet naar de andere site
- eigen schema `@id`'s op het nieuwe domein
- volledig herschreven teksten, andere structuur (Profiel / Diensten / Werk / Contact) en ander visueel ontwerp
- `sameAs` in de Person-schema linkt beide domeinen + LinkedIn, zodat Google begrijpt dat het om dezelfde persoon gaat (geen spamsignaal)

Tip: voeg op de **andere** site eventueel `https://pieter-vandenkeybus.be` toe aan de `sameAs`-lijst, zodat de koppeling wederzijds is.
