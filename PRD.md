# PRD: Edunvalvonnan Mediaseuranta-Dashboard
## Tampereen Kauppakamari x Aava & Bang AI

**Versio**: 0.1 (Ideointi)
**Paivamaara**: 2026-03-05
**Asiakas**: Tampereen Kauppakamari, Edunvalvontayksikko

---

## 1. Tausta ja tavoite

Tampereen Kauppakamarin edunvalvontayksikko tarvitsee tyokalun, joka kokoaa automaattisesti eri medioista edunvalvontaa koskevat mediaosumat yhteen nakymaan. Tama saastaa manuaalista mediaseurantatyota ja varmistaa, etta olennaiset julkaisut eivat jaa huomaamatta.

**Tavoite**: AI-pohjainen media-dashboard, joka:
- Kerailee mediahitteja useista lahteista automaattisesti
- Pisteyttaa ne relevanssin ja tarkeyden mukaan
- Tarjoaa selkean kokonaisnakyman edunvalvonnan mediakenttaan
- Mahdollistaa nopean reagoinnin olennaisiin julkaisuihin

---

## 2. Kohderyhmäa ja kayttajat

| Kayttajarooli | Tarve |
|---|---|
| Edunvalvontapaallikko | Paivan kokonaiskuva, trendit, tarkeimmat hitit |
| Edunvalvonta-asiantuntija | Yksittaisten osumien syvempi tarkastelu, reagointi |
| Kauppakamarin johto | Viikko-/kuukausitason raportit, strateginen nakyma |

---

## 3. Tietolahteet

### 3.1 Perinteiset mediat
- **Verkkolehdet**: Aamulehti, Yle Tampere, Helsingin Sanomat, Kauppalehti, Talouselama
- **Paikallismediat**: Tamperelainen, Tredea-uutiset, maakuntalehdet
- **Toimialajulkaisut**: Kauppakamari.fi, EK, Keskuskauppakamari

### 3.2 Sosiaalinen media
- **LinkedIn**: Avainhenkiloiden ja organisaatioiden postaukset
- **X.com (Twitter)**: Keskustelut, kannanotot, uutisjaot
- **Threads**: Kasvava alusta julkiseen keskusteluun
- **Facebook**: Ryhmat ja sivut (valinnainen)

### 3.3 Viralliset lahteet
- **Eduskunta**: Lakialoitteet, valiokuntien poytakirjat, kirjalliset kysymykset
- **Valtioneuvosto**: Tiedotteet, saadoshankkeet
- **EU**: Asetukset ja direktiivit jotka koskevat elinkeinoelaman etuja
- **Tampereen kaupunki**: Kaupunginvaltuuston paatokset, kaavoitus

### 3.4 Muut lahteet
- **Blogit ja kolumnit**: Mielipidekirjoitukset, asiantuntija-analyysit
- **Podcastit/videot**: Transkriptiot relevanteista jaksoista (valinnainen)
- **RSS-syyotteet**: Konfiguroitavat

---

## 4. Dashboard-nakymat

### 4.1 Paanakyma (Daily Brief)
Ensimmainen asia jonka kayttaja nakee kirjautuessaan:

- **Paivan yhteenveto (AI-generoitu)**
  - 3-5 lauseen tiivistelma paivan olennaisimmista tapahtumista
  - Tyylin esimerkki: "Tanaan hallitus julkaisi esityksen yritysverotuksen uudistamisesta. Aamulehti uutisoi Tampereen raitiotien laajennuksen rahoituksesta. LinkedIn-keskustelussa korostui tyovoimapula..."

- **Top 10 mediahitit** (pisteytettyna)
  - Otsikko, lahde, julkaisuaika
  - Relevanssipistemäara (1-100)
  - Sentimentti-indikaattori (positiivinen/neutraali/negatiivinen)
  - Aiheluokitus (tagi)
  - Nopeat toiminnot: Avaa, Jaa, Merkitse luetuksi, Lisaa seurantaan

- **Trendikartta**
  - Reaaliaikainen aihekartta: mista puhutaan nyt
  - Nousevat aiheet (trending up)
  - Hiipuvat aiheet (trending down)

- **Aktiivisuusmittari**
  - Mediaosumien maara: tanaan vs. edellinen paiva/viikko
  - Kaavio: osumien maara per tunti/paiva

### 4.2 Aihenakyma (Topic Deep Dive)
Kayttaja voi porautua yksittaiseen aiheeseen:

- **Aihekohtainen aikajana**: Kaikki osumat kronologisessa jarjestyksessa
- **Sentimenttianalyysi**: Miten mielipideilmasto muuttuu ajan myota
- **Avainhenkilot**: Ketka puhuvat tasta aiheesta eniten
- **Lahdejanalyysi**: Mista medioista osumat tulevat
- **AI-yhteenveto**: Automaattinen tiivistelma aiheesta ja sen kehityksesta
- **Liittyvat aiheet**: Mihin muihin teemoihin aihe kytkeytyy

### 4.3 Lahdenakyma (Source View)
Nakyma per medialahde:

- **Lahdekohtainen syote**: Kaikki osumat yhdesta lahteesta
- **Lahteen luotettavuusarvio**: Kuinka usein lahde tuottaa relevantteja osumia
- **Lahteen aktiivisuus**: Julkaisutahti, aihejakauma

### 4.4 Henkilonakyma (People & Organizations)
Seurattavien avainhenkiloiden ja organisaatioiden nakyma:

- **Henkiloprofiilit**: Kansanedustajat, ministerit, kunnanvaltuutetut, elinkeinojohtajat
- **Organisaatioprofiilit**: Ministeriöt, virastot, etujärjestöt
- **Aktiivisuusseuranta**: Milloin ja missa henkilö/org on maininnut relevantteja aiheita
- **Verkostokartta**: Kuka puhuu kenesta, miten aiheet leviaavat

### 4.5 Raporttinäkyma (Reports)
Automaattiset raportit eri aikavaileille:

- **Viikkoraportti**: AI-generoitu yhteenveto viikon tapahtumista
- **Kuukausiraportti**: Trendit, tarkemmat analyysit, strategiset havainnot
- **Kvartaaliraportti**: Isot linjat, pitkän aikavalin trendit
- **Raporttigeneraattori**: Kayttaja valitsee aikavalin, aiheet, lahteet → PDF/PPTX

---

## 5. AI-ominaisuudet

### 5.1 Alykäs pisteytys (Smart Scoring)
Jokainen mediaosuma pisteytetaan automaattisesti:

| Kriteeri | Paino | Kuvaus |
|---|---|---|
| Aiherelevanssi | 30% | Kuinka lahella edunvalvonnan ydinalueita |
| Lahteen painoarvo | 20% | Median tavoittavuus ja vaikuttavuus |
| Ajankohtaisuus | 15% | Tuoreus, uutisarvo |
| Sentimentti | 10% | Positiivinen/negatiivinen vaikutus elinkeinoille |
| Leviamispotentiaali | 15% | Todennakoisyys etta aihe kasvaa |
| Toimenpidepotentiaali | 10% | Vaatiiko reagointia kauppakamarilta |

### 5.2 Automaattiset halytykset (Smart Alerts)
- **Kriittinen halytys**: Aihe joka vaatii välitöntä reagointia (esim. lakimuutos)
- **Tarkea halytys**: Merkittava mediahitti tai nouseva trendi
- **Info-halytys**: Mielenkiintoinen mutta ei kiireellinen
- **Kanavat**: Email, push-notifikaatio, Teams/Slack-integraatio

### 5.3 AI-assistentti (Chat)
Dashboard-sisainen AI-chatti:
- "Tiivista viime viikon tapahtumat koskien yritysverotusta"
- "Miten Tampereen raitiotie-keskustelu on kehittynyt kuukauden aikana?"
- "Ketka kansanedustajat ovat puhuneet eniten tyovoimapulasta?"
- "Laadi vastine tanaan julkaistuun mielipidekirjoitukseen"

### 5.4 Ennakoiva analyysi (Predictive)
- **Aihe-ennusteet**: Mitkä aiheet tulevat kasvamaan lahiviikkoina
- **Reagointisuositukset**: AI ehdottaa toimenpiteita (kannanotto, tiedote, some-viesti)
- **Vaikuttavuusanalyysi**: Kuinka kauppakamarin omat viestit ovat vaikuttaneet mediakeskusteluun

---

## 6. Aihealueet ja luokittelu

### 6.1 Edunvalvonnan ydinaiheet
- **Verotus**: Yritysverotus, kuntaverot, alv-muutokset
- **Tyovoima**: Tyovoimapula, koulutus, maahanmuutto, tyoluvat
- **Liikenne ja infra**: Raitiotie, tieyhteydet, lentoyhteydet, logistiikka
- **Kaavoitus ja maankaytto**: Yritystonttien saatavuus, keskustan kehitys
- **Saately ja byrokratia**: Lupaprosessit, saadosmuutokset
- **Elinvoima**: Investoinnit, yrityshankkeet, startup-ekosysteemi
- **Energia**: Energiapolitiikka, puhdas siirtyma, sahkon hinta
- **Koulutus**: Ammatillinen koulutus, korkeakoulut, osaajien houkuttelu
- **Turvallisuus**: Huoltovarmuus, kyberturvallisuus
- **EU-asiat**: Saately, kauppapolitiikka, rahoitus

### 6.2 Maantieteellinen fokus
- **Ensisijainen**: Pirkanmaa, Tampere
- **Toissijainen**: Kansallinen taso
- **Kolmas taso**: EU ja kansainvalinen

---

## 7. Toiminnallisuudet

### 7.1 Haku ja suodatus
- Vapaa tekstihaku kaikista osumista
- Suodatus: aihe, lahde, ajankohta, sentimentti, pistemäara
- Tallennetut haut ja hakuhalytykset
- Boolean-haku edistyneille kayttajille

### 7.2 Merkinta ja organisointi
- Omien tagien lisaaminen osumiin
- Kokoelmat: ryhma aiheeseen liittyvat osumat yhteen
- Kommentointi: sisainen keskustelu osumista
- Tehtavat: "Valmistele kannanotto" → linkitys osumaan

### 7.3 Jakaminen ja viestinta
- Jaa osuma tai raportti suoraan sahkopostilla
- Koosta uutiskirje valituista osumista (sisainen/ulkoinen)
- Integroi Teams/Slackiin: automaattiset viestit kanavalle
- Social media -vastineen luonti AI-avusteisesti

### 7.4 Kayttajahallinta
- Roolipohjainen kayttohallinnointi (admin, asiantuntija, lukija)
- Henkilokohtaiset asetukset: suosikit, halytysasetukset
- Kayttologit ja tilastot: kuka kayttaa mita

### 7.5 Dashboardin muokkaus
- Widgettipohjaisuus: kayttaja voi muokata omaa nakymaa
- Useat dashboard-nakymat eri tarpeisiin
- Aiheseurannan konfigurointi: lisaa/poista seurattavia aiheita ja avainsanoja

---

## 8. Pisteytyslogiikka (tarkemmin)

### Media-hitin elinkaari:
```
1. Kerays     → Lahteesta poimittu raakadata
2. Luokittelu → AI tunnistaa aiheen, henkilot, organisaatiot
3. Pisteytys  → Relevanssipistemäara lasketaan
4. Rikastus   → Sentimentti, NER, yhteenvedot
5. Halytys    → Jos pistemäara ylittaa kynnyksen
6. Naytto     → Dashboardilla oikeassa paikassa
```

### Pisteytysesimerkki:
```
Osuma: "Hallitus esittaa yritysverotuksen kiristysta"
  - Aiherelevanssi:        95/100  (verotus = ydinaihe)
  - Lahteen painoarvo:     85/100  (Helsingin Sanomat)
  - Ajankohtaisuus:        100/100 (juuri julkaistu)
  - Sentimentti:           80/100  (negatiivinen elinkeinoille = kiinnostava)
  - Leviamispotentiaali:   90/100  (hallituksen esitys = iso uutinen)
  - Toimenpidepotentiaali:  95/100 (vaatii kannanottoa)
  → Kokonaispistemäara:    91/100 → KRIITTINEN
```

---

## 9. Halytystasot

| Taso | Pistemäara | Toiminto | Esimerkki |
|---|---|---|---|
| Kriittinen | 85-100 | Välitön push + email | Lakimuutos joka vaikuttaa yrityksiin |
| Tarkea | 65-84 | Email-kooste 2x/pv | Merkittava mediakirjoitus aiheesta |
| Normaali | 40-64 | Nakyy dashboardilla | Tavallinen uutisointi relevantti aihe |
| Matala | 0-39 | Arkistoidaan | Sivumaininta, vanha aihe |

---

## 10. Tekniset nakokulmat (korkean tason)

### Arkkitehtuuri
- **Frontend**: Moderni SPA (React/Next.js)
- **Backend**: API-palvelin keraykseen ja prosessointiin
- **AI-kerros**: LLM luokitteluun, tiivistelyyn, pisteyttamiseen
- **Tietokanta**: Osumien tallennus ja haku
- **Ajastimet**: Lahdekerays 15min–1h valein

### Integraatiot
- Uutissyotteet (RSS/Atom)
- Sosiaalisen median API:t (LinkedIn, X, Threads)
- Eduskunnan avoin data
- Valtioneuvoston hankeikkuna
- Email-lahetys (SMTP/API)
- Teams/Slack webhookit

---

## 11. Mockup-prioriteetit

HTML-mockupia varten priorisointi:

### P1 - Ensimmainen demo
1. **Paanäkymä**: AI-yhteenveto + Top 10 lista + trendikartta
2. **Yksittaisen osuman kortti**: Pisteytys, sentimentti, tagit, toiminnot
3. **Halytykset**: Kriittinen-bannerit

### P2 - Toinen demo
4. **Aihenakyma**: Aihekohtainen porautuminen
5. **Raporttinäkyma**: Viikkoraportin esikatselu
6. **AI-chatti**: Interaktiivinen kyselynäkymä

### P3 - Kolmas demo
7. **Henkilonakyma**: Avainhenkiloiden seuranta
8. **Asetukset**: Aihe- ja lahdemaarittely
9. **Verkostokartta**: Visuaalinen verkostonäkymä

---

## 12. Mittarit (KPI)

### Palvelun onnistumisen mittarit
- Kuinka monta relevanttia osumaa loydetaan vs. manuaalinen seuranta
- Reaktioaika: kuinka nopeasti kriittinen aihe huomataan
- Kayttajatyytyväisyys (NPS/CSAT)
- Kayttoaste: päivittäiset/viikoittaiset aktiiviset kayttajat

---

## 13. Riskit ja avoimet kysymykset

| Riski | Vaikutus | Mitigaatio |
|---|---|---|
| Some-API-rajoitukset | LinkedIn/X ei tarjoa helposti dataa | Vaihtoehtoiset keraystavat, kumppani-API:t |
| AI-pisteytyksen tarkkuus | Vaarat halytykset/puuttuvat osumat | Kayttajapalautesilmukka, jatkuva viritys |
| Tietosuoja (GDPR) | Henkilötietojen kasittely | Juridinen arviointi, minimointiperiaate |
| Lahdemateriaali tekijanoikeus | Uutissisallön jakaminen | Vain otsikot + tiivistelmat, linkit lahteisiin |
| Skaalautuvuus | Osumien maara kasvaa → hidas | Arkistointi, indeksointi, caching |

---

## 14. Kehitysideat (V2+)

### 14.1 Datan kerays ja lahteet

- **Kuntapaatokset**: Tampereen kaupungin esityslistat ja poytakirjat automaattisesti parseroidaan — nama ovat edunvalvonnalle kultaa, koska ne tulevat usein ennen mediaa
- **Lakihankkeet (lausuntokierrokset)**: lausuntopalvelu.fi -integraatio — halytys kun uusi lausuntopyynto liittyy edunvalvonnan aiheisiin, ja deadline-muistutus
- **Hankeikkuna**: Valtioneuvoston hankeikkuna-API seuraamaan saadosvalmisteluhankkeiden etenemista
- **Podcast-transkriptiot**: Politiikka- ja talouspodcastien automaattinen transkriptointi ja analyysi (esim. Politiikkaradio, Taloussanomat-podcast)
- **Kilpailevat kauppakamarit**: Mita muut kauppakamarit viestivat samoista aiheista — benchmarking

### 14.2 AI-ominaisuudet

- **Vaikuttavuusanalyysi**: Seuraa miten kauppakamarin omat kannanotot ja tiedotteet vaikuttavat mediakeskusteluun — nakyykö kauppakamarin viesti myohemmin median uutisoinnissa tai poliitikkojen puheissa
- **Vastine-generaattori**: AI laatii vastineluonnoksen suoraan mediahittiin pohjautuen — osaa viitata kauppakamarin aiempiin kannanottoihin ja dataan
- **Aihe-ennusteet**: Ennakoi tulevia aiheita eduskunnan kalenterin, EU:n lainsaadantoaikataulujen ja hallitusohjelman perusteella — "ensi viikolla kasittelyssa X, valmistaudu"
- **Argumenttipankki**: AI kokoaa ja yllapitaa aihealueittain parhaita argumentteja, tilastoja ja esimerkkeja joita edunvalvonnassa voi kayttaa
- **Media-briefing aamulla**: Automaattinen aamubrief sahkopostiin tai Teamsiin klo 7 — tiivistelma yon tapahtumista + paivan odotettavissa olevat aiheet

### 14.3 Toiminnallisuudet

- **Reagointiputki**: Mediaosumasta suoraan tyonkulkuun — "Laadi kannanotto" → AI-luonnos → hyvaksynta → julkaisu kauppakamarin kanavissa
- **Sidosryhmakartta**: Kuka paattaa mistakin — kansanedustajat valiokunnittain, ministerit vastuualueineen, virkahenkilot. Kun aihe nousee, nayttaa suoraan keihin pitaisi olla yhteydessa
- **Kampanjaseuranta**: Jos kauppakamari ajaa tiettya asiaa (esim. raitiotien rahoitus), oma dashboard-nakyma joka seuraa kampanjan etenemista, mediapeittoa ja vaikuttavuutta
- **Vertailukaupungit**: Miten Tampere nakyy suhteessa Turkuun, Ouluun, Lahteen — kilpailevien alueiden elinvoimakeskustelu
- **Jasenyritysten mediaseuranta**: Lisapalveluna kauppakamarin jasenyrityksille oma mediaseurantanakyma — lisaarvoa jasenyydelle

---

## 15. Seuraavat askeleet

1. [x] Kayda PRD lapi asiakkaan kanssa, keraa palaute
2. [ ] Priorisoi ominaisuudet MVP:ta varten
3. [x] Rakenna HTML-mockup P1-ominaisuuksilla
4. [ ] Esittely Tampereen Kauppakamarille
5. [ ] Teknisen toteutuksen suunnittelu
