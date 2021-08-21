---
title: Apartment multithreading
description: Apartment multithreading
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69271b4fb6447d48c15fa9005d39020075af09bcc327b12ce539a739c33f8d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047919"
---
# <a name="multithreaded-apartments"></a>Apartment multithreading

In un modello di apartment a thread multipli tutti i thread del processo inizializzati come a thread libero si trovano in un singolo apartment. Non è quindi necessario effettuare il marshalling tra thread. I thread non devono recuperare e inviare messaggi perché COM non usa messaggi finestra in questo modello.

Le chiamate ai metodi degli oggetti nell'apartment multithreading possono essere eseguite su qualsiasi thread nell'apartment. Non esiste alcuna serializzazione delle chiamate. Molte chiamate possono verificarsi allo stesso metodo o allo stesso oggetto contemporaneamente. Gli oggetti creati nell'apartment multithreading devono essere in grado di gestire le chiamate ai relativi metodi da altri thread in qualsiasi momento.

Poiché le chiamate agli oggetti non vengono serializzate in alcun modo, la concorrenza di oggetti multithreading offre le massime prestazioni e sfrutta al meglio l'hardware multiprocessore per le chiamate tra thread, tra processi e tra computer. Ciò significa, tuttavia, che il codice per gli oggetti deve fornire la sincronizzazione nelle implementazioni dell'interfaccia, in genere tramite l'uso di primitive di sincronizzazione, ad esempio oggetti evento, sezioni critiche, mutex o semafori, descritti più avanti in questa sezione. Inoltre, poiché l'oggetto non controlla la durata dei thread che vi accedono, non è possibile archiviare alcuno stato specifico del thread nell'oggetto (nell'archiviazione thread-local).

Di seguito sono riportate alcune considerazioni importanti relative alla sincronizzazione per apartment multithreading:

-   COM fornisce la sincronizzazione delle chiamate solo per apartment a thread singolo.
-   Gli apartment multithreading non ricevono chiamate durante l'esecuzione di chiamate (sullo stesso thread).
-   Gli apartment multithreading non possono effettuare chiamate sincronizzate con input.
-   Le chiamate asincrone vengono convertite in chiamate sincrone in apartment multithreading.
-   Il filtro messaggi non viene chiamato per alcun thread in un apartment multithreading.

Per inizializzare un thread come a thread libero, chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), specificando COINIT \_ MULTITHREADED. Per informazioni sul threading del server in-process, vedere [Problemi di threading del server in-process.](in-process-server-threading-issues.md)

Più client possono chiamare contemporaneamente, da thread diversi, un oggetto che supporta il threading libero. Nei server out-of-process a thread libero COM, tramite il sottosistema RPC, crea un pool di thread nel processo server e una chiamata client (o più chiamate client) può essere recapitata da uno di questi thread in qualsiasi momento. Un server out-of-process deve implementare anche la sincronizzazione nel class factory. Gli oggetti in-process a thread libero possono ricevere chiamate dirette da più thread del client.

Il client può eseguire operazioni COM in più thread. Tutti i thread appartengono allo stesso apartment multithreading. I puntatori a interfaccia vengono passati direttamente da thread a thread all'interno di un apartment multithreading, pertanto non viene effettuato il marshalling dei puntatori di interfaccia tra i relativi thread. I filtri messaggi (implementazioni di [**IMessageFilter)**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)non vengono usati negli apartment multithreading. Il thread client verrà sospeso quando effettua una chiamata COM a oggetti out-of-apartment e riprenderà al termine della chiamata. Le chiamate tra processi vengono comunque gestite da RPC.

I thread inizializzati con il modello a thread libero devono implementare la propria sincronizzazione. Come accennato in precedenza in questa sezione, Windows questa implementazione tramite le primitive di sincronizzazione seguenti:

-   Gli oggetti evento consentono di segnalare a uno o più thread che si è verificato un evento. Qualsiasi thread all'interno di un processo può creare un oggetto evento. Un handle per l'evento viene restituito dalla funzione di creazione dell'evento, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Dopo aver creato un oggetto evento, i thread con un handle all'oggetto possono attenderlo prima di continuare l'esecuzione.
-   Le sezioni critiche vengono usate per una sezione di codice che richiede l'accesso esclusivo a un set di dati condivisi prima di poter essere eseguito e che viene usata solo dai thread all'interno di un singolo processo. Una sezione critica è simile a un turntile attraverso il quale può passare un solo thread alla volta, funzionando come segue:
    -   Per garantire che non più di un thread alla volta accerta i dati condivisi, il thread primario di un processo alloca una struttura di dati CRITICAL SECTION globale e ne inizializza \_ i membri. Un thread che entra in una sezione critica chiama [**la funzione EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) e modifica i membri della struttura di dati.
    -   Un thread che tenta di accedere a una sezione critica chiama [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) che verifica se la struttura dei dati CRITICAL \_ SECTION è stata modificata. In tal caso, un altro thread si trova attualmente nella sezione critica e il thread successivo viene messo in stato di sospensione. Un thread che esce da una sezione critica chiama [**LeaveCriticalSection,**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection)che reimposta la struttura dei dati. Quando un thread esce da una sezione critica, il sistema riattiva uno dei thread in sospensione, che quindi entra nella sezione critica.
-   I mutex eseguono la stessa funzione di una sezione critica, ad eccezione del fatto che il mutex è accessibile ai thread in esecuzione in processi diversi. La proprietà di un oggetto mutex è come avere il piano in un distorsio. Un processo crea un oggetto mutex chiamando la [**funzione CreateMutex,**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) che restituisce un handle. Il primo thread che richiede un oggetto mutex ottiene la proprietà di esso. Quando il thread termina con il mutex, la proprietà passa ad altri thread in base al primo passaggio.
-   I semafori vengono usati per mantenere un conteggio dei riferimenti su alcune risorse disponibili. Un thread crea un semaforo per una risorsa chiamando la funzione [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) e passando un puntatore alla risorsa, un conteggio delle risorse iniziale e il numero massimo di risorse. Questa funzione restituisce un handle. Un thread che richiede una risorsa passa l'handle del semaforo in una chiamata alla [**funzione WaitForSingleObject.**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) L'oggetto semaforo esegue il polling della risorsa per determinare se è disponibile. In tal caso, il semaforo decrementa il numero di risorse e riattiva il thread in attesa. Se il conteggio è zero, il thread rimane in stato di sospensione fino a quando un altro thread rilascia una risorsa, causando l'incremento del conteggio a uno da parte del semaforo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 