---
description: La classe CMsgThread è una classe thread di lavoro che accoda le richieste al thread di accodamento per il completamento in modo asincrono.
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
ms.openlocfilehash: 021683808900a7265f4708dae0bb29ff6d07f6619430ed5687eb77d5e2332a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813701"
---
# <a name="cmsgthread-class"></a>Classe CMsgThread

La classe è una classe thread di lavoro che accoda le richieste al thread di accodamento `CMsgThread` per il completamento in modo asincrono. Per usare questa classe, derivare la classe da essa ed eseguire l'override della funzione membro [**CMsgThread::ThreadMessageProc.**](cmsgthread-threadmessageproc.md) La **funzione membro ThreadMessageProc** esegue ogni richiesta. Le funzioni client e la **funzione membro ThreadMessageProc** devono condividere una definizione comune dei parametri nell'oggetto [**CMsg.**](cmsg.md)

Un meccanismo negoziato indica al thread di lavoro di uscire. In genere, si tratta di un valore del codice [**del messaggio uMsg**](cmsg.md) della classe **CMsg.**

È buona idea inviare questo messaggio dal distruttore della classe derivata e chiamare la funzione membro [**CMsgThread::WaitForThreadExit**](cmsgthread-waitforthreadexit.md) prima di completare la distruzione della classe derivata.



| Membri dati protetti                                    | Descrizione                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | Indica un handle usato per la segnalazione.                                                                                                |
| m \_ Lock                                                   | Protegge l'accesso agli elenchi.                                                                                                             |
| m \_ lWaiting                                               | Indica l'attesa di un thread libero.                                                                                                  |
| m \_ ThreadQueue                                            | Esegue l'override della funzione membro [**CMsgThread::GetThreadMsg**](cmsgthread-getthreadmsg.md) e si blocca su elementi diversi da questa coda. |
| Funzioni di membro                                          | Descrizione                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Costruisce un **oggetto CMsgThread.**                                                                                                   |
| [**Createthread**](cmsgthread-createthread.md)           | Crea un thread.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Recupera l'handle del thread.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Recupera l'identificatore del thread.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Recupera la priorità del thread corrente.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Accoda una richiesta di esecuzione da parte del thread di lavoro.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Continua l'operazione del thread di lavoro.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Imposta la priorità del thread su un nuovo valore.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Sospende l'operazione di un thread in esecuzione.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Si blocca fino alla chiusura del thread dopo una chiamata alla funzione membro [**CMsgThread::SuspendThread.**](cmsgthread-suspendthread.md) |
| Funzioni membro sottoponibili a override                              | Descrizione                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Recupera un oggetto [**CMsg in coda**](cmsg.md) contenente una richiesta.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Fornisce l'inizializzazione in un thread.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Elabora le richieste. Si tratta di una funzione membro virtuale pura.                                                                           |



 

 

 



