---
title: In attesa della risposta asincrona
description: Le attività del client durante l'attesa della notifica di una risposta dal server dipendono dal meccanismo di notifica selezionato.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- RPC Remote Procedure Call, attività, in attesa di risposte asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff50357402d96c32444f077d07558c01ed93d0367514e947643a28bf3041f204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010479"
---
# <a name="waiting-for-the-asynchronous-reply"></a>In attesa della risposta asincrona

Le attività del client durante l'attesa della notifica di una risposta dal server dipendono dal meccanismo di notifica selezionato.

Se il client usa un evento per la notifica, in genere chiama la [**funzione WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForSingleObjectEx.**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) Il client entra in uno stato bloccato quando chiama una di queste funzioni. Ciò è efficiente perché il client non utilizza cicli di esecuzione della CPU mentre è bloccato.

Quando usa il polling per attendere i risultati, il programma client entra in un ciclo che chiama ripetutamente la funzione [**RpcAsyncGetCallStatus.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus) Si tratta di un metodo efficiente di attesa se il programma client esegue altre elaborazioni nel ciclo di polling. Ad esempio, può preparare i dati in piccoli blocchi per una chiamata di procedura remota asincrona successiva. Al termine di ogni blocco, il client può eseguire il polling della chiamata di procedura remota asincrona in attesa per verificare se è stata completata.

Il programma client può fornire una chiamata di procedura asincrona (APC), ovvero un tipo di funzione di callback che la libreria di runtime RPC richiama al termine della chiamata di procedura remota asincrona. Il programma client deve essere in uno stato di attesa avvisabile. Ciò significa in genere che il client chiama Windows funzione API per impostare se stesso in uno stato bloccato. Per altre informazioni, vedere [Chiamate di procedura asincrone.](/windows/desktop/Sync/asynchronous-procedure-calls)

> [!Note]  
> La notifica del completamento non verrà restituita da una routine RPC asincrona se viene generata un'eccezione RPC durante una chiamata asincrona.

 

Se il programma client usa una porta di completamento I/O per ricevere la notifica di completamento, deve chiamare la [**funzione GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) In questo caso, può attendere una risposta per un periodo illimitato o continuare a eseguire altre operazioni di elaborazione. Se esegue altre operazioni di elaborazione durante l'attesa di una risposta, deve eseguire il polling della porta di completamento con **la funzione GetQueuedCompletionStatus.** In questo caso, in genere deve impostare *dwMilliseconds* su zero. In questo **modo GetQueuedCompletionStatus** viene restituito immediatamente, anche se la chiamata asincrona non è stata completata.

I programmi client possono anche ricevere notifiche di completamento tramite le code di messaggi della finestra. In questo caso, elaborano semplicemente il messaggio di completamento come qualsiasi Windows messaggio.

In un'applicazione multithreading una chiamata asincrona può essere annullata dal client solo dopo che il thread che ha originato la chiamata è stato restituito correttamente dalla chiamata. In questo modo si garantisce che la chiamata non sia annullata in modo asincrono da un altro thread dopo l'esito negativo di una chiamata sincrona. Come procedura standard, una chiamata asincrona che ha esito negativo in modo sincrono non deve essere annullata in modo asincrono. L'applicazione client deve osservare questo comportamento se è possibile eseguire e annullare chiamate su thread diversi. Inoltre, dopo l'annullamento della chiamata, il codice client deve attendere la notifica di completamento e completare la chiamata. La [**funzione RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) si limita a inviare la notifica di completamento. non sostituisce il completamento della chiamata.

Nel frammento di codice seguente viene illustrato come un programma client può utilizzare un evento per attendere una risposta asincrona.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



I programmi client che usano un APC per ricevere la notifica di una risposta asincrona si trovano in genere in uno stato bloccato. Il frammento di codice seguente illustra questa operazione.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



In questo caso, il programma client passa alla sospensione, senza cicli di CPU, fino a quando la libreria di runtime RPC non chiama il comando APC (non visualizzato).

L'esempio seguente illustra un client che usa una porta di completamento I/O per attendere una risposta asincrona.


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



Nell'esempio precedente la chiamata a [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) attende per un periodo illimitato fino al completamento della chiamata asincrona di procedura remota.

Un potenziale problema si verifica quando si scrivono applicazioni multithreading. Se un thread richiama una chiamata di procedura remota e termina prima di ricevere la notifica del completamento dell'invio, la chiamata di procedura remota potrebbe non riuscire e lo stub del client potrebbe chiudere la connessione al server. Pertanto, i thread che chiamano una procedura remota non devono terminare prima che la chiamata venga completata o annullata quando il comportamento è indesiderato.

 

 