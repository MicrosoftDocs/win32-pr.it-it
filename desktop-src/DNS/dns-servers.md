---
title: Server DNS
description: Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Server DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712241"
---
# <a name="dns-servers"></a>Server DNS

Un *server DNS* è un computer che completa il processo di risoluzione dei nomi in DNS. I server DNS contengono [*file di zona*](z-gly.md) che consentono di risolvere i nomi in indirizzi IP e indirizzi IP in nomi. Quando viene eseguita una query, un server DNS risponderà in uno dei tre modi seguenti:

-   Il server restituisce i dati richiesti per la risoluzione dei nomi o la risoluzione IP.
-   Il server restituisce un puntatore a un altro server DNS che può servire la richiesta.
-   Il server indica che non sono presenti i dati richiesti.

I server DNS potrebbero, durante la preparazione della restituzione dei dati di risoluzione richiesti, eseguire una query su altri server DNS, ma, oltre a questo, i server DNS non eseguono altre operazioni.

Sono disponibili tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache.

## <a name="primary-server"></a>Server primario

Il *server primario* è il server autorevole per la zona. Tutte le attività amministrative associate alla zona, ad esempio la creazione di sottodomini all'interno della zona o altre attività amministrative simili, devono essere eseguite sul server primario. Inoltre, le eventuali modifiche associate alla zona o alle eventuali modifiche o aggiunte a RRs nei file di zona devono essere effettuate sul server primario. Per qualsiasi zona, esiste un server primario, tranne quando si integra Active Directory Services e il server DNS Microsoft.

## <a name="secondary-servers"></a>Server secondari

I *server secondari* sono server DNS di backup. I server secondari ricevono tutti i file di zona dai file di zona del server primario in un trasferimento di zona. Per qualsiasi zona specificata possono esistere più server secondari, il numero necessario per fornire [*bilanciamento del carico*](l-gly.md), [*tolleranza di errore*](f-gly.md)e riduzione del traffico. Inoltre, qualsiasi server DNS specificato può essere un server secondario per più zone.

Oltre ai server DNS primari e secondari, è possibile usare ruoli del server DNS aggiuntivi quando tali server sono appropriati per un'infrastruttura DNS. Questi server aggiuntivi memorizzano nella cache server e server d' [*inoltri*](f-gly.md).

## <a name="caching-servers"></a>Server di memorizzazione nella cache

I [*server di memorizzazione nella cache*](c-gly.md), noti anche come server solo caching, eseguono come suggerito il nome; forniscono solo il servizio di query memorizzato nella cache per le risposte DNS. Anziché gestire i file di zona come altri server secondari, la memorizzazione nella cache dei server DNS esegue query, memorizza nella cache le risposte e restituisce i risultati al client di query. La differenza principale tra i server di memorizzazione nella cache e gli altri server secondari è che altri server secondari gestiscono i file di zona (ed eseguono trasferimenti di zona quando appropriato, generando così il traffico di rete associato al trasferimento), i server di memorizzazione nella cache non lo sono.

 

 




