---
title: In attesa della risposta asincrona
description: L'operazione eseguita dal client mentre è in attesa di ricevere una risposta dal server dipende dal meccanismo di notifica selezionato.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- RPC (Remote Procedure Call), attività, in attesa di risposte asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338478"
---
# <a name="waiting-for-the-asynchronous-reply"></a>In attesa della risposta asincrona

L'operazione eseguita dal client mentre è in attesa di ricevere una risposta dal server dipende dal meccanismo di notifica selezionato.

Se il client usa un evento per la notifica, in genere chiama la funzione [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o la funzione [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) . Il client entra in uno stato bloccato quando chiama una di queste funzioni. Questa operazione è efficace perché il client non usa cicli di esecuzione della CPU mentre è bloccato.

Quando usa il polling per attendere i risultati, il programma client immette un ciclo che chiama ripetutamente la funzione [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Si tratta di un metodo efficace per attendere se il programma client esegue altre operazioni di elaborazione nel ciclo di polling. È ad esempio possibile preparare i dati in piccoli blocchi per una chiamata di procedura remota asincrona successiva. Al termine di ogni blocco, il client può eseguire il polling della chiamata di procedura remota asincrona in attesa per verificare se è stata completata.

Il programma client può fornire una chiamata di procedura asincrona (APC), ovvero un tipo di funzione di callback che verrà richiamata dalla libreria di runtime RPC al completamento della chiamata asincrona remota. Il programma client deve essere in uno stato di attesa di avviso. Ciò significa in genere che il client chiama una funzione API di Windows per inserirsi in uno stato bloccato. Per ulteriori informazioni, vedere [chiamate di procedure asincrone](/windows/desktop/Sync/asynchronous-procedure-calls).

> [!Note]  
> La notifica del completamento non verrà restituita da una routine RPC asincrona se viene generata un'eccezione RPC durante una chiamata asincrona.

 

Se il programma client usa una porta di completamento di I/O per ricevere la notifica di completamento, deve chiamare la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Quando si esegue questa operazione, è possibile attendere indefinitamente una risposta o continuare a eseguire altre operazioni di elaborazione. Se esegue altre elaborazioni durante l'attesa di una risposta, deve eseguire il polling della porta di completamento con la funzione **GetQueuedCompletionStatus** . In questo caso, è in genere necessario impostare *dwMilliseconds* su zero. In questo modo, **GetQueuedCompletionStatus** restituirà immediatamente, anche se la chiamata asincrona non è stata completata.

I programmi client possono inoltre ricevere notifiche di completamento tramite le relative code di messaggi della finestra. In questa situazione, elaborano semplicemente il messaggio di completamento come tutti i messaggi di Windows.

In un'applicazione multithread, una chiamata asincrona può essere annullata dal client solo dopo che il thread che ha originato la chiamata è stato restituito correttamente dalla chiamata. Ciò garantisce che la chiamata non venga annullata in modo asincrono da un altro thread dopo che ha avuto esito negativo una chiamata sincrona. Come procedura standard, una chiamata asincrona che ha esito negativo in modo sincrono non deve essere annullata in modo asincrono. L'applicazione client deve osservare questo comportamento se le chiamate possono essere emesse e annullate su thread diversi. Inoltre, dopo che la chiamata è stata annullata, il codice client deve attendere la notifica di completamento e completare la chiamata. La funzione [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) scorre semplicemente la notifica di completamento; non è un sostituto per il completamento della chiamata.

Nel frammento di codice seguente viene illustrato come un programma client può utilizzare un evento per attendere una risposta asincrona.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



I programmi client che usano un APC per ricevere una notifica di una risposta asincrona si trovano in genere in uno stato bloccato. Il frammento di codice seguente mostra questo.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



In questo caso, il programma client passa alla modalità di sospensione, consumando nessun ciclo della CPU, finché la libreria di runtime RPC non chiama l'APC (non mostrato).

Nell'esempio seguente viene illustrato un client che utilizza una porta di completamento di I/O per attendere una risposta asincrona.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



Nell'esempio precedente, la chiamata a [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) attende per un periodo di tempo illimitato fino al completamento della chiamata asincrona di procedura remota.

Un potenziale problema si verifica durante la scrittura di applicazioni multithread. Se un thread richiama una chiamata di procedura remota e termina prima di ricevere una notifica che l'invio è stato completato, la chiamata di procedura remota potrebbe non riuscire e lo stub client potrebbe chiudere la connessione al server. Pertanto, i thread che chiamano una procedura remota non devono terminare prima del completamento o dell'annullamento della chiamata quando il comportamento è indesiderato.

 

 