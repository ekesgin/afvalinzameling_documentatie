# Productinhoud loopafstand pand

| attribuut                | datatype                       | omschrijving                                                                                                                            | domein                                                                                                                                                 |
|--------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| object_id                | character varying              | landelijk identificerend kenmerk pand                                                                                                   |                                                                                                                                                        |
| bag_object_type          | character varying              | type bagobject                                                                                                                          | {pand, ligplaats, standplaats}                                                                                                                         |
| afvalfractie             | character varying              | type afval wat wordt ingezameld                                                                                                         |  { (Anders, leeg, onbekend), Rest,  Glas,  Papier,  Plastic,   Textiel,   GFT,   Grof,  PMD (Plastic of Metalen verpakkingen en Drinkpakken),  Brood } |
| loopafstand_afvalfractie | numeric                        | berekende mediaan van de afstand over de weg van de woningen binnen het pand tot cluster van containers van de betreffende afvalfractie |                                                                                                                                                        |
| categorie_loopafstand    | character varying              | de loopafstand berekend over de weg v                                                                                                   |                                                                                                                                                        |
| peildatum_gegeven        | timestamp                      | peildatum die aageeft wanneer de gegevens zijn afgeleid                                                                                 |                                                                                                                                                        |
| geometrie                | geometry (MULTIPOLYGON, 28992) | geometrie van het type POLYGON of MULTIPOLYGON in RD (epsg:28992)                                                                       |                                                                                                                                                        |