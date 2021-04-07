---
description: Sono disponibili molte applicazioni che creano thread che impiegano molto tempo nello stato di sospensione in attesa del verificarsi di un evento.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Pooling dei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf3565401dc57b077e333043861d42b683e810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881693"
---
# <a name="thread-pooling"></a>Pooling dei thread

Sono disponibili molte applicazioni che creano thread che impiegano molto tempo nello stato di sospensione in attesa del verificarsi di un evento. Gli altri thread possono entrare in uno stato di sospensione solo per essere riattivati periodicamente per eseguire il polling di una modifica o aggiornare le informazioni sullo stato. Il *pool di thread* consente di usare i thread in modo più efficiente fornendo all'applicazione un pool di thread di lavoro gestiti dal sistema. Almeno un thread monitora lo stato di tutte le operazioni di attesa accodate al pool di thread. Al termine di un'operazione di attesa, un thread di lavoro del pool di thread esegue la funzione di callback corrispondente.

Questo argomento descrive l'API del pool di thread originale. L'API del pool di thread introdotta in Windows Vista è più semplice, più affidabile, offre prestazioni migliori e offre maggiore flessibilità per gli sviluppatori. Per informazioni sull'API del pool di thread corrente, vedere [pool di thread](thread-pools.md).

È anche possibile accodare gli elementi di lavoro che non sono correlati a un'operazione di attesa al pool di thread. Per richiedere che un elemento di lavoro venga gestito da un thread nel pool di thread, chiamare la funzione [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) . Questa funzione accetta un parametro per la funzione che verrà chiamata dal thread selezionato dal pool di thread. Non è possibile annullare un elemento di lavoro dopo che è stato accodato.

[Timer:](../sync/timer-queues.md) i timer della coda e [le operazioni di attesa registrate](../sync/wait-functions.md) utilizzano anche il pool di thread. Le funzioni di callback vengono accodate al pool di thread. È anche possibile usare la funzione [**BindIoCompletionCallback ha provocato**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) per inviare operazioni di I/O asincrone. Al completamento dell'i/O, il callback viene eseguito da un thread del pool di thread.

Il pool di thread viene creato la prima volta che si chiama [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) o [**BindIoCompletionCallback ha provocato**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)o quando un timer-coda timer o un'operazione di attesa registrata Accoda una funzione di callback. Per impostazione predefinita, il numero di thread che è possibile creare nel pool di thread è pari a circa 500. Ogni thread usa le dimensioni predefinite dello stack e viene eseguito con la priorità predefinita.

Esistono due tipi di thread di lavoro nel pool di thread: I/O e non-I/O. Un *thread di lavoro di I/O* è un thread che attende uno stato di attesa di avviso. Gli elementi di lavoro vengono accodati ai thread di lavoro di I/O come chiamate di procedure asincrone (APC). È necessario accodare un elemento di lavoro a un thread di lavoro di I/O se deve essere eseguito in un thread che attende in uno stato di avviso.

Un *thread di lavoro non di i/o* è in attesa sulle porte di completamento i/o. L'utilizzo di thread di lavoro non di I/O è più efficiente rispetto all'utilizzo di thread di lavoro di I/O. Pertanto, quando possibile, è consigliabile utilizzare thread di lavoro non di I/O. I thread di lavoro di I/O e non di I/O non terminano se sono presenti richieste di I/O asincrone in sospeso. Entrambi i tipi di thread possono essere utilizzati da elementi di lavoro che avviano richieste di completamento I/O asincrone. Evitare tuttavia di inviare richieste di completamento I/O asincrone nei thread di lavoro non di I/O se il completamento potrebbe richiedere molto tempo.

Per usare il pool di thread, gli elementi di lavoro e tutte le funzioni che chiamano devono essere sicuri del pool di thread. Una funzione Safe non presuppone che il thread che lo esegue sia un thread dedicato o persistente. In generale, è consigliabile evitare di usare l' [archiviazione locale di thread](thread-local-storage.md) o effettuare una chiamata asincrona che richiede un thread persistente, ad esempio la funzione [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) . Tuttavia, tali funzioni possono essere chiamate su un thread dedicato (creato dall'applicazione) o accodate a un thread di lavoro permanente (usando [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) con l' \_ opzione WT EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[I/O Alertable](../fileio/alertable-i-o.md)
</dt> <dt>

[Chiamate di procedure asincrone](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Porte di completamento I/O](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Pool di thread](thread-pools.md)
</dt> </dl>

 

 
