---
title: Record di risorse
description: Informazioni sui record di risorse. Un record di risorse è l'unità di immissione di informazioni nei file di zona DNS, usata per risolvere tutte le query DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606d74f41e18fefa144ff21d3ed88d9683938304b0c8aa0bc7d94e2fbaa624cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825061"
---
# <a name="resource-records"></a>Record di risorse

Un record di risorse, comunemente definito RR, è l'unità di immissione di informazioni nei file di zona DNS. Gli RR sono i blocchi predefiniti di base delle informazioni su nome host e IP e vengono usati per risolvere tutte le query DNS. I record di risorse esistono tutti i tipi per fornire servizi di risoluzione dei nomi estesi.

I diversi tipi di RR hanno formati diversi, in quanto contengono dati diversi. In generale, tuttavia, molti RR condividono un formato comune, come illustrato nell'esempio seguente di record di risorse degli indirizzi. L'esempio fittizio seguente illustra i campi trovati in un record di risorsa A:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Il primo campo (microsoft.com) indica il proprietario.
-   Il secondo campo (600) è il parametro time-to-live (TTL), espresso in secondi.
-   Il terzo campo (IN) è il campo della classe che rappresenta la famiglia di protocolli, che è quasi sempre IN, per la classe Internet.
-   Il quarto campo (A) è il tipo di risorsa rappresentato da RR.
-   Il quinto campo (150.150.150.1) è i dati della risorsa o RDATA. Questo campo è un tipo di variabile che fornisce informazioni appropriate per il tipo di risorsa. In questo caso, si tratta di un indirizzo IP a 32 bit.

I tipi di record di risorse seguenti vengono comunemente usati in DNS:

-   Inizio dell'autorità (SOA)
-   Server dei nomi (NS)
-   [*Record puntatore*](p-gly.md) (PTR)
-   Indirizzo (A)
-   Indirizzo IPv6 (AAAA)
-   Mail exchange (MX)
-   [*Nome canonico*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   Ricerca inversa WINS (WINSR)

In DNS sono disponibili molti altri tipi di record di risorse. Per altre informazioni, vedere [Informazioni di riferimento sul provider WMI DNS](dns-wmi-provider-reference.md).

 

 




