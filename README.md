# IdrætsID – studieprototype

Mobilførst, interaktiv mockup med HTML, CSS, Vanilla TypeScript og Vite. Storyboardet i brugerens første besked er den primære visuelle reference. Præsentationen var ikke tilgængelig i projektmappen, og brugeren bad derefter om at følge storyboardet alene.

## Kør og byg

Node.js 20.19+ eller 22.12+. `npm install`, derefter `npm run dev`. `npm run typecheck` kontrollerer TypeScript. `npm run build` bygger **dist/**, **release/idraetsid-demo.html** og **release/idraetsid-mockup.zip** fra samme kilde. `npm run preview` viser webbuild. `npx playwright install chromium` installerer testbrowseren. `npm test` kører browserkontroller og opdaterer screenshots; kør build igen for at pakke de nyeste screenshots i ZIP.

## Struktur og demotilstand

`src/main.ts`: demodata samlet i DEMO, State/Request-typer, skærme og handlinger. `src/style.css`: responsivt design. `scripts/build.mjs`: Vite-builds, lokale appikoner, versionscache og ZIP. `tests/flow.mjs`: automatiserede kontroller. `BRUGERVEJLEDNING.md`: deling og mobilinstallation.

Kun profiloplysninger og demoopsætning gemmes under `idraetsid-study-v1`. PIN gemmes aldrig; loginanmodninger, oplåsning og godkendelse lever i hukommelsen. Genindlæsning viser en fungerende klubside, hvor en ny anmodning kan startes. Browserens tilbageknap fjerner oplåsningen, så swipe kræver ny oplåsning. Lagringsfejl ignoreres, og appen fungerer i hukommelsen.

## Assets og begrænsninger

Alle assets er lokale. IdrætsID-symbolet er en forenklet SVG-fortolkning af referencebilledet, klubmærket en tekstbaseret erstatning, og heroen en CSS-illustration af en fodboldspiller. De er ikke officielle logo-/fotoassets. Der bruges systemfonte. Ingen rigtig autentifikation, kontooprettelse eller eksterne systemer. Markedsføringsvalget er valgfrit og sendes/gemmes ikke.

Webudgaven er klar til statisk HTTPS-hosting, også i undermapper. Service worker registreres kun i sikre webmiljøer og aldrig fra file://. Egen cache indeholder alle flowets filer. HTML-udgaven indeholder alt inline.

## Test og manuel kontrol

Se `TESTRESULTATER.md` for udførte tests. Screenshots er i `screenshots/`. Desktopbrowserens mobilviewports dokumenterer layout og touch-events, ikke installation på en fysisk iPhone. Manuel kontrol resterer: host på HTTPS, installer på fysisk iPhone/Android, genåbn fra hjemmeskærmen og kontroller offlinebrug samt tastatur/safe areas. Intet er publiceret.

Skærmoversigten under appen viser alle 16 hoved- og underskærme. Scroll vandret, og klik på et kort for at indlæse trinnets demotilstand. Piletaster, Home/End og Enter kan også bruges. Valget kan simulere en allerede oplåst eller godkendt anmodning til præsentation; en ny anmodning kræver stadig ny oplåsning.
