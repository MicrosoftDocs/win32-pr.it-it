---
title: Record di risorse
description: Un record di risorse, noto come RR, è l'unità di immissione di informazioni nei file di zona DNS. RRs sono i blocchi predefiniti di base del nome host e le informazioni IP e vengono usati per risolvere tutte le query DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712799"
---
# <a name="resource-records"></a>Record di risorse

Un record di risorse, noto come RR, è l'unità di immissione di informazioni nei file di zona DNS. RRs sono i blocchi predefiniti di base del nome host e le informazioni IP e vengono usati per risolvere tutte le query DNS. I record di risorse esistono come molti tipi per offrire servizi estesi per la risoluzione dei nomi.

Diversi tipi di RRs hanno formati diversi, poiché contengono dati diversi. In generale, tuttavia, molti RRs condividono un formato comune, come illustrato nell'esempio riportato di seguito. Nell'esempio fittizio riportato di seguito vengono illustrati i campi presenti in un record di risorse:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Il primo campo (microsoft.com) indica il proprietario.
-   Il secondo campo (600) è il parametro TTL (time-to-Live), in secondi.
-   Il terzo campo (IN) è il campo della classe che rappresenta la famiglia di protocolli, che è quasi sempre IN, per la classe Internet.
-   Il quarto campo (A) è il tipo di risorsa che rappresenta l'RR.
-   Il quinto campo (150.150.150.1) è i dati della risorsa, o RDATA. Questo campo è un tipo di variabile che fornisce le informazioni appropriate per il tipo di risorsa. in questo caso, si tratta di un indirizzo IP a 32 bit.

I tipi di record di risorse seguenti sono comunemente usati in DNS:

-   Inizio dell'autorità (SOA)
-   Server del nome (NS)
-   [*Record puntatore*](p-gly.md) (PTR)
-   Indirizzo (A)
-   Indirizzo IPv6 (AAAA)
-   Mail Exchange (MX)
-   [*Nome canonico*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   Ricerca inversa WINS (WINSr)

Sono disponibili molti altri tipi di record di risorse in DNS. Per ulteriori informazioni, vedere [riferimento del provider WMI DNS](dns-wmi-provider-reference.md).

 

 




