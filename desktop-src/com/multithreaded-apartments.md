---
title: Apartment con multithreading
description: Apartment con multithreading
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2594f9341fc662b068fb7e007e538282a31273
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300547"
---
# <a name="multithreaded-apartments"></a>Apartment con multithreading

In un modello di Apartment a thread multipli tutti i thread del processo che sono stati inizializzati come a thread libero si trovano in un unico Apartment. Non è pertanto necessario effettuare il marshalling tra thread. I thread non devono recuperare e inviare messaggi perché COM non usa i messaggi di finestra in questo modello.

Le chiamate a metodi di oggetti nell'Apartment con multithreading possono essere eseguite in qualsiasi thread dell'Apartment. Nessuna serializzazione delle chiamate; molte chiamate possono verificarsi contemporaneamente allo stesso metodo o allo stesso oggetto. Gli oggetti creati nell'Apartment a thread multipli devono essere in grado di gestire le chiamate sui rispettivi metodi da altri thread in qualsiasi momento.

Poiché le chiamate agli oggetti non vengono serializzate in alcun modo, la concorrenza di oggetti multithreading offre le prestazioni più elevate e sfrutta al meglio l'hardware del multiprocessore per la chiamata cross-thread, tra processi e tra computer. Ciò significa, tuttavia, che il codice per gli oggetti deve fornire la sincronizzazione nelle implementazioni dell'interfaccia, in genere tramite l'uso di primitive di sincronizzazione, ad esempio oggetti evento, sezioni critiche, mutex o semafori, descritti più avanti in questa sezione. Inoltre, poiché l'oggetto non controlla la durata dei thread che vi accedono, non è possibile archiviare lo stato specifico del thread nell'oggetto (nell'archiviazione locale del thread).

Di seguito sono riportate alcune considerazioni importanti relative alla sincronizzazione per gli Apartment a thread multipli:

-   COM fornisce la sincronizzazione delle chiamate solo per gli Apartment a thread singolo.
-   Gli Apartment con multithreading non ricevono chiamate durante l'esecuzione di chiamate (sullo stesso thread).
-   Gli apartment multithreading non possono eseguire chiamate sincronizzate in input.
-   Le chiamate asincrone vengono convertite in chiamate sincrone in Apartment con multithreading.
-   Il filtro messaggi non viene chiamato per alcun thread in un Apartment a thread multipli.

Per inizializzare un thread come a thread libero, chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), specificando CoInit \_ multithreading. Per informazioni sul threading del server in-process, vedere [problemi di threading del server in-process](in-process-server-threading-issues.md).

Più client possono chiamare contemporaneamente, da thread diversi, un oggetto che supporta il threading libero. Nei server out-of-process a thread libero, COM, tramite il sottosistema RPC, crea un pool di thread nel processo server e una chiamata client (o più chiamate client) può essere recapitata da uno qualsiasi di questi thread in qualsiasi momento. Un server out-of-process deve implementare anche la sincronizzazione nell'class factory. Gli oggetti in-process a thread libero possono ricevere chiamate dirette da più thread del client.

Il client può eseguire operazioni COM in più thread. Tutti i thread appartengono allo stesso Apartment a thread multipli. I puntatori di interfaccia vengono passati direttamente dal thread al thread all'interno di un Apartment a thread multipli, quindi non viene eseguito il marshalling dei puntatori di interfaccia tra i thread. I filtri messaggi (implementazioni di [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)) non vengono usati negli Apartment a thread multipli. Il thread client verrà sospeso quando effettuerà una chiamata COM a oggetti out-of-Apartment e riprenderà quando la chiamata restituirà. Le chiamate tra i processi sono ancora gestite da RPC.

I thread inizializzati con il modello a thread libero devono implementare la propria sincronizzazione. Come indicato in precedenza in questa sezione, Windows Abilita questa implementazione tramite le primitive di sincronizzazione seguenti:

-   Gli oggetti evento consentono di segnalare uno o più thread in cui si è verificato un evento. Qualsiasi thread all'interno di un processo può creare un oggetto evento. Un handle per l'evento viene restituito dalla funzione di creazione degli eventi, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Una volta creato un oggetto evento, i thread con un handle per l'oggetto possono attenderlo prima di continuare l'esecuzione.
-   Le sezioni critiche vengono utilizzate per una sezione di codice che richiede l'accesso esclusivo a un set di dati condivisi prima che sia possibile eseguirlo e che venga utilizzato solo dai thread all'interno di un singolo processo. Una sezione critica è come un tornello attraverso il quale può trascorrere un solo thread alla volta, funzionando come segue:
    -   Per assicurarsi che non più di un thread alla volta acceda ai dati condivisi, il thread primario di un processo alloca una struttura di \_ dati della sezione critica globale e inizializza i relativi membri. Un thread che entra in una sezione critica chiama la funzione [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) e modifica i membri della struttura di dati.
    -   Un thread che tenta di immettere una sezione critica chiama [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) che verifica se la \_ struttura dei dati della sezione critica è stata modificata. In tal caso, un altro thread si trova attualmente nella sezione critica e il thread successivo viene messo in stato di sospensione. Un thread che lascia una sezione critica chiama [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection), che reimposta la struttura dei dati. Quando un thread lascia una sezione critica, il sistema riattiva uno dei thread in sospensione, che quindi immette la sezione critica.
-   Mutex esegue la stessa funzione di una sezione critica, ad eccezione del fatto che il mutex è accessibile ai thread in esecuzione in processi diversi. Il proprietario di un oggetto mutex è simile a una discussione. Un processo crea un oggetto mutex chiamando la funzione [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) , che restituisce un handle. Il primo thread che richiede un oggetto Mutex ne ottiene la proprietà. Quando il thread è terminato con il mutex, la proprietà passa ad altri thread in base a una prima esecuzione, prima che venga servita.
-   I semafori vengono usati per mantenere un conteggio dei riferimenti in alcune risorse disponibili. Un thread crea un semaforo per una risorsa chiamando la funzione [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) e passando un puntatore alla risorsa, un numero di risorse iniziale e il numero massimo di risorse. Questa funzione restituisce un handle. Un thread che richiede una risorsa passa l'handle del semaforo in una chiamata alla funzione [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) . L'oggetto semaforo esegue il polling della risorsa per stabilire se è disponibile. In tal caso, il semaforo decrementa il conteggio delle risorse e riattiva il thread in attesa. Se il conteggio è pari a zero, il thread rimane in attesa fino a quando un altro thread non rilascia una risorsa, causando l'incremento del numero a uno del semaforo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra gli Apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 