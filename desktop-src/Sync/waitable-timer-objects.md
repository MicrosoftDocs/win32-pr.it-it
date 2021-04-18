---
description: Un oggetto timer che può essere atteso è un oggetto di sincronizzazione il cui stato è impostato su segnalato quando arriva il tempo di scadenza specificato.
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: Oggetti timer waitable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316060"
---
# <a name="waitable-timer-objects"></a>Oggetti timer waitable

Un *oggetto timer* che può essere atteso è un oggetto di sincronizzazione il cui stato è impostato su segnalato quando arriva il tempo di scadenza specificato. È possibile creare due tipi di timer che è possibile attendere, ovvero la reimpostazione manuale e la sincronizzazione. Un timer di uno dei due tipi può anche essere un timer periodico.



| Oggetto                | Descrizione                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| timer di reimpostazione manuale    | Timer il cui stato rimane segnalato fino a quando non viene chiamato [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) per stabilire una nuova ora di scadenza.                                                                          |
| timer di sincronizzazione | Timer il cui stato rimane segnalato fino al completamento di un'operazione di attesa sull'oggetto timer da parte di un thread.                                                                                                     |
| timer periodico        | Timer che viene riattivato ogni volta che il periodo specificato scade, fino a quando il timer viene reimpostato o annullato. Un timer periodico è un timer di reimpostazione manuale periodico o un timer di sincronizzazione periodico. |



 

> [!Note]  
> Quando viene segnalato un timer, il processore deve eseguire per elaborare le istruzioni associate. I timer periodici ad alta frequenza mantengono il processore sempre occupato, impedendo al sistema di rimanere in uno [stato di alimentazione](../power/system-power-states.md) inferiore per un periodo di tempo significativo. Ciò può avere un impatto negativo sulla durata della batteria dei computer portatili e sugli scenari che dipendono da un risparmio energia efficace, ad esempio Data Center di grandi dimensioni. Per una maggiore efficienza energetica, è consigliabile usare notifiche basate su eventi anziché notifiche basate sul tempo nell'applicazione. Se è necessario un timer, utilizzare un timer segnalato una volta anziché un timer periodico oppure impostare l'intervallo su un valore maggiore di un secondo.

 

Un thread usa la funzione [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) o [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) per creare un oggetto timer. Il thread di creazione specifica se il timer è un timer di reimpostazione manuale o un timer di sincronizzazione. Il thread di creazione può specificare un nome per l'oggetto timer. I thread di altri processi possono aprire un handle per un timer esistente specificandone il nome in una chiamata alla funzione [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Qualsiasi thread con un handle a un oggetto timer può utilizzare una delle [funzioni di attesa](wait-functions.md) per attendere che lo stato del timer sia impostato su segnalato.

-   Il thread chiama la funzione [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) per attivare il timer. Si noti l'uso dei parametri seguenti per **SetWaitableTimer**:
-   Usare il parametro *lpDueTime* per specificare l'ora in cui deve essere impostato il timer sullo stato segnalato. Quando un timer di reimpostazione manuale è impostato sullo stato segnalato, rimane in questo stato fino a quando [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) non stabilisce un nuovo tempo di scadenza. Quando un timer di sincronizzazione è impostato sullo stato segnalato, rimane in questo stato fino al completamento di un'operazione di attesa sull'oggetto timer da parte di un thread.
-   Usare il parametro *lPeriod* della funzione [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) per specificare il periodo del timer. Se il periodo è diverso da zero, il timer è un timer periodico; viene riattivato ogni volta che il periodo scade, fino a quando il timer viene reimpostato o annullato. Se il punto è zero, il timer non è un timer periodico; viene segnalato una volta e quindi disattivato.

Un thread può utilizzare la funzione [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) per impostare il timer sullo stato inattivo. Per reimpostare il timer, chiamare [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Al termine dell'oggetto timer, chiamare [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) per chiudere l'handle per l'oggetto timer.

Il comportamento di un timer waitable può essere riepilogato come segue:

-   Quando viene impostato un timer, questo viene annullato se era già attivo, lo stato del timer è non segnalato e il timer viene inserito nella coda del timer del kernel.
-   Quando un timer scade, il timer viene impostato sullo stato segnalato. Se il timer ha una routine di completamento, viene accodato al thread che ha impostato il timer. La routine di completamento rimane nella coda della [chiamata di procedura asincrona](asynchronous-procedure-calls.md) (APC) del thread finché il thread non entra in uno stato di attesa di avviso. A questo punto, l'APC viene inviato e viene chiamata la routine di completamento. Se il timer è periodico, viene inserito nuovamente nella coda del timer del kernel.
-   Quando un timer viene annullato, viene rimosso dalla coda del timer del kernel se è in sospeso. Se il timer è scaduto ed esiste ancora una coda APC al thread che ha impostato il timer, l'APC viene rimosso dalla coda APC del thread. Lo stato segnalato del timer non è interessato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamate di procedure asincrone](asynchronous-procedure-calls.md)
</dt> <dt>

[Uso di oggetti timer waitable](using-waitable-timer-objects.md)
</dt> </dl>

 

 
