---
title: Record di risorse
description: Informazioni sui record di risorse. Un record di risorse è l'unità di immissione di informazioni nei file di zona DNS, usata per risolvere tutte le query DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010674"
---
# <a name="resource-records"></a>Record di risorse

Un record di risorse, comunemente noto come RR, è l'unità di immissione di informazioni nei file di zona DNS; Le richieste riservate sono i blocchi predefiniti di base delle informazioni su nome host e IP e vengono usate per risolvere tutte le query DNS. I record di risorse esistono tutti i tipi per fornire servizi estesi di risoluzione dei nomi.

Tipi diversi di RR hanno formati diversi, in quanto contengono dati diversi. In generale, tuttavia, molte RR condividono un formato comune, come illustrato nell'esempio di record di risorse di indirizzo seguente. L'esempio fittizio seguente illustra i campi trovati in un record di risorse A:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Il primo campo (microsoft.com) indica il proprietario.
-   Il secondo campo (600) è il parametro della durata (TTL), espresso in secondi.
-   Il terzo campo (IN) è il campo della classe che rappresenta la famiglia di protocolli, che è quasi sempre IN, per la classe Internet.
-   Il quarto campo (A) è il tipo di risorsa rappresentato da RR.
-   Il quinto campo (150.150.150.1) sono i dati delle risorse o RDATA. Questo campo è un tipo di variabile che fornisce informazioni appropriate per il tipo di risorsa. In questo caso, si tratta di un indirizzo IP a 32 bit.

In DNS vengono comunemente usati i tipi di record di risorse seguenti:

-   Inizio dell'autorità (SOA)
-   Server dei nomi (NS)
-   [*Record puntatore*](p-gly.md) (PTR)
-   Indirizzo (A)
-   Indirizzo IPv6 (AAAA)
-   Mail exchange (MX)
-   [*Nome canonico*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   Wins Reverse Look up (WINSR)

In DNS sono disponibili molti altri tipi di record di risorse. Per altre informazioni, vedere [Dns WMI Provider Reference](dns-wmi-provider-reference.md).

 

 




