Introduksjon til nevrale nettverk
Samling 1 Oppgave


Steg-for-steg
1. Samle datasett

Som gruppe skal dere samle totalt 30 bilder av 2–3 forskjellige verktøy fra prototype-laben.
2. Lag masker (labels)

For hvert bilde skal dere lage en binær maske (hvit = verktøy, svart = bakgrunn). Hvilket verktøy dere bruker for å lage maskene, bestemmer dere selv.
3. Ekstraher features med DinoV3

    Følg eksemplet fra notebooken dere har gått gjennom.
    Kjør segmentering på deres egne bilder.
    Bruk output fra DinoV3 som feature-vektorer.

4. Tren logistisk regresjon

    Bruk features (X) og labels (y) fra maskene.
    Tren en logistisk regresjon til å skille mellom verktøy og bakgrunn.

5. Test modellen

    Bruk nye bilder (som modellen ikke har sett før).
    Prediker maske for disse bildene.
    Visualiser: vis originalbildet og den predikerte masken.




Gruppen har tatt bilde av skrujern, fastnøkkler og sag som ble funnet på verkstedet.

For å kunne trene modellen må vi lage masker (labels) som forteller modellen hvor objektet vi ønsker å gjenkjenne er i bildet.
Masken ble lagd lagret i .png format med der bakgrunnen er gjennomsiktig og modellen er farget helt sort.

Det er viktig at bildet og masken matcher dvs. at masken dekker over objektet når den legges over bildet. De må derfor ha samme oppløsning og være rotert i samme rettning.
Masken ble lagd med GIMP som er et bilderedigeringsprogram. Objektet ble merkert med lassoverktøyet og klippet ut. Det utklippede objektet ble limt inn i nytt lag og farget sort. Orginal bildet ble lagret som .jpg og masken som .png.

For å trene modellen ble det tatt utgangspunkt i jupyter notbooken "foreground_segmentation" som vi så på under web undervisningen. Notbooken ble modifisert slik slik at den kunne trenes med bildene vi hadde tatt. Etter modellen er trent testes den mot alle testbildene i mappen.