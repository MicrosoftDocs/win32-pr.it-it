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
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="a5350-105">Creazione della chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="a5350-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="a5350-106">Prima di poter effettuare una chiamata remota asincrona, il client deve inizializzare l'handle asincrono.</span><span class="sxs-lookup"><span data-stu-id="a5350-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="a5350-107">I programmi client e server utilizzano i puntatori alla struttura di [**\_ \_ stato asincrono RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) per gli handle asincroni.</span><span class="sxs-lookup"><span data-stu-id="a5350-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="a5350-108">Ogni chiamata in attesa deve avere un proprio handle asincrono univoco.</span><span class="sxs-lookup"><span data-stu-id="a5350-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="a5350-109">Il client crea l'handle e lo passa alla funzione [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) .</span><span class="sxs-lookup"><span data-stu-id="a5350-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="a5350-110">Affinché la chiamata venga completata correttamente, il client deve garantire che la memoria per l'handle non venga rilasciata finché non riceve la risposta asincrona del server.</span><span class="sxs-lookup"><span data-stu-id="a5350-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="a5350-111">Inoltre, prima di eseguire un'altra chiamata su un handle asincrono esistente, il client deve reinizializzare l'handle.</span><span class="sxs-lookup"><span data-stu-id="a5350-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="a5350-112">Questa operazione può causare la generazione di un'eccezione da parte dello stub del client durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="a5350-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="a5350-113">Il client deve inoltre assicurarsi che i buffer forniti per i parametri \[ [**out**](/windows/desktop/Midl/out-idl) \] e \[ [**in**](/windows/desktop/Midl/in), i parametri **out** \] di una procedura remota asincrona rimangano allocati fino a quando non riceve la risposta dal server.</span><span class="sxs-lookup"><span data-stu-id="a5350-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="a5350-114">Quando richiama una procedura remota asincrona, il client deve selezionare il metodo che verrà usato dalla libreria di runtime RPC per notificare il completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a5350-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="a5350-115">Il client può ricevere questa notifica in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5350-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="a5350-116">Evento.</span><span class="sxs-lookup"><span data-stu-id="a5350-116">Event.</span></span> <span data-ttu-id="a5350-117">Il client può specificare un evento da generare al termine della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a5350-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="a5350-118">Per informazioni dettagliate, vedere [oggetti evento](/windows/desktop/Sync/event-objects).</span><span class="sxs-lookup"><span data-stu-id="a5350-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="a5350-119">Polling.</span><span class="sxs-lookup"><span data-stu-id="a5350-119">Polling.</span></span> <span data-ttu-id="a5350-120">Il client può chiamare ripetutamente [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="a5350-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="a5350-121">Se il valore restituito è diverso dalla \_ \_ chiamata asincrona di RPC \_ \_ in sospeso, la chiamata è completa.</span><span class="sxs-lookup"><span data-stu-id="a5350-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="a5350-122">Questo metodo usa più tempo della CPU rispetto agli altri metodi descritti qui.</span><span class="sxs-lookup"><span data-stu-id="a5350-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="a5350-123">APC.</span><span class="sxs-lookup"><span data-stu-id="a5350-123">APC.</span></span> <span data-ttu-id="a5350-124">Il client può specificare una [chiamata di procedura asincrona (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) che viene chiamata al completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a5350-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="a5350-125">Per il prototipo della funzione APC, vedere [**\_ routine RPCNOTIFICATION**](/previous-versions/aa375808(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="a5350-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="a5350-126">L'APC viene chiamato con il parametro di evento impostato su RpcCallComplete.</span><span class="sxs-lookup"><span data-stu-id="a5350-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="a5350-127">Affinché APC venga inviato, il thread del client deve essere in uno stato di attesa di avviso.</span><span class="sxs-lookup"><span data-stu-id="a5350-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="a5350-128">Se il campo **hThread** nell'handle asincrono è impostato su 0, il APC viene accodato nel thread che ha effettuato la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="a5350-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="a5350-129">Se è diverso da zero, i APC vengono accodati nel thread specificato da m.</span><span class="sxs-lookup"><span data-stu-id="a5350-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="a5350-130">IOC.</span><span class="sxs-lookup"><span data-stu-id="a5350-130">IOC.</span></span> <span data-ttu-id="a5350-131">La porta di completamento I/O riceve una notifica con i parametri specificati nell'handle asincrono.</span><span class="sxs-lookup"><span data-stu-id="a5350-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="a5350-132">Per ulteriori informazioni, vedere [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span><span class="sxs-lookup"><span data-stu-id="a5350-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="a5350-133">Handle di Windows.</span><span class="sxs-lookup"><span data-stu-id="a5350-133">Windows handle.</span></span> <span data-ttu-id="a5350-134">Un messaggio viene inserito nell'handle di finestra specificato (HWND).</span><span class="sxs-lookup"><span data-stu-id="a5350-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="a5350-135">Nel frammento di codice seguente vengono illustrati i passaggi essenziali necessari per inizializzare un handle asincrono e utilizzarlo per eseguire una chiamata di procedura remota asincrona.</span><span class="sxs-lookup"><span data-stu-id="a5350-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


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



<span data-ttu-id="a5350-136">Come illustrato in questo esempio, il programma client può eseguire chiamate di procedure remote sincrone mentre una chiamata di procedura asincrona è ancora in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a5350-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="a5350-137">Questo client crea un oggetto evento per la libreria di runtime RPC da usare per inviare una notifica al completamento della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="a5350-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="a5350-138">La notifica del completamento non verrà restituita da una routine RPC asincrona se viene generata un'eccezione RPC durante una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="a5350-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 