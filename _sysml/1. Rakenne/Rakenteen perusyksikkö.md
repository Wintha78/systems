

**SysML‑lohko on järjestelmän rakenteen perusyksikkö**, joka toimii _tyyppinä_ (BDD) ja _instanssina_ (IBD). <mark style="background:#affad1">Se kokoaa yhteen ominaisuudet, rajapinnat, käyttäytymisen kohdennukset ja vaatimukset</mark>. Lohko on se “paikka”, johon kaikki muu SysML‑mallinnustieto ankkuroituu.

### 1. Lohkon kaksi puolta: Määrittely ja käyttö

SysML käsittelee rakennetta lohkojen kautta kahdesta toisiaan täydentävästä näkökulmasta:
![[Rakenteen perusyksikkö-1779222471708.webp]]

- **Määrittely (Definition):** Käytetään **lohkomäärittelykaaviota (BDD)**, joka vastaa kysymykseen: _"Mitä osia järjestelmässä on?"_. BDD:ssä lohkot määritellään tyyppeinä (kuten "antilock controller"), ja niiden välille luodaan hierarkioita, kuten **koostumussuhteita** (musta timantti) ja **yleistyksiä** (valkoinen kolmio).

**Musta timantti** — _“Omistan tämän osan täysin.”_

- Osa **ei voi kuulua muualle**.
- Osa **ei voi elää ilman kokonaisuutta**.
- Osa **tuhoaa** kokonaisuuden mukana.
    
- SysML:ssä tämä on **koostumus**, ja se muodostaa järjestelmän **osaluettelon**.

**Valkoinen timantti** — _“Tämä on osa minua, mutta ei omistuksessani.”_

- Osa **voi kuulua useaan kokonaisuuteen**.
- Osa **voi elää ilman kokonaisuutta**.
- Ei omistajuutta, vain “on osa” ‑suhde.
- SysML:ssä tätä käytetään harvoin, koska järjestelmämallinnuksessa omistajuus on yleensä selkeä.
----------

- **Käyttö (Usage):** Käytetään **sisäistä lohkokaaviota (IBD)**, joka tarkastelee lohkon sisäpuolta. Se näyttää, miten lohkon sisältämät osat (jotka ovat lohkotyyppien instansseja) on kytketty toisiinsa **liittimillä** ja **porteilla**, jotka kuvaavat osien välisiä rajapintoja ja virtoja.

![[Rakenteen perusyksikkö-1779222940322.webp]]
IBD:ssä on kolme keskeistä rakennetta:

1. **Portit** – lohkon rajapintapisteet
2. **Liittimet** – yhteydet porttien tai osien välillä
3. **Virrat** – data, energia tai materia, joka kulkee liittimien kautta


### 2. Lohkon sisäinen anatomia

Lohko toimii säiliönä erilaisille piirteille, jotka kuvaavat sen ominaisuuksia ja toimintaa:

- **Ominaisuudet (Properties):** Lohkolla on ominaisuuksia, kuten **osa-ominaisuuksia** (part properties, jotka kuvaavat koostumusta), **viiteominaisuuksia** (reference properties, jotka kuvaavat assosiaatioita muihin lohkoihin) ja **arvo-ominaisuuksia** (value properties, kuten massa, lämpötila tai hinta).
- **Toiminnot (Operations):** Nämä kuvaavat, mitä lohko tekee, eli sen suoritettavissa olevaa käyttäytymistä.

### 3. Lohko järjestelmämallin ankkurina

Lohko on rakenteellinen runko, johon kaikki SysML:n muut pilarit kytkeytyvät:

- **Käyttäytyminen (Behavior):** Käyttäytymismallit, kuten aktiviteetit tai tilakoneet, **kohdennetaan (allocate)** lohkoille tai niiden osille, jotka ovat vastuussa kyseisen toiminnon suorittamisesta.
- **Vaatimukset (Requirements):** Lohkon katsotaan **toteuttavan (satisfy)** sille asetetut vaatimukset. Esimerkiksi jarrunohjain-lohko toteuttaa sille asetetut suorituskykyvaatimukset.
- **Parametriikka (Parametrics):** Lohkojen sisältämät arvo-ominaisuudet kytketään matemaattisiin yhtälöihin parametrisissa kaavioissa, mikä mahdollistaa järjestelmän suorituskyvyn ja rajoitteiden analysoinnin.

### Yhteenveto

Lohko on lähteiden mukaan järjestelmän "rakennuspalikka", joka antaa rakenteellisen kontekstin kaikelle muulle mallinnustiedolle. Se mahdollistaa monimutkaisen järjestelmän purkamisen hallittavaan **osaluetteloon** (hierarkiaan) ja varmistaa, että järjestelmän osat, niiden väliset kytkennät, toiminnot ja vaatimukset ovat keskenään johdonmukaisia.