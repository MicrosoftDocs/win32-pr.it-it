---
title: Gestione dei record di risorse DNS
description: Informazioni sulla gestione dei record di risorse. Un record di risorse è l'unità di immissione di informazioni nei file di zona DNS, usata per risolvere tutte le query DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c818899414cc541a1c89bfd11747051b2f5f1
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011114"
---
# <a name="managing-dns-resource-records"></a>Gestione dei record di risorse DNS

Un record di risorse, comunemente definito RR, è l'unità di immissione di informazioni nei file di zona DNS. Gli RR sono i blocchi predefiniti di base delle informazioni su nome host e IP e vengono usati per risolvere tutte le query DNS. I record di risorse sono disponibili in un'ampia gamma di tipi per fornire servizi di risoluzione dei nomi estesi.

I diversi tipi di RR hanno formati diversi, in quanto contengono dati diversi. Molti RR condividono un formato comune. Ogni server DNS contiene rr per la parte dello spazio dei nomi per cui è autorevole.

Il provider WMI DNS supporta attualmente i tipi di RR seguenti. Fare clic sul nome del record di risorsa per passare alla pagina di riferimento.



| Record di risorse (nel provider)                             | Descrizione                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | Record di mapping nome-indirizzo                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | Record di indirizzi da host a Ipv6                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Record del server di database del file system andrew                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | Record da indirizzo a nome ATM                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | [*Record di nome*](c-gly.md) canonico |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Record di informazioni sull'host                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | Record di rete digitale dei servizi integrati                   |
| [**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)     | Record KEY. Vedere RFC 2535                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | Record della cassetta postale                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | Agente di posta per il record di dominio                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | Agente di inoltro della posta per il record di dominio                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | Record del gruppo di posta elettronica                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Record di informazioni sulla posta elettronica                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Record di ridenominazione della cassetta postale                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | Record mail exchanger                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Record del server dei nomi                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Record successivo                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Indirizzo al record di mapping dei nomi                               |
| [**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)       | Record della persona responsabile                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Route tramite record                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | Record di firma                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Inizio dell'autorità                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Record del servizio                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Record di testo                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | Record del server WINS                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | Record di ricerca inversa WINS                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Record di servizi noti                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | Record di mapping da indirizzo a nome X.121                         |



 

## <a name="administration-steps"></a>Passaggi di amministrazione

Il provider WMI DNS consente l'amministrazione di RR dal server stesso o da host remoti. I passaggi generali necessari per amministrare gli RR tramite il provider WMI DNS sono:

-   Connessione al provider WMI DNS
-   Recupero di un'istanza del record di risorse
-   Elenco o modifica di una proprietà del record di risorse o uso di un metodo

Le attività seguenti sono collegate agli esempi di scripting associati.

-   [Elenco dei tipi di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Aggiunta di un record di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Eliminazione di un record di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Modifica di un record di risorse](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




