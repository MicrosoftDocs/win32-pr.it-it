---
title: Esecuzione della chiamata asincrona
description: Prima di poter effettuare una chiamata remota asincrona, il client deve inizializzare l'handle asincrono. I programmi client e server usano puntatori alla struttura RPC \_ ASYNC \_ STATE per gli handle asincroni.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Chiamata di procedura remota RPC, attività, esecuzione di chiamate asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928377"
---
# <a name="making-the-asynchronous-call"></a>Esecuzione della chiamata asincrona

Prima di poter effettuare una chiamata remota asincrona, il client deve inizializzare l'handle asincrono. I programmi client e server usano puntatori alla [**struttura RPC \_ ASYNC \_ STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) per gli handle asincroni.

Ogni chiamata in attesa deve avere un proprio handle asincrono univoco. Il client crea l'handle e lo passa alla [**funzione RpcAsyncInitializeHandle.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) Per il corretto completamento della chiamata, il client deve assicurarsi che la memoria per l'handle non venga rilasciata fino a quando non riceve la risposta asincrona del server. Inoltre, prima di effettuare un'altra chiamata su un handle asincrono esistente, il client deve reinizializzare l'handle. In caso negativo, lo stub del client può generare un'eccezione durante la chiamata. Il client deve anche garantire che i buffer forniti per i parametri out e in , i parametri out a una procedura remota asincrona rimangano allocati fino a quando non riceve la risposta \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in)  \] dal server.

Quando richiama una procedura remota asincrona, il client deve selezionare il metodo che verrà utilizzato dalla libreria di runtime RPC per notificare il completamento della chiamata. Il client può ricevere questa notifica in uno dei modi seguenti:

-   Evento. Il client può specificare un evento da generato al termine della chiamata. Per informazioni dettagliate, vedere [Oggetti evento.](/windows/desktop/Sync/event-objects)
-   Polling. Il client può chiamare ripetutamente [**RpcAsyncGetCallStatus.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus) Se il valore restituito è diverso da RPC \_ S \_ ASYNC \_ CALL \_ PENDING, la chiamata è completa. Questo metodo usa più tempo di CPU rispetto agli altri metodi descritti qui.
-   Apc. Il client può specificare una [chiamata di procedura asincrona (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) che viene chiamata al completamento della chiamata. Per il prototipo della funzione APC, vedere [**RPCNOTIFICATION \_ ROUTINE**](/previous-versions/aa375808(v=vs.80)). L'APC viene chiamato con il relativo parametro Event impostato su RpcCallComplete. Per l'invio delle API, il thread client deve essere in uno stato di attesa avvisabile.

    Se il **campo hThread** nell'handle asincrono è impostato su 0, le API vengono accodati nel thread che ha effettuato la chiamata asincrona. Se è diverso da zero, le API vengono accodati nel thread specificato da m.

-   Ioc. La porta di completamento dell'I/O viene notificata con i parametri specificati nell'handle asincrono. Per altre informazioni, vedere [**CreateIoCompletionPort.**](/windows/desktop/FileIO/createiocompletionport)
-   Windows handle. Viene inviato un messaggio all'handle di finestra specificato (HWND).

Il frammento di codice seguente illustra i passaggi essenziali necessari per inizializzare un handle asincrono e usarlo per effettuare una chiamata di procedura remota asincrona.


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



Come illustrato in questo esempio, il programma client può eseguire chiamate sincrone di procedura remota mentre una chiamata di procedura asincrona è ancora in sospeso. Questo client crea un oggetto evento per la libreria di runtime RPC da usare per notificare il completamento della chiamata asincrona.

> [!Note]  
> La notifica del completamento non verrà restituita da una routine RPC asincrona se viene generata un'eccezione RPC durante una chiamata asincrona.

 

 

 