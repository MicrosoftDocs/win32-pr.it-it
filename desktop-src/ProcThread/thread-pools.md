---
description: Un pool di thread è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Pool di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7918a0f6f0b881233ebea8e664d6e743a7bff105e265270063b08af313417e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081261"
---
# <a name="thread-pools"></a>Pool di thread

Un *pool di thread* è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione. Il pool di thread viene usato principalmente per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro. Le applicazioni possono accodre elementi di lavoro, associare il lavoro agli handle waitable, accodarsi automaticamente in base a un timer ed eseguire l'associazione con I/O.

## <a name="thread-pool-architecture"></a>Architettura del pool di thread

Le applicazioni seguenti possono trarre vantaggio dall'uso di un pool di thread:

-   Un'applicazione altamente parallela e in grado di inviare un numero elevato di piccoli elementi di lavoro in modo asincrono, ad esempio la ricerca di indici distribuiti o l'I/O di rete.
-   Applicazione che crea ed elimina un numero elevato di thread eseguiti per un breve periodo di tempo. L'uso del pool di thread può ridurre la complessità della gestione dei thread e l'overhead necessario per la creazione e la distruzione dei thread.
-   Applicazione che elabora elementi di lavoro indipendenti in background e in parallelo, ad esempio il caricamento di più schede.
-   Applicazione che deve eseguire un'attesa esclusiva sugli oggetti del kernel o bloccare gli eventi in ingresso su un oggetto . L'uso del pool di thread può ridurre la complessità della gestione dei thread e aumentare le prestazioni riducendo il numero di commutatori di contesto.
-   Applicazione che crea thread del waiter personalizzati per l'attesa degli eventi.

Il pool di thread originale è stato completamente riarchitetto in Windows Vista. Il nuovo pool di thread è stato migliorato perché fornisce un singolo tipo di thread di lavoro (supporta sia I/O che non I/O), non usa un thread timer, fornisce una singola coda timer e fornisce un thread permanente dedicato. Offre anche gruppi di pulizia, prestazioni più elevate, più pool per processo pianificati in modo indipendente e una nuova API del pool di thread.

L'architettura del pool di thread è costituita dai seguenti elementi:

-   Thread di lavoro che eseguono le funzioni di callback
-   Thread del waiter in attesa di più handle di attesa
-   Coda di lavoro
-   Un pool di thread predefinito per ogni processo
-   Una worker factory che gestisce i thread di lavoro

## <a name="best-practices"></a>Procedure consigliate

La nuova [API del pool di thread](thread-pool-api.md) offre maggiore flessibilità e controllo rispetto all'API del pool di thread [originale.](thread-pooling.md) Esistono tuttavia alcune differenze sottili ma importanti. Nell'API originale la reimpostazione dell'attesa era automatica. nella nuova API, l'attesa deve essere reimpostata in modo esplicito ogni volta. L'API originale ha gestito automaticamente la rappresentazione, trasferendo il contesto di sicurezza del processo chiamante al thread. Con la nuova API, l'applicazione deve impostare in modo esplicito il contesto di sicurezza.

Di seguito sono riportate le procedure consigliate quando si usa un pool di thread:

-   I thread di un processo condividono il pool di thread. Un singolo thread di lavoro può eseguire più funzioni di callback, una alla volta. Questi thread di lavoro sono gestiti dal pool di thread. Pertanto, non terminare un thread dal pool di thread chiamando [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) sul thread o chiamando [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) da una funzione di callback.
-   Una richiesta di I/O può essere eseguita su qualsiasi thread nel pool di thread. L'annullamento dell'I/O in un thread del pool di thread richiede la sincronizzazione perché la funzione di annullamento potrebbe essere eseguita in un thread diverso da quello che gestisce la richiesta di I/O, che può comportare l'annullamento di un'operazione sconosciuta. Per evitare questo problema, fornire sempre la struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) con cui è stata avviata una richiesta di I/O quando si chiama [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) per operazioni di I/O asincrone oppure usare la propria sincronizzazione per assicurarsi che nessun altro I/O possa essere avviato nel thread di destinazione prima di chiamare la funzione [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) **o CancelIoEx.**
-   Pulire tutte le risorse create nella funzione di callback prima di restituire dalla funzione. Sono inclusi TLS, i contesti di sicurezza, la priorità dei thread e la registrazione COM. Le funzioni di callback devono anche ripristinare lo stato del thread prima di restituire .
-   Mantenere attivi gli handle di attesa e gli oggetti associati fino a quando il pool di thread non ha segnalato che è stato completato con l'handle.
-   Contrassegnare tutti i thread in attesa di operazioni di lunga durata (ad esempio scaricamenti di I/O o pulizia delle risorse) in modo che il pool di thread possa allocare nuovi thread anziché attendere questo.
-   Prima di scaricare una DLL che usa il pool di thread, annullare tutti gli elementi di lavoro, l'I/O, le operazioni di attesa e i timer e attendere il completamento dell'esecuzione dei callback.
-   Evitare i deadlock eliminando le dipendenze tra gli elementi di lavoro e tra i callback, assicurando che un callback non sia in attesa del completamento e mantenendo la priorità del thread.
-   Non accoda troppi elementi troppo rapidamente in un processo con altri componenti che usano il pool di thread predefinito. Esiste un pool di thread predefinito per ogni processo, incluso Svchost.exe. Per impostazione predefinita, ogni pool di thread ha un massimo di 500 thread di lavoro. Il pool di thread tenta di creare più thread di lavoro quando il numero di thread di lavoro nello stato pronto/in esecuzione deve essere inferiore al numero di processori.
-   Evitare il modello di apartment a thread singolo COM, perché non è compatibile con il pool di thread. STA crea lo stato del thread che può influire sull'elemento di lavoro successivo per il thread. STA è in genere di lunga durata e ha affinità di thread, che è l'opposto del pool di thread.
-   Creare un nuovo pool di thread per controllare la priorità e l'isolamento dei thread, creare caratteristiche personalizzate ed eventualmente migliorare la velocità di risposta. Tuttavia, i pool di thread aggiuntivi richiedono più risorse di sistema (thread, memoria del kernel). Un numero eccessivo di pool aumenta il potenziale di una l'insicuzione della CPU.
-   Se possibile, usare un oggetto waitable anziché un meccanismo basato su APC per segnalare un thread del pool di thread. Le API non funzionano anche con i thread del pool di thread come altri meccanismi di segnalazione perché il sistema controlla la durata dei thread del pool di thread, quindi è possibile che un thread venga terminato prima che venga recapitata la notifica.
-   Usare l'estensione del debugger del pool di thread, !tp. Questo comando ha l'utilizzo seguente:

    -   flag *di indirizzo del* *pool*
    -   flag di *indirizzo*  obj
    -   Flag di *indirizzo della* *coda*
    -   indirizzo *del* waiter
    -   indirizzo del *ruolo di lavoro*

    Per pool, waiter e worker, se l'indirizzo è zero, il comando esegue il dump di tutti gli oggetti. Per il waiter e il ruolo di lavoro, l'omissione dell'indirizzo esegue il dump del thread corrente. Vengono definiti i flag seguenti: 0x1 (output a riga singola), 0x2 (membri dump) e 0x4 (coda di lavoro del pool di dump).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread Pool API](thread-pool-api.md)
</dt> <dt>

[Uso delle funzioni del pool di thread](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
