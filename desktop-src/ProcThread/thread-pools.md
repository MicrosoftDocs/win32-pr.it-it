---
description: Un pool di thread è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Pool di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690aa3eb6fd3ce7a99d71e0f57118529ef79113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313318"
---
# <a name="thread-pools"></a>Pool di thread

Un *pool di thread* è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione. Il pool di thread viene utilizzato principalmente per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro. Le applicazioni possono accodare gli elementi di lavoro, associare il lavoro con handle waitable, accodarsi automaticamente in base a un timer e associarli all'I/O.

## <a name="thread-pool-architecture"></a>Architettura del pool di thread

Le applicazioni seguenti possono trarre vantaggio dall'utilizzo di un pool di thread:

-   Applicazione altamente parallela che può inviare un numero elevato di piccoli elementi di lavoro in modo asincrono, ad esempio ricerca di indici distribuiti o I/O di rete.
-   Applicazione che crea ed elimina un numero elevato di thread eseguiti per un breve periodo di tempo. L'utilizzo del pool di thread può ridurre la complessità della gestione dei thread e l'overhead necessario per la creazione e la distruzione di thread.
-   Applicazione che elabora gli elementi di lavoro indipendenti in background e in parallelo (ad esempio il caricamento di più schede).
-   Un'applicazione che deve eseguire un'attesa esclusiva sugli oggetti kernel o bloccare gli eventi in ingresso in un oggetto. L'utilizzo del pool di thread può ridurre la complessità della gestione dei thread e migliorare le prestazioni riducendo il numero di cambi di contesto.
-   Applicazione che crea thread del cameriere personalizzati da attendere per gli eventi.

Il pool di thread originale è stato completamente riprogettato in Windows Vista. Il nuovo pool di thread è migliorato perché fornisce un solo tipo di thread di lavoro (supporta le I/O e non I/O), non utilizza un thread del timer, fornisce una sola coda del timer e fornisce un thread permanente dedicato. Fornisce inoltre gruppi di pulitura, prestazioni più elevate, più pool per processo pianificati in modo indipendente e una nuova API del pool di thread.

L'architettura del pool di thread è costituita dagli elementi seguenti:

-   Thread di lavoro che eseguono le funzioni di callback
-   Thread del cameriere che attendono più handle di attesa
-   Coda di lavoro
-   Un pool di thread predefinito per ogni processo
-   Una factory di lavoro che gestisce i thread di lavoro

## <a name="best-practices"></a>Procedure consigliate

La nuova [API del pool di thread](thread-pool-api.md) offre maggiore flessibilità e controllo rispetto all' [API originale del pool di thread](thread-pooling.md). Tuttavia, esistono alcune differenze minime ma importanti. Nell'API originale il ripristino delle attese era automatico; nella nuova API, l'attesa deve essere reimpostata in modo esplicito ogni volta. L'API originale ha gestito automaticamente la rappresentazione, trasferendo il contesto di sicurezza del processo chiamante al thread. Con la nuova API, l'applicazione deve impostare in modo esplicito il contesto di sicurezza.

Di seguito sono illustrate le procedure consigliate per l'utilizzo di un pool di thread:

-   I thread di un processo condividono il pool di thread. Un singolo thread di lavoro può eseguire più funzioni di callback, una alla volta. Questi thread di lavoro vengono gestiti dal pool di thread. Pertanto, non terminare un thread dal pool di thread chiamando [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) sul thread o chiamando [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) da una funzione di callback.
-   Una richiesta di I/O può essere eseguita in qualsiasi thread del pool di thread. Per annullare l'I/O su un thread del pool di thread è necessaria la sincronizzazione perché la funzione Cancel può essere eseguita su un thread diverso da quello che gestisce la richiesta di I/O, operazione che può causare l'annullamento di un'operazione sconosciuta. Per evitare questo problema, fornire sempre la struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) a cui è stata avviata una richiesta di i/o durante la chiamata di [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) per l'i/o asincrono oppure utilizzare la sincronizzazione personalizzata per assicurarsi che non sia possibile avviare altre operazioni di i/o nel thread di destinazione prima di chiamare la funzione [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) o **CancelIoEx** .
-   Eseguire la pulizia di tutte le risorse create nella funzione di callback prima di restituire dalla funzione. Sono inclusi TLS, contesti di sicurezza, priorità dei thread e registrazione COM. Le funzioni di callback devono inoltre ripristinare lo stato del thread prima di restituire.
-   Mantiene attivi gli handle di attesa e gli oggetti associati fino a quando il pool di thread non ha segnalato che è terminato con l'handle.
-   Contrassegnare tutti i thread in attesa di operazioni lunghe, ad esempio gli scaricamenti di I/O o la pulizia delle risorse, in modo che il pool di thread possa allocare nuovi thread invece di attendere questo.
-   Prima di scaricare una DLL che usa il pool di thread, annullare tutti gli elementi di lavoro, le operazioni di I/O, le operazioni di attesa e i timer e attendere il completamento dell'esecuzione dei callback.
-   Evitare i deadlock eliminando le dipendenze tra gli elementi di lavoro e tra i callback, garantendo che un callback non sia in attesa del completamento e mantenendo la priorità del thread.
-   Non accodare troppi elementi troppo rapidamente in un processo con altri componenti che usano il pool di thread predefinito. È presente un pool di thread predefinito per processo, incluso Svchost.exe. Per impostazione predefinita, ogni pool di thread ha un massimo di 500 thread di lavoro. Il pool di thread tenta di creare più thread di lavoro quando il numero di thread di lavoro nello stato pronto/in esecuzione deve essere inferiore al numero di processori.
-   Evitare il modello di Apartment a thread singolo COM, perché non è compatibile con il pool di thread. STA creando lo stato del thread che può influire sull'elemento di lavoro successivo per il thread. Sta in genere di lunga durata e presenta affinità di thread, che è l'opposto del pool di thread.
-   Creare un nuovo pool di thread per controllare la priorità e l'isolamento del thread, creare caratteristiche personalizzate e possibilmente migliorare la velocità di risposta. Tuttavia, i pool di thread aggiuntivi richiedono più risorse di sistema (thread, memoria kernel). Troppi pool aumentano il rischio di contesa di CPU.
-   Se possibile, usare un oggetto waitable anziché un meccanismo basato su APC per segnalare un thread del pool di thread. APC non funzionano anche con i thread del pool di thread come altri meccanismi di segnalazione, perché il sistema controlla la durata dei thread del pool di thread, quindi è possibile che un thread venga terminato prima che la notifica venga recapitata.
-   Utilizzare l'estensione del debugger del pool di thread,! TP. Questo comando presenta il seguente utilizzo:

    -   *flag* di *indirizzi* del pool
    -   *flag* di *indirizzi* obj
    -   flag *indirizzi*  TImpossibile creare
    -   *Indirizzo* del cameriere
    -   *Indirizzo* di lavoro

    Per il pool, il cameriere e il ruolo di lavoro, se l'indirizzo è zero, il comando eseguirà il dump di tutti gli oggetti. Per il cameriere e il ruolo di lavoro, omettendo l'indirizzo viene eseguito il dump del thread corrente. Vengono definiti i flag seguenti: 0x1 (output su una sola riga), 0x2 (membri dump) e 0x4 (dump coda di lavoro pool).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API del pool di thread](thread-pool-api.md)
</dt> <dt>

[Uso delle funzioni del pool di thread](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
