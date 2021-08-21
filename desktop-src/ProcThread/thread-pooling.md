---
description: Esistono molte applicazioni che creano thread che impiegano molto tempo nello stato di sospensione in attesa che si verifichi un evento.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Pooling dei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c581e416952e6bac14dbf12a8f87202925a5254879b7e220c7cb2d780699f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081281"
---
# <a name="thread-pooling"></a>Pooling dei thread

Esistono molte applicazioni che creano thread che impiegano molto tempo nello stato di sospensione in attesa che si verifichi un evento. Altri thread possono entrare in uno stato di sospensione solo per essere svegliati periodicamente per eseguire il polling di una modifica o aggiornare le informazioni sullo stato. *Il pool di thread* consente di usare i thread in modo più efficiente fornendo all'applicazione un pool di thread di lavoro gestiti dal sistema. Almeno un thread monitora lo stato di tutte le operazioni di attesa accodati al pool di thread. Al termine di un'operazione di attesa, un thread di lavoro del pool di thread esegue la funzione di callback corrispondente.

Questo argomento descrive l'API del pool di thread originale. L'API del pool di thread introdotta in Windows Vista è più semplice, affidabile, offre prestazioni migliori e offre maggiore flessibilità per gli sviluppatori. Per informazioni sull'API del pool di thread corrente, vedere [Pool di thread](thread-pools.md).

È anche possibile accodare al pool di thread gli elementi di lavoro non correlati a un'operazione di attesa. Per richiedere che un elemento di lavoro sia gestito da un thread nel pool di thread, chiamare la [**funzione QueueUserWorkItem.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) Questa funzione accetta un parametro per la funzione che verrà chiamata dal thread selezionato dal pool di thread. Non è possibile annullare un elemento di lavoro dopo che è stato accodato.

[Anche i timer della coda timer](../sync/timer-queues.md) e le operazioni di attesa [registrate](../sync/wait-functions.md) usano il pool di thread. Le funzioni di callback vengono accodati al pool di thread. È anche possibile usare la [**funzione BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) per pubblicare operazioni di I/O asincrone. Al completamento dell'I/O, il callback viene eseguito da un thread del pool di thread.

Il pool di thread viene creato la prima volta che si chiama [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) o [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)oppure quando un timer della coda timer o un'operazione di attesa registrata accoda una funzione di callback. Per impostazione predefinita, il numero di thread che è possibile creare nel pool di thread è di circa 500. Ogni thread usa le dimensioni predefinite dello stack e viene eseguito con la priorità predefinita.

Nel pool di thread sono disponibili due tipi di thread di lavoro: I/O e non I/O. Un *thread di lavoro di I/O* è un thread in attesa in uno stato di attesa avvisabile. Gli elementi di lavoro vengono accodati ai thread di lavoro di I/O come chiamate di procedura asincrone (APC). È consigliabile accodare un elemento di lavoro a un thread di lavoro di I/O se deve essere eseguito in un thread in attesa in uno stato di avviso.

Un *thread di lavoro non di I/O* attende le porte di completamento dell'I/O. L'uso di thread di lavoro non di I/O è più efficiente rispetto all'uso di thread di lavoro di I/O. È pertanto consigliabile usare thread di lavoro non di I/O quando possibile. I thread di lavoro di I/O e non di I/O non vengono terminati se sono presenti richieste di I/O asincrone in sospeso. Entrambi i tipi di thread possono essere usati dagli elementi di lavoro che avviano richieste di completamento I/O asincrone. Evitare tuttavia di pubblicare richieste di completamento I/O asincrone nei thread di lavoro non di I/O se il completamento potrebbe richiedere molto tempo.

Per usare il pooling di thread, gli elementi di lavoro e tutte le funzioni chiamate devono essere thread-pool safe. Una funzione sicura non presuppone che il thread che la esegue sia un thread dedicato o permanente. In generale, è consigliabile evitare di usare l'archiviazione locale del [thread](thread-local-storage.md) o di effettuare una chiamata asincrona che richiede un thread permanente, ad esempio la funzione [**RegNotifyChangeKeyValue.**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) Tuttavia, tali funzioni possono essere chiamate su un thread dedicato (creato dall'applicazione) o accodate a un thread di lavoro permanente (usando [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) con l'opzione WT \_ EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[I/O con avvisi](../fileio/alertable-i-o.md)
</dt> <dt>

[Chiamate di procedura asincrone](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Porte di completamento I/O](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Pool di thread](thread-pools.md)
</dt> </dl>

 

 
