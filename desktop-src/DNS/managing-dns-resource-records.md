---
title: Gestione dei record di risorse DNS
description: Un record di risorse, noto come RR, è l'unità di immissione di informazioni nei file di zona DNS. RRs sono i blocchi predefiniti di base del nome host e le informazioni IP e vengono usati per risolvere tutte le query DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99edffa52b5137858468fd64122d2af826a896ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856521"
---
# <a name="managing-dns-resource-records"></a>Gestione dei record di risorse DNS

Un record di risorse, noto come RR, è l'unità di immissione di informazioni nei file di zona DNS. RRs sono i blocchi predefiniti di base del nome host e le informazioni IP e vengono usati per risolvere tutte le query DNS. I record di risorse sono disponibili in un'ampia gamma di tipi per offrire servizi estesi per la risoluzione dei nomi.

Diversi tipi di RRs hanno formati diversi, poiché contengono dati diversi. Molti RRs condividono un formato comune. Ogni server DNS contiene RRs per la parte dello spazio dei nomi per cui è autorevole.

Il provider WMI DNS supporta attualmente i tipi RR seguenti. Fare clic sul nome del record di risorse per passare alla relativa pagina di riferimento.



| Record di risorse (nel provider)                             | Descrizione                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**\_AType MicrosoftDNS**](microsoftdns-atype.md)         | Nome da indirizzare al record di mapping                               |
| [**\_AAAAType MicrosoftDNS**](microsoftdns-aaaatype.md)   | Da host a record di indirizzi IPv6                                  |
| [**\_AFSDBType MicrosoftDNS**](microsoftdns-afsdbtype.md) | Record del server di database del file System Andrew                    |
| [**\_ATMAType MicrosoftDNS**](microsoftdns-atmatype.md)   | Record da indirizzo a nome ATM                                   |
| [**\_CNAMEType MicrosoftDNS**](microsoftdns-cnametype.md) | Record di [*nome canonico*](c-gly.md) |
| [**\_HINFOType MicrosoftDNS**](microsoftdns-hinfotype.md) | Record informazioni host                                      |
| [**\_ISDNType MicrosoftDNS**](microsoftdns-isdntype.md)   | Record di rete digitale dei servizi integrati                   |
| [**Tipo di MicrosoftDNS \_**](microsoftdns-keytype.md)     | Record di chiave. Vedere RFC 2535                                     |
| [**\_MBType MicrosoftDNS**](microsoftdns-mbtype.md)       | Record cassetta postale                                               |
| [**\_MDType MicrosoftDNS**](microsoftdns-mdtype.md)       | Agente di posta elettronica per il record di dominio                             |
| [**\_MFType MicrosoftDNS**](microsoftdns-mftype.md)       | Agente di invio della posta elettronica per il record di dominio                  |
| [**\_MGType MicrosoftDNS**](microsoftdns-mgtype.md)       | Record del gruppo di posta                                            |
| [**\_MINFOType MicrosoftDNS**](microsoftdns-minfotype.md) | Record di informazioni sulla posta                                      |
| [**\_MRType MicrosoftDNS**](microsoftdns-mrtype.md)       | Record di ridenominazione delle cassette postali                                        |
| [**\_MXType MicrosoftDNS**](microsoftdns-mxtype.md)       | Record di Mail Exchanger                                        |
| [**\_NSType MicrosoftDNS**](microsoftdns-nstype.md)       | Record del server dei nomi                                           |
| [**\_NXTType MicrosoftDNS**](microsoftdns-nxttype.md)     | Record successivo                                                  |
| [**\_PTRType MicrosoftDNS**](microsoftdns-ptrtype.md)     | Indirizzo del record di mapping dei nomi                               |
| [**\_RPType MicrosoftDNS**](microsoftdns-rptype.md)       | Record persona responsabile                                    |
| [**\_RTType MicrosoftDNS**](microsoftdns-rttype.md)       | Route attraverso record                                         |
| [**\_SIGType MicrosoftDNS**](microsoftdns-sigtype.md)     | Record di firma                                             |
| [**\_SOAType MicrosoftDNS**](microsoftdns-soatype.md)     | Inizio dell'autorità                                           |
| [**\_SRVType MicrosoftDNS**](microsoftdns-srvtype.md)     | Record di servizio                                               |
| [**\_TXTType MicrosoftDNS**](microsoftdns-txttype.md)     | Record di testo                                                  |
| [**\_WINSType MicrosoftDNS**](microsoftdns-winstype.md)   | Record server WINS                                           |
| [**\_WINSRType MicrosoftDNS**](microsoftdns-winsrtype.md) | Record di ricerca inversa WINS                                   |
| [**\_WKSType MicrosoftDNS**](microsoftdns-wkstype.md)     | Record di servizi noti                                   |
| [**\_X25Type MicrosoftDNS**](microsoftdns-x25type.md)     | Record di mapping da indirizzo a nome X. 121                         |



 

## <a name="administration-steps"></a>Procedura di amministrazione

Il provider WMI DNS consente l'amministrazione di RRs dal server stesso o da host remoti. I passaggi generali necessari per amministrare RRs usando il provider WMI DNS sono:

-   Connessione al provider WMI DNS
-   Recupero di un'istanza di record di risorse
-   Elenco o modifica di una proprietà del record di risorse o utilizzo di un metodo

Le attività seguenti sono collegate agli esempi di script associati.

-   [Elenco di tipi di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Aggiunta di un record di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Eliminazione di un record di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Modifica di un record di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




