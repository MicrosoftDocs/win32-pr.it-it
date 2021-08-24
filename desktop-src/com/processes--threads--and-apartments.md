---
title: Processi, thread e apartment
description: Un processo è una raccolta di spazio di memoria virtuale, codice, dati e risorse di sistema.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320b09d76200739c77c7202af4d53a35089b2eca2e6fd282dd507f048aa7a10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130033"
---
# <a name="processes-threads-and-apartments"></a>Processi, thread e apartment

Un *processo* è una raccolta di spazio di memoria virtuale, codice, dati e risorse di sistema. Un *thread è* codice che deve essere eseguito in serie all'interno di un processo. Un processore esegue thread, non processi, quindi ogni applicazione ha almeno un processo e un processo ha sempre almeno un thread di esecuzione, noto come thread primario. Un processo può avere più thread oltre al thread primario.

I processi comunicano tra loro tramite messaggi, usando la tecnologia RPC (Remote Procedure Call) di Microsoft per passare informazioni tra loro. Non esiste alcuna differenza per il chiamante tra una chiamata proveniente da un processo in un computer remoto e una chiamata proveniente da un altro processo nello stesso computer.

Quando un thread inizia a essere eseguito, continua fino a quando non viene interrotto o interrotto da un thread con priorità più alta (da un'azione dell'utente o dall'utilità di pianificazione dei thread del kernel). Ogni thread può eseguire sezioni separate di codice oppure più thread possono eseguire la stessa sezione di codice. I thread che eseguono lo stesso blocco di codice mantengono stack separati. Ogni thread in un processo condivide le variabili e le risorse globali del processo.

L'utilità di pianificazione del thread determina quando e con quale frequenza eseguire un thread, in base a una combinazione dell'attributo della classe di priorità del processo e della priorità di base del thread. Per impostare l'attributo della classe di priorità di un processo, chiamare la [**funzione SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) e impostare la priorità di base di un thread con una chiamata a [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Le applicazioni multithreading devono evitare due problemi di threading: *deadlock* *e race.* Un deadlock si verifica quando ogni thread è in attesa che l'altro eserciti un'operazione. Il controllo delle chiamate COM consente di evitare deadlock nelle chiamate tra oggetti. Un race condition si verifica quando un thread termina prima di un altro da cui dipende, causando l'uso di un valore non inizializzato da parte del primo perché quest'ultimo non ne ha ancora fornito uno valido. COM fornisce alcune funzioni appositamente progettate per evitare race conditions nei server out-of-process. Vedere [Helper di implementazione del server out-of-process.](out-of-process-server-implementation-helpers.md)

## <a name="the-apartment-and-the-com-threading-architecture"></a>Apartment e architettura di threading COM

Mentre COM supporta il modello a thread singolo per processo prevalente prima dell'introduzione di più thread di esecuzione, è possibile scrivere codice per sfruttare i vantaggi di più thread, generando applicazioni più efficienti, consentendo l'esecuzione di un thread mentre un altro thread attende il completamento di un'operazione dispendiosa in termini di tempo.

> [!Note]  
> L'uso di più thread non garantisce prestazioni migliori. Infatti, poiché il factoring dei thread è un problema difficile, l'uso di più thread spesso causa problemi di prestazioni. La chiave è usare più thread solo se si è molto certi di ciò che si sta facendo.

 

In generale, il modo più semplice per visualizzare l'architettura di threading COM è pensare a tutti gli oggetti COM nel processo come suddivisi in gruppi denominati *apartment.* Un oggetto COM risiede esattamente in un apartment, nel senso che i relativi metodi possono essere legalmente chiamati direttamente solo da un thread appartenente a tale apartment. Qualsiasi altro thread che vuole chiamare l'oggetto deve passare attraverso un proxy.

Esistono due tipi di apartment: apartment a [thread singolo](single-threaded-apartments.md)e [apartment multithreading.](multithreaded-apartments.md)

-   Gli apartment a thread singolo sono costituiti esattamente da un thread, pertanto tutti gli oggetti COM che si convivono in un apartment a thread singolo possono ricevere chiamate al metodo solo da un thread appartenente a tale apartment. Tutte le chiamate di metodo a un oggetto COM in un apartment a thread singolo vengono sincronizzate con la coda di messaggi di Windows per il thread dell'apartment a thread singolo. Un processo con un singolo thread di esecuzione è semplicemente un caso speciale di questo modello.
-   Gli apartment multithreading sono costituiti da uno o più thread, pertanto tutti gli oggetti COM che si convivono in un apartment multithreading possono ricevere chiamate al metodo direttamente da uno qualsiasi dei thread che appartengono all'apartment multithreading. I thread in un apartment multithreading usano un modello denominato *free-threading*. Le chiamate agli oggetti COM in un apartment multithreading vengono sincronizzate dagli oggetti stessi.

> [!Note]  
> Per una descrizione della comunicazione tra apartment a thread singolo e apartment multithreading all'interno dello stesso processo, vedere Comunicazione a thread singolo [e multithreading](single-threaded-and-multithreaded-communication.md).

 

Un processo può avere zero o più apartment a thread singolo e zero o un apartment multithreading.

In un processo, l'apartment principale è il primo da inizializzare. In un processo a thread singolo, questo è l'unico apartment. Viene effettuato il marshalling dei parametri di chiamata tra apartment e COM gestisce la sincronizzazione tramite messaggistica. Se si designa più thread in un processo come thread libero, tutti i thread liberi risiedono in un singolo apartment, i parametri vengono passati direttamente a qualsiasi thread nell'apartment ed è necessario gestire tutta la sincronizzazione. In un processo con threading free e apartment, tutti i thread liberi risiedono in un singolo apartment e tutti gli altri apartment sono apartment a thread singolo. Un processo che esegue il lavoro COM è una raccolta di apartment con, al massimo, un apartment multithreading ma un numero qualsiasi di apartment a thread singolo.

I modelli di threading in COM forniscono il meccanismo per consentire ai client e ai server che usano architetture di threading diverse di funzionare insieme. Le chiamate tra oggetti con modelli di threading diversi in processi diversi sono naturalmente supportate. Dal punto di vista dell'oggetto chiamante, tutte le chiamate a oggetti all'esterno di un processo si comportano in modo identico, indipendentemente dal modo in cui l'oggetto chiamato viene threadato. Analogamente, dal punto di vista dell'oggetto chiamato, le chiamate in arrivo si comportano in modo identico, indipendentemente dal modello di threading del chiamante.

L'interazione tra un client e un oggetto out-of-process è semplice, anche quando usano modelli di threading diversi perché il client e l'oggetto si trova in processi diversi. COM, interposto tra il client e il server, può fornire il codice per l'interoperabilità dei modelli di threading, usando il marshalling standard e RPC. Ad esempio, se un oggetto a thread singolo viene chiamato contemporaneamente da più client a thread libero, le chiamate verranno sincronizzate da COM inserendo i messaggi di finestra corrispondenti nella coda di messaggi del server. L'apartment dell'oggetto riceverà una chiamata ogni volta che recupera e invia messaggi. È tuttavia necessario assicurarsi che i server in-process interagiscano correttamente con i client. Vedere [Problemi di threading del server in-process.](in-process-server-threading-issues.md)

Il problema più importante nella programmazione con un modello multithreading è rendere il codice thread-safe in modo che i messaggi destinati a un thread specifico vadano solo a tale thread e l'accesso ai thread sia protetto.

Per altre informazioni, vedere i seguenti argomenti:

-   [Scelta del modello di threading](choosing-the-threading-model.md)
-   [Apartment a thread singolo](single-threaded-apartments.md)
-   [Apartment multithreading](multithreaded-apartments.md)
-   [Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
-   [Problemi di threading del server in-process](in-process-server-threading-issues.md)
-   [Accesso alle interfacce tra apartment](accessing-interfaces-across-apartments.md)

 

 