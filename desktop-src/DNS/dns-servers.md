---
title: Server DNS
description: Informazioni sui server DNS. Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Server DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011254"
---
# <a name="dns-servers"></a>Server DNS

Un *server DNS* è un computer che completa il processo di risoluzione dei nomi in DNS. I server DNS [*contengono file di*](z-gly.md) zona che consentono di risolvere i nomi in indirizzi IP e indirizzi IP in nomi. Quando viene eseguita una query, un server DNS risponderà in uno dei tre modi seguenti:

-   Il server restituisce i dati di risoluzione dei nomi o IP richiesti.
-   Il server restituisce un puntatore a un altro server DNS in grado di eseguire la richiesta.
-   Il server indica che non dispone dei dati richiesti.

I server DNS potrebbero, durante la preparazione alla restituzione dei dati di risoluzione richiesti, eseguire query su altri server DNS, ma oltre a questo, i server DNS non eseguono altre operazioni.

Esistono tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache.

## <a name="primary-server"></a>Server primario

Il *server primario* è il server autorevole per la zona. Tutte le attività amministrative associate alla zona, ad esempio la creazione di sottodomini all'interno della zona o altre attività amministrative simili, devono essere eseguite nel server primario. Inoltre, tutte le modifiche associate alla zona o eventuali modifiche o aggiunte alle richiesteri nei file di zona devono essere apportate nel server primario. Per ogni zona è presente un server primario, tranne quando si integrano i servizi Active Directory e il server DNS Microsoft.

## <a name="secondary-servers"></a>Server secondari

*I server secondari* sono server DNS di backup. I server secondari ricevono tutti i relativi file di zona dai file di zona del server primario in un trasferimento di zona. Per qualsiasi zona possono esistere più server secondari, tutti necessari per garantire il bilanciamento del [*carico,*](l-gly.md)la tolleranza di [*errore*](f-gly.md)e la riduzione del traffico. Inoltre, qualsiasi server DNS specificato può essere un server secondario per più zone.

Oltre ai server DNS primari e secondari, è possibile usare ruoli server DNS aggiuntivi quando tali server sono appropriati per un'infrastruttura DNS. Questi server aggiuntivi memorizzano nella cache server e [*server d'inoltro*](f-gly.md).

## <a name="caching-servers"></a>Memorizzazione nella cache dei server

[*I server di memorizzazione*](c-gly.md)nella cache, noti anche come server di sola memorizzazione nella cache, vengono eseguono come suggerisce il nome; forniscono solo il servizio query memorizzate nella cache per le risposte DNS. Invece di gestire i file di zona come fanno altri server secondari, la memorizzazione nella cache dei server DNS esegue query, memorizza nella cache le risposte e restituisce i risultati al client che esegue le query. La differenza principale tra i server di memorizzazione nella cache e gli altri server secondari è che altri server secondari gestiscono i file di zona (e, se appropriato, e, se appropriato, generano traffico di rete associato al trasferimento), i server di memorizzazione nella cache non lo fanno.

 

 




