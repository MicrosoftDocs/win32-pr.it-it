---
title: Creazione della chiamata asincrona
description: Prima di poter effettuare una chiamata remota asincrona, il client deve inizializzare l'handle asincrono. I programmi client e server utilizzano i puntatori alla \_ struttura di stato asincrono RPC \_ per gli handle asincroni.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- RPC (Remote Procedure Call), attività, esecuzione di chiamate asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300146"
---
# <a name="making-the-asynchronous-call"></a>Creazione della chiamata asincrona

Prima di poter effettuare una chiamata remota asincrona, il client deve inizializzare l'handle asincrono. I programmi client e server utilizzano i puntatori alla struttura di [**\_ \_ stato asincrono RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) per gli handle asincroni.

Ogni chiamata in attesa deve avere un proprio handle asincrono univoco. Il client crea l'handle e lo passa alla funzione [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) . Affinché la chiamata venga completata correttamente, il client deve garantire che la memoria per l'handle non venga rilasciata finché non riceve la risposta asincrona del server. Inoltre, prima di eseguire un'altra chiamata su un handle asincrono esistente, il client deve reinizializzare l'handle. Questa operazione può causare la generazione di un'eccezione da parte dello stub del client durante la chiamata. Il client deve inoltre assicurarsi che i buffer forniti per i parametri \[ [**out**](/windows/desktop/Midl/out-idl) \] e \[ [**in**](/windows/desktop/Midl/in), i parametri **out** \] di una procedura remota asincrona rimangano allocati fino a quando non riceve la risposta dal server.

Quando richiama una procedura remota asincrona, il client deve selezionare il metodo che verrà usato dalla libreria di runtime RPC per notificare il completamento della chiamata. Il client può ricevere questa notifica in uno dei modi seguenti:

-   Evento. Il client può specificare un evento da generare al termine della chiamata. Per informazioni dettagliate, vedere [oggetti evento](/windows/desktop/Sync/event-objects).
-   Polling. Il client può chiamare ripetutamente [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Se il valore restituito è diverso dalla \_ \_ chiamata asincrona di RPC \_ \_ in sospeso, la chiamata è completa. Questo metodo usa più tempo della CPU rispetto agli altri metodi descritti qui.
-   APC. Il client può specificare una [chiamata di procedura asincrona (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) che viene chiamata al completamento della chiamata. Per il prototipo della funzione APC, vedere [**\_ routine RPCNOTIFICATION**](/previous-versions/aa375808(v=vs.80)). L'APC viene chiamato con il parametro di evento impostato su RpcCallComplete. Affinché APC venga inviato, il thread del client deve essere in uno stato di attesa di avviso.

    Se il campo **hThread** nell'handle asincrono è impostato su 0, il APC viene accodato nel thread che ha effettuato la chiamata asincrona. Se è diverso da zero, i APC vengono accodati nel thread specificato da m.

-   IOC. La porta di completamento I/O riceve una notifica con i parametri specificati nell'handle asincrono. Per ulteriori informazioni, vedere [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   Handle di Windows. Un messaggio viene inserito nell'handle di finestra specificato (HWND).

Nel frammento di codice seguente vengono illustrati i passaggi essenziali necessari per inizializzare un handle asincrono e utilizzarlo per eseguire una chiamata di procedura remota asincrona.


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



Come illustrato in questo esempio, il programma client può eseguire chiamate di procedure remote sincrone mentre una chiamata di procedura asincrona è ancora in sospeso. Questo client crea un oggetto evento per la libreria di runtime RPC da usare per inviare una notifica al completamento della chiamata asincrona.

> [!Note]  
> La notifica del completamento non verrà restituita da una routine RPC asincrona se viene generata un'eccezione RPC durante una chiamata asincrona.

 

 

 