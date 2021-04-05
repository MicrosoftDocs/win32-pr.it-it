---
title: Server Active Directory e DNS dinamico
description: I server Active Directory pubblicano i relativi indirizzi in modo che i client possano individuarli conoscendo solo il nome di dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707222"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Server Active Directory e DNS dinamico

I server Active Directory pubblicano i relativi indirizzi in modo che i client possano individuarli conoscendo solo il nome di dominio. I server Active Directory vengono pubblicati usando i record di risorse del servizio (SRV RR) in DNS. SRV RR è un record DNS utilizzato per eseguire il mapping del nome di un servizio all'indirizzo di un server che offre il servizio. Il nome di un record SRV è nel formato seguente:


```C++
<service>.<protocol>.<domain>
```



I server Active Directory offrono il servizio LDAP sul protocollo TCP, in modo che i nomi pubblicati siano "LDAP. <domain> TCP". Pertanto, l'RR SRV per fabrikam.com è "ldap.tcp.fabrikam.com". I dati aggiuntivi sull'RR SRV indicano la priorità e il peso per il server, consentendo ai client di scegliere il server migliore per le proprie esigenze.

Quando si installa un server di Active Directory, viene utilizzato il DNS dinamico per la pubblicazione. Poiché gli indirizzi TCP/IP sono soggetti a modifiche, i server verificano periodicamente le registrazioni per assicurarsi che siano corretti e aggiornarli, se necessario.

Il DNS dinamico è una recente aggiunta allo standard DNS. DNS dinamico definisce un protocollo per l'aggiornamento dinamico di un server DNS con nuovi dati. Prima del DNS dinamico, agli amministratori veniva richiesto di configurare manualmente i record archiviati dai server DNS.

 

 




