---
title: Coda delle richieste denominate
description: Coda delle richieste denominate
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4aca045f84fe9f9e4b57365ba8831456f2dc1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332087"
---
# <a name="named-request-queue"></a>Coda delle richieste denominate

L'API server HTTP versione 2,0 denominata funzionalità coda di richieste consente a più applicazioni, che operano in processi e account utente distinti, di accedere alla coda di richieste. La coda di richieste viene aperta in base al nome e protetta tramite elenchi di controllo di accesso (ACL) per garantire che le applicazioni non siano in grado di accedere ai dati di altri. Un singolo processo crea la coda di richieste e concede l'autorizzazione ad altri processi per l'utilizzo della coda di richieste. Quindi, altri processi nel computer accedono alla coda di richieste con il privilegio minimo necessario per soddisfare le richieste. Il possibile danneggiamento del servizio HTTP, a causa di vulnerabilità nel codice di terze parti, viene ridotto al minimo quando le applicazioni vengono eseguite con privilegi minimi.

La coda di richieste denominata viene creata con la funzione [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) . Quando viene creata la coda di richieste, l'applicazione specifica l'ACL nel parametro *pSecurityAttribute* . L'ACL, che può essere impostato solo quando viene creata la coda di richieste, consente ai processi di lavoro di aprire la coda di richieste, ricevere richieste e inviare risposte. Per impostazione predefinita, i processi non possono aprire una coda di richieste a meno che non dispongano dell'autorizzazione nell'ACL. Per creare la coda di richieste, le applicazioni non richiedono privilegi amministrativi.

È necessario creare la coda di richieste con un nome specificato nel parametro *pname* di [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) per l'apertura della coda di richieste da parte di altri processi. Se *pname* è **null**, viene creata una coda di richieste senza nome e nessun altro processo può aprirlo.

## <a name="creator-and-controller-processes"></a>Processi del creatore e del controller

Quando viene creata la coda di richieste, l'applicazione può aprirla come processo del controller o processo dell'autore. I processi del controller e del creatore agiscono entrambi come amministratori per la coda di richieste, ma il controller non esegue operazioni di I/O. L'applicazione indica che si tratta di un processo controller quando la coda di richieste viene creata specificando il **controller di flag della coda di \_ \_ richiesta HTTP \_ \_ \_ create** nel parametro *Flags* di [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue). Se il flag del **controller di flag della \_ coda di \_ richiesta \_ \_ \_ http create** non è impostato, l'applicazione è un processo dell'autore.

L'elenco seguente contiene le attività eseguite dal processo del controller e dal processo Creator:

-   Creare la coda di richieste e specificare il nome.
-   Configurare la coda di richieste usando la funzione [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .
-   Eseguire una query sui parametri di configurazione della coda di richiesta utilizzando la funzione [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) .
-   Creare gruppi di URL e associarli a una coda di richieste.
-   Impostare l'ACL specificando i processi di lavoro che sono autorizzati a ricevere I/O nella coda delle richieste.
-   Chiamare [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) per ritardare la creazione di un'istanza dei processi di lavoro fino a quando non arriva la prima richiesta nella coda di richieste.

Oltre a queste attività, il processo Creator può eseguire operazioni di I/O nella coda delle richieste.

## <a name="worker-processes"></a>Processi di lavoro

Un processo di lavoro può aprire una coda di richieste esistente solo se ne è stato concesso l'accesso nell'ACL. I processi di lavoro che operano con privilegi minimi possono aprire una coda di richieste ed eseguire operazioni di I/O su di essa. Le applicazioni aprono una coda di richieste esistente chiamando [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) con il **flag di coda della richiesta di creazione http \_ \_ \_ \_ \_ aperto \_ esistente** nel parametro *Flags* e il nome della coda di richieste nel parametro *pname* .

Il processo di lavoro esegue le funzioni seguenti:

-   Ricevere richieste e inviare risposte nella coda di richieste.
-   Aprire una coda di richieste esistente in base al nome. Non è possibile usare l'handle della coda di richieste restituita al processo di lavoro per configurare la coda delle richieste.
-   Eseguire una query sui parametri di configurazione della coda di richiesta.

Il diagramma seguente illustra il modello di processo di lavoro per le code di richiesta. La coda di richieste può disporre di diversi processi di lavoro che elaborano i/O e di un processo Creator che configura la coda delle richieste.

![modello di processo di lavoro per le code di richiesta](images/namedrequestqueue.png)

 

 




