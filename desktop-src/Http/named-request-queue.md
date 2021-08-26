---
title: Coda di richieste denominate
description: Coda di richieste denominate
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2174044f23f30470f3285e3c8fcf9bd2dbd474b10c306df7f2fbb215b992eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078346"
---
# <a name="named-request-queue"></a>Coda di richieste denominate

La funzionalità della coda di richieste denominate dell'API del server HTTP versione 2.0 consente a più applicazioni, che operano con processi e account utente separati, di accedere alla coda delle richieste. La coda di richieste viene aperta in base al nome e protetta tramite elenchi di controllo di accesso (ACL) per garantire che le applicazioni non siano in grado di accedere a dati reciproci. Un singolo processo crea la coda di richieste e concede l'autorizzazione ad altri processi per l'uso della coda di richieste. Di conseguenza, gli altri processi nel computer accedono alla coda di richieste con il privilegio minimo necessario per il servizio delle richieste. I possibili danni al servizio HTTP, a causa di vulnerabilità nel codice di terze parti, vengono ridotti al minimo quando le applicazioni vengono eseguite con privilegi minimi.

La coda di richieste denominata viene creata con [**la funzione HttpCreateRequestQueue.**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) Quando viene creata la coda di richieste, l'applicazione specifica l'ACL nel *parametro pSecurityAttribute.* L'ACL, che può essere impostato solo quando viene creata la coda di richieste, consente ai processi di lavoro di aprire la coda delle richieste, ricevere richieste e inviare risposte. Per impostazione predefinita, ai processi non è consentito aprire una coda di richieste a meno che non sia stata loro concessa l'autorizzazione nell'ACL. Le applicazioni non richiedono privilegi amministrativi per creare la coda di richieste.

La coda di richieste deve essere creata con un nome specificato nel *parametro pName* di [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) perché altri processi apronomino la coda di richieste. Se *pName* è **NULL,** viene creata una coda di richieste senza nome e nessun altro processo può aprirla.

## <a name="creator-and-controller-processes"></a>Processi creator e controller

Quando viene creata la coda di richieste, l'applicazione può aprirla come processo controller o processo creatore. I processi del controller e dell'autore fungono entrambi da amministratori per la coda di richieste, ma il controller non esegue operazioni di I/O su di essa. L'applicazione indica che si tratta di un processo controller quando viene creata la coda di richieste specificando **HTTP CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ \_ CONTROLLER** nel parametro *Flags* di [**HttpCreateRequestQueue.**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) Se il flag **HTTP CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ \_ CONTROLLER** non è impostato, l'applicazione è un processo creatore.

L'elenco seguente contiene le attività eseguite dal processo controller e dal processo creatore:

-   Creare la coda di richieste e specificare il nome.
-   Configurare la coda di richieste usando [**la funzione HttpSetRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)
-   Eseguire una query sui parametri di configurazione della coda delle richieste [**usando la funzione HttpQueryRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty)
-   Creare gruppi di URL e associarli a una coda di richieste.
-   Impostare l'ACL specificando i processi di lavoro a cui è consentito ricevere I/O nella coda delle richieste.
-   Chiamare [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) per ritardare la creazione di istanze dei processi di lavoro fino all'arrivo della prima richiesta nella coda delle richieste.

Oltre a queste attività, il processo di creazione può anche eseguire operazioni di I/O sulla coda delle richieste.

## <a name="worker-processes"></a>Processi di lavoro

Un processo di lavoro può aprire una coda di richieste esistente solo se gli è stato concesso l'accesso nell'ACL. I processi di lavoro che operano con privilegi minimi possono aprire una coda di richieste ed eseguire operazioni di I/O su di essa. Le applicazioni aprono una coda di richieste esistente chiamando [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) con **HTTP CREATE REQUEST QUEUE FLAG OPEN \_ \_ \_ \_ \_ \_ EXISTING** nel parametro *Flags* e il nome della coda di richieste nel *parametro pName.*

Il processo di lavoro esegue le funzioni seguenti:

-   Ricevere richieste e inviare risposte nella coda delle richieste.
-   Aprire una coda di richieste esistente in base al nome. L'handle per la coda di richieste restituita al processo di lavoro non può essere usato per configurare la coda di richieste.
-   Eseguire una query sui parametri di configurazione della coda di richieste.

Il diagramma seguente illustra il modello di processo di lavoro per le code di richieste. La coda di richieste può avere diversi processi di lavoro che elaborano l'I/O e un processo creatore che configura la coda di richieste.

![modello di processo di lavoro per le code di richieste](images/namedrequestqueue.png)

 

 




