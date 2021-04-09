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
ms.openlocfilehash: 78af7a975d54ba832bbdf1fb7f8027f87b747660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123765"
---
# <a name="ccmdqueue-class"></a>Classe CCmdQueue

La `CCmdQueue` classe è una classe di base che fornisce una coda di oggetti [**CDeferredCommand**](cdeferredcommand.md) e funzioni membro per aggiungere, rimuovere, controllare lo stato e richiamare i comandi in coda. Un `CCmdQueue` oggetto fa parte di un oggetto che implementa i metodi [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . Filter Graph Manager implementa i metodi **IQueueCommand** in modo che le applicazioni possano accodare i comandi al grafo del filtro. I filtri che implementano l'interfaccia **IQueueCommand** usano direttamente questa classe. Se si desidera utilizzare oggetti **CDeferredCommand** , è necessario che la coda derivi da questa classe.

Sono disponibili due modalità di sincronizzazione: grossolana e accurata. In modalità grossolana, l'applicazione attende fino a quando non arriva un orario specificato e quindi esegue il comando. In modalità accurata, l'applicazione attende fino a quando l'elaborazione non inizia nell'esempio visualizzato al momento, quindi esegue il comando. Il filtro determina quale implementazione verrà implementata. Filter Graph Manager implementa sempre la modalità grossolana per i comandi in coda in gestione grafico dei filtri.

Se si desidera una sincronizzazione grossolana, è probabile che si desideri attendere fino a quando non è presente un comando, quindi eseguirlo. È possibile eseguire questa operazione chiamando [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md). Se sono presenti diversi aspetti da attendere, ottenere l'handle dell'evento da [**CCmdQueue:: GetDueHandle**](ccmdqueue-getduehandle.md) e quindi chiamare **CCmdQueue:: GetDueCommand** quando questo viene segnalato. il [**tempo di flusso**](stream-time.md) viene anticipato solo tra le chiamate alle funzioni membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) . Non esiste alcuna garanzia che se l'handle è impostato, sarà pronto un comando. Ogni volta che l'evento viene segnalato, chiamare la funzione membro **GetDueCommand** (probabilmente con un timeout di zero); Questo può restituire E \_ interrompere se nessun comando è pronto.

Se si vuole sincronizzare con precisione, chiamare la funzione membro [**CCmdQueue:: GetCommandDueFor**](ccmdqueue-getcommandduefor.md) e passare gli esempi che verranno elaborati come parametro. Viene restituito quanto segue:

-   Un comando in fase di flusso dovuto a o prima del tempo di flusso.
-   Comando in fase di presentazione dovuto a o prima della presentazione del tempo del flusso. Eseguire questa operazione solo tra le funzioni membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) , perché al di fuori di questo, il mapping dal tempo di flusso al tempo di presentazione non è noto.
-   Qualsiasi comando della fase di presentazione ora.

Se si desidera sincronizzare accuratamente gli esempi che potrebbero essere elaborati in modalità di sospensione, è necessario utilizzare i comandi in fase di flusso.

In tutti i casi, i comandi rimangono accodati fino a quando non viene chiamato o annullato. L'impostazione e la reimpostazione dell'handle di evento sono gestite interamente da questo oggetto Queue.



| Membri dati protetti                                 | Descrizione                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ Bruning                                            | Flag per lo stato di esecuzione; impostare **true** durante l'esecuzione di.                                                     |
| \_dwAdvise m                                            | Identificatore di notifica dal clock di riferimento (zero se nessun avviso in attesa).                            |
| \_evDue m                                               | Imposta l'ora in cui i comandi sono dovuti.                                                               |
| \_listPresentation m                                    | Archivia i comandi accodati in fase di presentazione.                                                           |
| \_listStream m                                          | Archivia i comandi accodati nel tempo di flusso.                                                                 |
| \_blocco m                                                | Protegge l'accesso agli elenchi.                                                                              |
| \_pClock m                                              | Clock di riferimento corrente.                                                                               |
| \_StreamTimeOffset m                                    | Contiene l'offset dell'ora del flusso quando **m \_ Brunne** è **true**.                                      |
| \_StreamTimeOffset m                                    | Contiene l'offset dell'ora del flusso quando **m \_ Brunne** è **true**.                                      |
| Funzioni di membro                                       | Descrizione                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Costruisce un oggetto **CCmdQueue** .                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Determina se un dato tempo è dovuto.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Recupera l'handle dell'evento che verrà segnalato.                                                      |
| Funzioni membro sottoponibili a override                           | Descrizione                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Passa alla modalità arrestata o sospesa.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Recupera un comando posticipato pianificato a un'ora specificata.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Recupera un puntatore al comando successivo che è dovuto a.                                                   |
| [**Insert**](ccmdqueue-insert.md)                     | Aggiunge l'oggetto [**CDeferredCommand**](cdeferredcommand.md) alla coda.                             |
| [**Nuova**](ccmdqueue-new.md)                           | Inizializza un comando da eseguire e restituisce un nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) . |
| [**Rimuovi**](ccmdqueue-remove.md)                     | Rimuove l'oggetto [**CDeferredCommand**](cdeferredcommand.md) dalla coda.                        |
| [**Correre**](ccmdqueue-run.md)                           | Passa alla modalità di esecuzione.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Imposta l'orologio usato per la temporizzazione.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Imposta un evento del timer con l'orologio di riferimento.                                                        |



 

 

 



