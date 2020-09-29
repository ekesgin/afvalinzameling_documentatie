# Productbeschrijving huishoudelijk afval

## Context
Deze datasets beschrijven de gegevens over onder- en bovengrondse afvalcontainers, hun locaties en afvalfracties.
Alle data wordt dagelijks geactualiseerd.

De data wordt in de volgende vormen beschikbaar:
- rest api
- OGC WFS (gebruik GIS software)

  
## Productinhoud
De productinhoud is voor alle vormen gelijk, per vorm kan de data anders zijn geordend. Op dit moment worden alleen de laatst bekende (actuele) gegevens beschikbaar gesteld. 


 - [productinhoud afvalcontainers](productinhoud_afvalcontainers.md)
 - [productinhoud clusters](productinhoud_afvalcontainer_clusters.md)
 - [productinhoud weeggegevens](productinhoud_afval_wegingen.md)
 - [productinhoud containerlocaties](productinhoud_containerlocaties.md)
 - [productinhoud containertype](productinhoud_containertype.md)
 - [productinhoud cluster_fractie](productinhoud_clusterfractie.md)


## Geografische afbakening
De producten bevatten alle gegevens binnen de bestuurlijke gemeentegrens van Amsterdam

## gegevensmodel
Het gegevensmodel representeert de samenhang tussen objectklassen uit het domein afval en gerelateerde entiteiten. Dit model vormt de basis van alle dataproducten die hieruit (kunnen) worden afgeleid.
De samenhang tussen de objecten is gebaseerd op basis van thematische voorwaarden, ruimte en tijd (historie).
Voor een grafische weergave van het model zie [logisch gegevensmodel integratie](conceptueel_gegevensmodel_integratie.md)

## Beschikbare productvormen

### Rest api
De rest api is aan te roepen met de url:
 - clusters: https://api.data.amsterdam.nl/v1/huishoudelijkafval/cluster/
 - containers: https://api.data.amsterdam.nl/v1/huishoudelijkafval/container/
 - wegingen: https://api.data.amsterdam.nl/v1/huishoudelijkafval/weging/
 - containertype: https://api.data.amsterdam.nl/v1/huishoudelijkafval/containertype/
 - cluster fractie: https://api.data.amsterdam.nl/v1/huishoudelijkafval/clusterfractie/
 - containerlocatie: https://api.data.amsterdam.nl/v1/huishoudelijkafval/containerlocatie/

### Documentatie Rest API
- Cluster: https://api.data.amsterdam.nl/v1/docs/datasets/huishoudelijkafval.html#cluster
- Container: https://api.data.amsterdam.nl/v1/docs/datasets/huishoudelijkafval.html#container
- wegingen: https://api.data.amsterdam.nl/v1/docs/datasets/huishoudelijkafval.html#weging
- containertype: https://api.data.amsterdam.nl/v1/docs/datasets/huishoudelijkafval.html#containertype
- cluster fractie: https://api.data.amsterdam.nl/v1/docs/datasets/huishoudelijkafval.html#clusterfractie
- containerlocatie

### WFS
WFS is aan te roepen met de volgende url:
https://api.data.amsterdam.nl/v1/wfs/huishoudelijkafval/

### Documentatie WFS
- Container: https://api.data.amsterdam.nl/v1/docs/wfs-datasets/huishoudelijkafval.html#container 
- Containerlocatie: https://api.data.amsterdam.nl/v1/docs/wfs-datasets/huishoudelijkafval.html#containerlocatie
- Cluster: https://api.data.amsterdam.nl/v1/docs/wfs-datasets/huishoudelijkafval.html#cluster
- Containertype: https://api.data.amsterdam.nl/v1/docs/wfs-datasets/huishoudelijkafval.html#containertype
- Weging: https://api.data.amsterdam.nl/v1/docs/wfs-datasets/huishoudelijkafval.html#weging
- Clusterfractie: https://api.data.amsterdam.nl/v1/docs/wfs-datasets/huishoudelijkafval.html#clusterfractie


## Definities objectklassen


#### afvalcontainer
Conform IMBOR luidt de definitie als volgt:
Boven- of ondergrondse bak voor de inzameling van afvalstoffen die duurzaam met de aarde verbonden is.

#### containerlocatie (well)
Een betonnen constructie voor de borging van ondergrondse afvalcontainers.

#### afvalcontainer cluster
Een afvalcontainer-cluster is een locatie waar 1 of meer afvalcontainers zijn geplaatst van 1 of meer afvalfracties.
De ondergrondse containers zijn geplaatst in putten, de bovengrondse zijn niet gemonteerd op putten. De containers zijn gerelateerd aan 1 containerlocatie van het type put/well of bovengronds.
Het cluster is afgeleid uit een verzameling van 1 of meer containerlocaties en is op basis van de volgende condities opgebouwd:
 - de maximale onderlinge afstand tussen het middelpunt tussen de nabijgelegen wells is gelijk of kleiner dan 12 meter.
 - de maximale grootte van een cluster bedraagt ook 12 meter
 - een cluster wordt niet doorsneden door een weg van het type rijbaan. Hierbij is de rijrichting niet van belang.


#### Weeggegevens
De wegingen worder per container uitgevoerd. Vanaf 2016 zijn er weeggegevens beschikbaar.
Een beperking is wanneer er meerdere containers van dezelfde fractie bij elkaar staan niet kan worden geidentificeerd welke weging op welke container betrekking heeft.

#### Cluster fractie


#### containertype
