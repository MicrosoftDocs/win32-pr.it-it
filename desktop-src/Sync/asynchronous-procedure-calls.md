---
description: Una chiamata di procedura asincrona (APC) è una funzione che viene eseguita in modo asincrono nel contesto di un thread specifico.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Chiamate di procedure asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd95e9afd663e2a462335b3c47bfe99462b449e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967999"
---
# <a name="asynchronous-procedure-calls"></a>Chiamate di procedure asincrone

Una *chiamata di procedura asincrona* (APC) è una funzione che viene eseguita in modo asincrono nel contesto di un thread specifico. Quando un APC viene accodato a un thread, il sistema emette un interrupt software. La volta successiva che il thread viene pianificato, verrà eseguita la funzione APC. Un APC generato dal sistema viene definito APC in *modalità kernel*. Un APC generato da un'applicazione viene definito *APC in modalità utente*. Un thread deve essere in uno stato di avviso per eseguire un'APC in modalità utente.

Ogni thread ha una propria coda APC. Un'applicazione Accoda un APC a un thread chiamando la funzione [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) . Il thread chiamante specifica l'indirizzo di una funzione APC nella chiamata a **QueueUserAPC**. L'accodamento di un APC è una richiesta per il thread per chiamare la funzione APC.

Quando un APC in modalità utente viene accodato, il thread in cui viene accodato non viene indirizzato per chiamare la funzione APC a meno che non si trovi in uno stato di avviso. Un thread entra in uno stato di avviso quando chiama la funzione [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)o [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) . Se l'attesa viene soddisfatta prima che l'APC venga accodato, il thread non è più in uno stato di attesa di avviso, quindi la funzione APC non verrà eseguita. Tuttavia, l'APC viene ancora accodato, quindi la funzione APC viene eseguita quando il thread chiama un'altra funzione di attesa di avviso.

Le funzioni [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer), [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) vengono implementate usando un APC come meccanismo di callback della notifica di completamento.

Se si usa un [pool di thread](../procthread/thread-pools.md), si noti che APC non funziona, oltre ad altri meccanismi di segnalazione, perché il sistema controlla la durata dei thread del pool di thread, quindi è possibile che un thread venga terminato prima che la notifica venga recapitata. Anziché usare un meccanismo di segnalazione basato su APC, ad esempio il parametro *pfnCompletionRoutine* di [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) o [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex), usare un oggetto waitable, ad esempio un timer creato con [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer). Per I/O, usare un oggetto di completamento I/O creato con [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) o una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) basata su *hEvent* in cui l'evento può essere passato alla funzione [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait) .

## <a name="synchronization-internals"></a>Elementi interni di sincronizzazione

Quando viene eseguita una richiesta di I/O, viene allocata una struttura per rappresentare la richiesta. Questa struttura è chiamata pacchetto di richiesta di I/O (IRP). Con l'I/O sincrono, il thread compila l'IRP, lo invia allo stack del dispositivo e attende che il pacchetto IRP venga completato. Con l'I/O asincrono, il thread compila l'IRP e lo invia allo stack del dispositivo. Lo stack potrebbe completare immediatamente il pacchetto IRP oppure potrebbe restituire uno stato in sospeso che indica che la richiesta è in corso. In questo caso, l'oggetto IRP è ancora associato al thread, quindi verrà annullato se il thread termina o chiama una funzione come [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio). Nel frattempo, il thread può continuare a eseguire altre attività mentre lo stack del dispositivo continua a elaborare l'IRP.

Esistono diversi modi in cui il sistema può indicare che l'IRP è stato completato:

-   Aggiornare la struttura sovrapposta con il risultato dell'operazione in modo che il thread possa eseguire il polling per determinare se l'operazione è stata completata.
-   Segnala l'evento nella struttura sovrapposta in modo che un thread possa essere sincronizzato nell'evento e venga riattivato al completamento dell'operazione.
-   Accodare l'oggetto IRP all'APC in sospeso del thread in modo che il thread esegua la routine APC quando entra in uno stato di attesa di avviso e restituisca l'operazione di attesa con uno stato che indica che ha eseguito una o più routine APC.
-   Accodare l'oggetto IRP a una porta di completamento I/O, in cui verrà eseguito dal thread successivo che attende la porta di completamento.

I thread che attendono una porta di completamento di I/O non attendono uno stato di avviso. Pertanto, se i thread rilasciano IRP impostati per il completamento come APC al thread, tali completamenti IPC non verranno eseguiti in modo tempestivo; si verificheranno solo se il thread preleva una richiesta dalla porta di completamento I/O e quindi si verifica l'immissione di un'attesa di avviso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un timer waitable con una chiamata di procedura asincrona](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
