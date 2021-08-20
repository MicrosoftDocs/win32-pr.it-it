---
description: La classe CCmdQueue è una classe di base che fornisce una coda di oggetti CDeferredCommand e funzioni membro per aggiungere, rimuovere, controllare lo stato e richiamare i comandi in coda.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: Classe CCmdQueue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5aac6f7315df58a39d119c72fc481816bdc40aab3c449852041b7a490f22f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074405"
---
# <a name="ccmdqueue-class"></a>Classe CCmdQueue

La classe è una classe di base che fornisce una coda di `CCmdQueue` [**oggetti CDeferredCommand**](cdeferredcommand.md) e funzioni membro per aggiungere, rimuovere, controllare lo stato e richiamare i comandi in coda. Un `CCmdQueue` oggetto fa parte di un oggetto che implementa i metodi [**IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand) Il gestore del grafo dei filtri **implementa i metodi IQueueCommand** in modo che le applicazioni possano accodare i comandi al grafico dei filtri. I filtri che implementano **l'interfaccia IQueueCommand** usano direttamente questa classe. Se si vogliono usare **oggetti CDeferredCommand,** la coda deve essere derivata da questa classe.

Esistono due modalità di sincronizzazione: grosso grosso modo e accurate. In modalità grosso modo, l'applicazione attende fino all'arrivo di un orario specificato e quindi esegue il comando. In modalità accurata, l'applicazione attende l'inizio dell'elaborazione nell'esempio visualizzato al momento e quindi esegue il comando . Il filtro determina quale verrà implementato. Il gestore dei grafi dei filtri implementa sempre la modalità grosso modo per i comandi accodati nel gestore del grafico filtro.

Se si vuole una sincronizzazione grossolano, è probabile che si voglia attendere la scadenza di un comando e quindi eseguirlo. A tale scopo, chiamare [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md). Se è necessario attendere diversi elementi, ottenere l'handle dell'evento [**da CCmdQueue::GetDueHandle**](ccmdqueue-getduehandle.md) e quindi chiamare **CCmdQueue::GetDueCommand** quando viene segnalato. [**Il tempo di**](stream-time.md) flusso avanza solo tra le chiamate alle funzioni membro [**CCmdQueue::Run**](ccmdqueue-run.md) e [**CCmdQueue::EndRun.**](ccmdqueue-endrun.md) Non è garantito che se l'handle è impostato, sarà disponibile un comando pronto. Ogni volta che l'evento viene segnalato, chiamare la funzione membro **GetDueCommand** (probabilmente con un timeout pari a zero). può restituire E \_ ABORT se non è pronto alcun comando.

Per una sincronizzazione accurata, chiamare la funzione membro [**CCmdQueue::GetCommandDueFor**](ccmdqueue-getcommandduefor.md) e passare gli esempi che si sta per elaborare come parametro. Verrà restituito quanto segue:

-   Comando in tempo di flusso dovuto in corrispondenza o prima di tale ora del flusso.
-   Comando in fase di presentazione in corrispondenza o prima della presentazione dell'ora del flusso. Eseguire questa operazione solo tra le funzioni membro [**CCmdQueue::Run**](ccmdqueue-run.md) e [**CCmdQueue::EndRun,**](ccmdqueue-endrun.md) perché al di fuori di questo, il mapping dall'ora del flusso all'ora di presentazione non è noto.
-   Qualsiasi comando in fase di presentazione in scadenza.

Se si vuole una sincronizzazione accurata per gli esempi che potrebbero essere elaborati durante la modalità sospesa, è necessario usare i comandi in fase di flusso.

In tutti i casi, i comandi rimangono in coda fino a quando non vengono chiamati o annullati. L'impostazione e la reimpostazione dell'handle dell'evento vengono gestite interamente da questo oggetto coda.



| Membri dati protetti                                 | Descrizione                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bEseguimento                                            | Flag per lo stato di esecuzione; impostare **TRUE durante** l'esecuzione.                                                     |
| m \_ dwAdvise                                            | Identificatore di consulenza dall'orologio di riferimento (zero se non è presente alcuna consulenza in sospeso).                            |
| m \_ evDue                                               | Imposta l'ora di scadenza di tutti i comandi.                                                               |
| m \_ listPresentation                                    | Archivia i comandi accodati in fase di presentazione.                                                           |
| m \_ listStream                                          | Archivia i comandi accodati in tempo di flusso.                                                                 |
| m \_ Lock                                                | Protegge l'accesso agli elenchi.                                                                              |
| m \_ pClock                                              | Clock di riferimento corrente.                                                                               |
| m \_ StreamTimeOffset                                    | Contiene l'offset di tempo del flusso **quando m \_ bRunning** è **TRUE.**                                      |
| m \_ StreamTimeOffset                                    | Contiene l'offset di tempo del flusso **quando m \_ bRunning** è **TRUE.**                                      |
| Funzioni di membro                                       | Descrizione                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Costruisce un **oggetto CCmdQueue.**                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Determina se un determinato tempo è scaduto.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Recupera l'handle dell'evento che verrà segnalato.                                                      |
| Funzioni membro sottoponibili a override                           | Descrizione                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Passa alla modalità arrestata o sospesa.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Recupera un comando posticipato pianificato a un'ora specificata.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Recupera un puntatore al comando successivo in scadenza.                                                   |
| [**Inserire**](ccmdqueue-insert.md)                     | Aggiunge [**l'oggetto CDeferredCommand**](cdeferredcommand.md) alla coda.                             |
| [**Nuovo**](ccmdqueue-new.md)                           | Inizializza un comando da eseguire e restituisce un nuovo [**oggetto CDeferredCommand.**](cdeferredcommand.md) |
| [**Rimuovi**](ccmdqueue-remove.md)                     | Rimuove [**l'oggetto CDeferredCommand**](cdeferredcommand.md) dalla coda.                        |
| [**Esegui**](ccmdqueue-run.md)                           | Passa alla modalità di esecuzione.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Imposta l'orologio utilizzato per l'intervallo.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Imposta un evento timer con l'orologio di riferimento.                                                        |



 

 

 



