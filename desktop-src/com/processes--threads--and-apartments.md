---
title: Processi, thread e Apartment
description: Un processo è una raccolta di spazio di memoria virtuale, codice, dati e risorse di sistema.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d598fc9d7dd39ab070b58aa7ba45a6e2fcae90db
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399758"
---
# <a name="processes-threads-and-apartments"></a>Processi, thread e Apartment

Un *processo* è una raccolta di spazio di memoria virtuale, codice, dati e risorse di sistema. Un *thread* è il codice che deve essere eseguito in modo seriale all'interno di un processo. Un processore esegue thread, non processi, quindi ogni applicazione dispone di almeno un processo e un processo ha sempre almeno un thread di esecuzione, noto come thread primario. Un processo può avere più thread oltre al thread primario.

I processi comunicano tra loro tramite messaggi, usando la tecnologia RPC (Remote Procedure Call) di Microsoft per passare le informazioni tra loro. Non esiste alcuna differenza per il chiamante tra una chiamata proveniente da un processo in un computer remoto e una chiamata proveniente da un altro processo nello stesso computer.

Quando un thread inizia l'esecuzione, continua fino a quando non viene terminato o fino a quando non viene interrotto da un thread con priorità più alta (da un'azione dell'utente o dall'utilità di pianificazione dei thread del kernel). Ogni thread può eseguire sezioni separate di codice oppure più thread possono eseguire la stessa sezione di codice. I thread che eseguono lo stesso blocco di codice conservano stack distinti. Ogni thread in un processo condivide le variabili e le risorse globali del processo.

L'utilità di pianificazione dei thread determina quando e con quale frequenza eseguire un thread, in base a una combinazione dell'attributo della classe di priorità del processo e della priorità di base del thread. Per impostare un attributo della classe di priorità di un processo, chiamare la funzione [**SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) e impostare la priorità di base di un thread con una chiamata a [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Le applicazioni multithread devono evitare due problemi di threading: *deadlock* e *Races*. Si verifica un deadlock quando ogni thread è in attesa dell'altro per eseguire un'operazione. Il controllo delle chiamate COM consente di impedire deadlock nelle chiamate tra oggetti. Un race condition si verifica quando un thread termina prima di un altro oggetto da cui dipende, causando il primo utilizzo di un valore non inizializzato perché quest'ultimo non ha ancora fornito un valore valido. COM fornisce alcune funzioni progettate appositamente per evitare race condition nei server out-of-process. (Vedere [Helper di implementazione di server out-of-process](out-of-process-server-implementation-helpers.md)).

## <a name="the-apartment-and-the-com-threading-architecture"></a>L'Apartment e l'architettura di threading COM

Sebbene COM supporti il modello a thread singolo per processo prevalentemente prima dell'introduzione di più thread di esecuzione, è possibile scrivere codice per sfruttare i vantaggi di più thread, ottenendo applicazioni più efficienti, consentendo l'esecuzione di un thread mentre un altro thread attende il completamento di un'operazione che richiede molto tempo.

> [!Note]  
> L'uso di più thread non garantisce prestazioni migliori. Infatti, poiché il fattore di threading è un problema complesso, l'utilizzo di più thread causa spesso problemi di prestazioni. La chiave consiste nell'usare più thread solo se si è sicuri di ciò che si sta facendo.

 

In generale, il modo più semplice per visualizzare l'architettura di threading COM consiste nel considerare tutti gli oggetti COM nel processo suddivisi in gruppi denominati *Apartment*. Un oggetto COM risiede esattamente in un Apartment, nel senso che i relativi metodi possono essere chiamati legalmente direttamente da un thread che appartiene a tale Apartment. Qualsiasi altro thread che desidera chiamare l'oggetto deve passare attraverso un proxy.

Sono disponibili due tipi di Apartment: [Apartment a thread singolo](single-threaded-apartments.md)e [apartment multithreading](multithreaded-apartments.md).

-   Gli Apartment a thread singolo sono costituiti esattamente da un solo thread, quindi tutti gli oggetti COM che risiedono in un Apartment a thread singolo possono ricevere chiamate al metodo solo da un thread che appartiene a tale Apartment. Tutte le chiamate al metodo a un oggetto COM in un Apartment a thread singolo vengono sincronizzate con la coda di messaggi di Windows per il thread dell'Apartment a thread singolo. Un processo con un solo thread di esecuzione è semplicemente un caso speciale di questo modello.
-   Gli Apartment a thread multipli sono costituiti da uno o più thread, quindi tutti gli oggetti COM che risiedono in un Apartment a thread multipli possono ricevere chiamate al metodo direttamente da uno qualsiasi dei thread appartenenti all'Apartment a thread multipli. I thread in un Apartment a thread multipli utilizzano un modello denominato *Threading libero*. Le chiamate a oggetti COM in un Apartment a thread multipli vengono sincronizzate dagli oggetti stessi.

> [!Note]  
> Per una descrizione della comunicazione tra Apartment a thread singolo e Apartment con multithreading nello stesso processo, vedere [comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md).

 

Un processo può avere zero o più Apartment a thread singolo e zero o un Apartment a thread multipli.

In un processo, l'Apartment principale è il primo da inizializzare. In un processo a thread singolo, questo è l'unico Apartment. Viene eseguito il marshalling dei parametri di chiamata tra gli Apartment e COM gestisce la sincronizzazione tramite la messaggistica. Se si definiscono più thread in un processo per essere a thread libero, tutti i thread disponibili si trovano in un singolo Apartment, i parametri vengono passati direttamente a qualsiasi thread nell'Apartment ed è necessario gestire tutte le sincronizzazioni. In un processo con threading libero e threading di Apartment, tutti i thread gratuiti si trovano in un singolo Apartment e tutti gli altri appartamenti sono appartamenti a thread singolo. Un processo che esegue lavoro COM è una raccolta di appartamenti con, al massimo, un Apartment a thread multipli ma un numero qualsiasi di Apartment a thread singolo.

I modelli di threading in COM forniscono il meccanismo per i client e i server che usano architetture di threading diverse per collaborare. Le chiamate tra oggetti con modelli di threading diversi in processi diversi sono naturalmente supportate. Dal punto di vista dell'oggetto chiamante, tutte le chiamate a oggetti all'esterno di un processo si comportano in modo identico, indipendentemente dal fatto che l'oggetto chiamato sia thread. Analogamente, dal punto di vista dell'oggetto chiamato, le chiamate in arrivo si comportano in modo identico, indipendentemente dal modello di threading del chiamante.

L'interazione tra un client e un oggetto out-of-process è semplice, anche quando usano modelli di threading diversi perché il client e l'oggetto si trovano in processi diversi. COM, interposta tra il client e il server, può fornire il codice per l'interoperabilità tra i modelli di threading, usando il marshalling standard e RPC. Se, ad esempio, un oggetto a thread singolo viene chiamato contemporaneamente da più client a thread libero, le chiamate verranno sincronizzate da COM inserendo i messaggi della finestra corrispondenti nella coda di messaggi del server. L'Apartment dell'oggetto riceve una chiamata ogni volta che recupera e invia i messaggi. Tuttavia, è necessario prestare attenzione per garantire che i server in-process interagiscano correttamente con i client. (Vedere [problemi di threading del server in-process](in-process-server-threading-issues.md)).

Il problema più importante nella programmazione con un modello multithreading consiste nel rendere il codice thread-safe in modo che i messaggi destinati a un particolare thread vadano solo a tale thread e che l'accesso ai thread sia protetto.

Per altre informazioni, vedere i seguenti argomenti:

-   [Scelta del modello di threading](choosing-the-threading-model.md)
-   [Apartment a thread singolo](single-threaded-apartments.md)
-   [Apartment con multithreading](multithreaded-apartments.md)
-   [Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
-   [Problemi di threading del server in-process](in-process-server-threading-issues.md)
-   [Accesso alle interfacce tra gli Apartment](accessing-interfaces-across-apartments.md)

 

 