SysML-kielessä **Rakenne (Structure)** on yksi neljästä peruspilarista, joiden avulla järjestelmäinsinöörit kuvaavat ja hallitsevat monimutkaisia kokonaisuuksia. Lähteiden mukaan rakennepilari keskittyy vastaamaan kysymykseen siitä, **mitä** järjestelmä on ja mistä osista se koostuu.

Tässä on kooste siitä, miten rakenne kuvataan näissä lähteissä laajemmassa SysML:n neljän pilarin kontekstissa:

![[Rakenne-1779222287428.webp]]
### 1. [[Rakenteen perusyksikkö]]: Lohko (Block)

Rakenteen atomistinen perusyksikkö on **lohko (block)**. Lohko on käsitteellinen "rakennuspalikka", joka edustaa järjestelmän osaa, jolla on tiettyjä ominaisuuksia, arvoja ja hierarkkisia suhteita muihin osiin. Lohkot toimivat "sinikopioina" tai blueprintteinä järjestelmän komponenteille.

### 2. Rakenteen kaksi näkökulmaa: Määrittely ja käyttö

Rakennetta tarkastellaan lähteissä kahdesta toisiaan täydentävästä näkökulmasta:

- **Määrittely (Definition):** Käytetään **lohkomäärittelykaaviota (BDD)**, joka kuvaa järjestelmän hierarkian ja luokittelut. Se näyttää, mistä osista järjestelmä koostuu (koostumussuhde) ja miten eri lohkot perivät ominaisuuksia toisiltaan (yleistyssuhde).
- **Käyttö (Usage):** Käytetään **sisäistä lohkokaaviota (IBD)**, joka näyttää, miten lohkon sisäiset osat on kytketty toisiinsa tietyssä kontekstissa. IBD keskittyy osien välisiin rajapintoihin (**portit**) ja siihen, mitä niiden välillä virtaa (**liittimet** ja **item flow**).

### 3. Rakenne osana neljää pilaria

Rakennepilari ei toimi eristyksissä, vaan se on ankkuri, johon muut pilarit kiinnittyvät:

- **Käyttäytyminen (Behavior):** Käyttäytyminen kuvaa järjestelmän toiminnan ("miten"). Lähteiden mukaan käyttäytymismallit, kuten aktiviteetit, **kohdennetaan (allocate)** rakenteellisille osille, jotka ovat vastuussa kyseisen toiminnon suorittamisesta. Esimerkiksi sekvenssikaavioissa esiintyvien elämänviivojen on vastattava rakennemallissa määriteltyjä elementtejä.
- **Vaatimukset (Requirements):** Rakenteellisten lohkojen katsotaan **toteuttavan (satisfy)** järjestelmälle asetetut vaatimukset. Requirement-kaavioiden avulla vaatimukset linkitetään suoraan niihin rakenteen osiin, joiden on ne täytettävä.
- **Parametriikka (Parametrics):** Tämä pilari sitoo matemaattiset yhtälöt rakenteen ominaisuuksiin ja arvoihin. Parametriset kaaviot yhdistävät rajoitukset (constraints) lohkojen ominaisuuksiin, mikä mahdollistaa suorituskyvyn analysoinnin.

### 4. Muut rakenteelliset kaaviot

Vaikka BDD ja IBD ovat keskeisimmät, SysML-standardi lukee rakenteellisiin kaavioihin myös:

- **Pakkauskaavion (Package diagram):** Mallin organisointiin.
- **Vaatimuskaavion (Requirement diagram):** Vaatimushierarkioiden kuvaamiseen (vaikka se on oma pilarinsa, se on taksonomialtaan rakenteellinen).
- **Parametrisen kaavion (Parametric diagram):** Arvoihin liittyvien rajoitteiden kuvaamiseen.

Yhteenvetona rakenne muodostaa **järjestelmän rungon**, joka mahdollistaa monimutkaisuuden hallinnan jakamalla järjestelmän hierarkkisiin osiin ja määrittelemällä niiden väliset yhteydet, joihin toiminnallisuus, vaatimukset ja laskennalliset analyysit kiinnittyvät.