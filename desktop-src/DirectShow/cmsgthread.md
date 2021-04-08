---
description: La classe CMsgThread è una classe thread di lavoro che accoda le richieste al thread di Accodamento per il completamento in modo asincrono.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: Classe CMsgThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 307b24e1563fe0545ee6f9405f9fb53e1b6d61b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747551"
---
# <a name="cmsgthread-class"></a>Classe CMsgThread

La `CMsgThread` classe è una classe thread di lavoro che accoda le richieste al thread di Accodamento per il completamento in modo asincrono. Per usare questa classe, derivare la classe da essa ed eseguire l'override della funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) . La funzione membro **ThreadMessageProc** esegue ogni richiesta. Le funzioni client e la funzione membro **ThreadMessageProc** devono condividere una definizione comune dei parametri nell'oggetto [**CMsg**](cmsg.md) .

Un meccanismo negoziato indica al thread di lavoro di uscire. Si tratta in genere di un valore del codice del messaggio **uMsg** della classe [**CMsg**](cmsg.md) .

È consigliabile inviare questo messaggio dal distruttore della classe derivata e chiamare la funzione membro [**CMsgThread:: WaitForThreadExit**](cmsgthread-waitforthreadexit.md) prima di completare la distruzione della classe derivata.



| Membri dati protetti                                    | Descrizione                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| \_hSem m                                                   | Indica un handle utilizzato per la segnalazione.                                                                                                |
| \_blocco m                                                   | Protegge l'accesso agli elenchi.                                                                                                             |
| \_lWaiting m                                               | Indica che è in attesa di un thread libero.                                                                                                  |
| \_ThreadQueue m                                            | Esegue l'override della funzione membro [**CMsgThread:: GetThreadMsg**](cmsgthread-getthreadmsg.md) e blocca su elementi diversi da questa coda. |
| Funzioni di membro                                          | Descrizione                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Costruisce un oggetto **CMsgThread** .                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Crea un thread.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Recupera l'handle del thread.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Recupera l'identificatore del thread.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Recupera la priorità del thread corrente.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Accoda una richiesta di esecuzione da parte del thread di lavoro.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Continua l'operazione del thread di lavoro.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Imposta la priorità del thread su un nuovo valore.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Sospende l'operazione di un thread in esecuzione.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Si blocca fino a quando il thread non è stato terminato dopo una chiamata alla funzione membro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) . |
| Funzioni membro sottoponibili a override                              | Descrizione                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Recupera un oggetto [**CMsg**](cmsg.md) in coda contenente una richiesta.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Fornisce l'inizializzazione su un thread.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Elabora le richieste. Si tratta di una funzione membro virtuale pura.                                                                           |



 

 

 



