# Automatiserede testresultater

- Ny bruger, ændrede profildata, MitID-annullering, forkert/korrekt PIN, Face ID-fejl, kort og fuldt museswipe, succes, logout, gentaget login, browser-tilbage og genindlæsning: bestået.
- Eksisterende bruger uden onboarding og tilgængelig godkendelsesknap efter oplåsning: bestået.
- Face ID fravalgt → naturlig PIN-vej; tastaturgodkendelse: bestået.
- 360×640, 390×844 og 1440×900: screenshots og kontrol for vandret overflow bestået.
- Webbuild genindlæst og gennemført offline efter aktiveret service worker/cache: bestået.
- Selvstændig HTML åbnet via file:// i offline browser og login gennemført; ingen HTTP-requests: bestået.
- Blokeret localStorage: flow fungerer i hukommelsen.
- Ingen JavaScript-runtimefejl observeret.

Testet i Playwright Chromium på Windows. Fysisk iPhone/Android-installation og enhedstastatur/safe areas kræver manuel kontrol.

- Touch-swipe via Chromium touch-events: kort træk og afbrudt træk går tilbage; fuldt træk godkender. Bestået.
