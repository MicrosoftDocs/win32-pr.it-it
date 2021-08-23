---
description: Una chiamata di procedura asincrona (APC) è una funzione che viene eseguita in modo asincrono nel contesto di un thread specifico.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Chiamate di procedura asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c024506c2afc9a895db645fd386ed76f915f6e1178c6b8ce3a257aa7d40fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661451"
---
# <a name="asynchronous-procedure-calls"></a>Chiamate di procedura asincrone

Una *chiamata di procedura asincrona* (APC) è una funzione che viene eseguita in modo asincrono nel contesto di un thread specifico. Quando un APC viene accodato a un thread, il sistema genera un interrupt software. Alla successiva pianificazione del thread, verrà eseguita la funzione APC. Un APC generato dal sistema è denominato *APC in modalità kernel.* Un APC generato da un'applicazione è detto *APC in modalità utente.* Un thread deve essere in uno stato di avviso per eseguire un APC in modalità utente.

Ogni thread ha la propria coda APC. Un'applicazione accoda un APC a un thread chiamando la [**funzione QueueUserAPC.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) Il thread chiamante specifica l'indirizzo di una funzione APC nella chiamata a **QueueUserAPC.** L'accodamento di un APC è una richiesta che il thread chiami la funzione APC.

Quando un APC in modalità utente viene accodato, il thread a cui viene accodato non viene indirizzato a chiamare la funzione APC a meno che non si trova in uno stato di avviso. Un thread entra in uno stato di avviso quando chiama la funzione [**SleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex) [**SignalObjectAndWait,**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) [**MsgWaitForMultipleObjectsEx,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)o [**WaitForSingleObjectEx.**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) Se l'attesa viene soddisfatta prima che l'APC venga accodato, il thread non è più in uno stato di attesa avvisabile, quindi la funzione APC non verrà eseguita. Tuttavia, L'APC è ancora in coda, quindi la funzione APC verrà eseguita quando il thread chiama un'altra funzione di attesa avvisabile.

Le [**funzioni ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer), [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) vengono implementate usando un APC come meccanismo di callback della notifica di completamento.

Se si usa un pool di [thread,](../procthread/thread-pools.md)si noti che le API non funzionano così come altri meccanismi di segnalazione perché il sistema controlla la durata dei thread del pool di thread, quindi è possibile che un thread venga terminato prima che la notifica venga recapitata. Anziché usare un meccanismo di segnalazione basato su APC, ad esempio il *parametro pfnCompletionRoutine* di [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) o [**SetWaitableTimerEx,**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)usare un oggetto waitable, ad esempio un timer creato con [**CreateThreadpoolTimer.**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer) Per I/O, usare un oggetto di completamento I/O creato con [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) o una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) basata su *hEvent* in cui l'evento può essere passato alla [**funzione SetThreadpoolWait.**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)

## <a name="synchronization-internals"></a>Componenti interni di sincronizzazione

Quando viene emessa una richiesta di I/O, viene allocata una struttura per rappresentare la richiesta. Questa struttura è detta pacchetto di richiesta di I/O (IRP). Con l'I/O sincrono, il thread compila il componente IRP, lo invia nello stack del dispositivo e attende nel kernel il completamento dell'IRP. Con l'I/O asincrono, il thread compila l'IRP e lo invia nello stack del dispositivo. Lo stack potrebbe completare immediatamente l'IRP oppure potrebbe restituire uno stato in sospeso che indica che la richiesta è in corso. In questo caso, l'IRP è ancora associato al thread, quindi verrà annullato se il thread termina o chiama una funzione, ad esempio [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio). Nel frattempo, il thread può continuare a eseguire altre attività mentre lo stack di dispositivi continua a elaborare il componente IRP.

Esistono diversi modi in cui il sistema può indicare che l'IRP è stato completato:

-   Aggiornare la struttura sovrapposta con il risultato dell'operazione in modo che il thread possa eseguire il polling per determinare se l'operazione è stata completata.
-   Segnalare l'evento nella struttura sovrapposta in modo che un thread possa sincronizzarsi sull'evento e essere svegliato al termine dell'operazione.
-   Accodare l'IRP all'APC in sospeso del thread in modo che il thread eseere la routine APC quando entra in uno stato di attesa avvisabile e restituirà dall'operazione di attesa uno stato che indica che ha eseguito una o più routine APC.
-   Accodare il protocollo IRP a una porta di completamento di I/O, in cui verrà eseguito dal thread successivo che attende sulla porta di completamento.

I thread in attesa su una porta di completamento I/O non attendono in uno stato di avviso. Pertanto, se tali thread emettere IRP impostati per il completamento come API per il thread, tali completamenti IPC non verranno eseguiti in modo corretto. si verificano solo se il thread riceve una richiesta dalla porta di completamento I/O e quindi immette un'attesa avvisabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un timer waitable con una chiamata di procedura asincrona](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
