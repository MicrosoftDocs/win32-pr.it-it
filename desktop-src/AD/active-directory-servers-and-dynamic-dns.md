---
title: Server Active Directory e DNS dinamico
description: I server Active Directory pubblicano gli indirizzi in modo che i client possano trovarli conoscendo solo il nome di dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9828a2d6d14d862e98d3c5c4129bbc70f5c411
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880067"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Server Active Directory e DNS dinamico

I server Active Directory pubblicano gli indirizzi in modo che i client possano trovarli conoscendo solo il nome di dominio. I server Active Directory vengono pubblicati usando i record di risorse del servizio (RR SRV) in DNS. SRV RR è un record DNS usato per eseguire il mapping del nome di un servizio all'indirizzo di un server che offre il servizio. Il nome di un RR SRV è nel formato seguente:


```C++
<service>.<protocol>.<domain>
```



I server Active Directory offrono il servizio LDAP tramite il protocollo TCP in modo che i nomi pubblicati siano "ldap.tcp. &lt; dominio &gt; ". Di conseguenza, sRV RR per fabrikam.com è "ldap.tcp.fabrikam.com". Dati aggiuntivi sul server SRV RR indicano la priorità e il peso del server, consentendo ai client di scegliere il server migliore per le proprie esigenze.

Quando viene installato un server Active Directory, usa DNS dinamico per pubblicare se stesso. Poiché gli indirizzi TCP/IP sono soggetti a modifiche, i server verificano periodicamente le registrazioni per assicurarsi che siano corrette e, se necessario, le aggiornano.

Dns dinamico è un'aggiunta recente allo standard DNS. DNS dinamico definisce un protocollo per l'aggiornamento dinamico di un server DNS con nuovi dati. Prima del DNS dinamico, gli amministratori dovevano configurare manualmente i record archiviati dai server DNS.

 

 




