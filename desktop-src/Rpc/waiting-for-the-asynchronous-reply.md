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
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="912b3-104">In attesa della risposta asincrona</span><span class="sxs-lookup"><span data-stu-id="912b3-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="912b3-105">L'operazione eseguita dal client mentre è in attesa di ricevere una risposta dal server dipende dal meccanismo di notifica selezionato.</span><span class="sxs-lookup"><span data-stu-id="912b3-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="912b3-106">Se il client usa un evento per la notifica, in genere chiama la funzione [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o la funzione [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) .</span><span class="sxs-lookup"><span data-stu-id="912b3-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="912b3-107">Il client entra in uno stato bloccato quando chiama una di queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="912b3-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="912b3-108">Questa operazione è efficace perché il client non usa cicli di esecuzione della CPU mentre è bloccato.</span><span class="sxs-lookup"><span data-stu-id="912b3-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="912b3-109">Quando usa il polling per attendere i risultati, il programma client immette un ciclo che chiama ripetutamente la funzione [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="912b3-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="912b3-110">Si tratta di un metodo efficace per attendere se il programma client esegue altre operazioni di elaborazione nel ciclo di polling.</span><span class="sxs-lookup"><span data-stu-id="912b3-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="912b3-111">È ad esempio possibile preparare i dati in piccoli blocchi per una chiamata di procedura remota asincrona successiva.</span><span class="sxs-lookup"><span data-stu-id="912b3-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="912b3-112">Al termine di ogni blocco, il client può eseguire il polling della chiamata di procedura remota asincrona in attesa per verificare se è stata completata.</span><span class="sxs-lookup"><span data-stu-id="912b3-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="912b3-113">Il programma client può fornire una chiamata di procedura asincrona (APC), ovvero un tipo di funzione di callback che verrà richiamata dalla libreria di runtime RPC al completamento della chiamata asincrona remota.</span><span class="sxs-lookup"><span data-stu-id="912b3-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="912b3-114">Il programma client deve essere in uno stato di attesa di avviso.</span><span class="sxs-lookup"><span data-stu-id="912b3-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="912b3-115">Ciò significa in genere che il client chiama una funzione API di Windows per inserirsi in uno stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="912b3-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="912b3-116">Per ulteriori informazioni, vedere [chiamate di procedure asincrone](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="912b3-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="912b3-117">La notifica del completamento non verrà restituita da una routine RPC asincrona se viene generata un'eccezione RPC durante una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="912b3-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="912b3-118">Se il programma client usa una porta di completamento di I/O per ricevere la notifica di completamento, deve chiamare la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="912b3-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="912b3-119">Quando si esegue questa operazione, è possibile attendere indefinitamente una risposta o continuare a eseguire altre operazioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="912b3-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="912b3-120">Se esegue altre elaborazioni durante l'attesa di una risposta, deve eseguire il polling della porta di completamento con la funzione **GetQueuedCompletionStatus** .</span><span class="sxs-lookup"><span data-stu-id="912b3-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="912b3-121">In questo caso, è in genere necessario impostare *dwMilliseconds* su zero.</span><span class="sxs-lookup"><span data-stu-id="912b3-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="912b3-122">In questo modo, **GetQueuedCompletionStatus** restituirà immediatamente, anche se la chiamata asincrona non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="912b3-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="912b3-123">I programmi client possono inoltre ricevere notifiche di completamento tramite le relative code di messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="912b3-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="912b3-124">In questa situazione, elaborano semplicemente il messaggio di completamento come tutti i messaggi di Windows.</span><span class="sxs-lookup"><span data-stu-id="912b3-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="912b3-125">In un'applicazione multithread, una chiamata asincrona può essere annullata dal client solo dopo che il thread che ha originato la chiamata è stato restituito correttamente dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="912b3-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="912b3-126">Ciò garantisce che la chiamata non venga annullata in modo asincrono da un altro thread dopo che ha avuto esito negativo una chiamata sincrona.</span><span class="sxs-lookup"><span data-stu-id="912b3-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="912b3-127">Come procedura standard, una chiamata asincrona che ha esito negativo in modo sincrono non deve essere annullata in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="912b3-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="912b3-128">L'applicazione client deve osservare questo comportamento se le chiamate possono essere emesse e annullate su thread diversi.</span><span class="sxs-lookup"><span data-stu-id="912b3-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="912b3-129">Inoltre, dopo che la chiamata è stata annullata, il codice client deve attendere la notifica di completamento e completare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="912b3-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="912b3-130">La funzione [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) scorre semplicemente la notifica di completamento; non è un sostituto per il completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="912b3-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="912b3-131">Nel frammento di codice seguente viene illustrato come un programma client può utilizzare un evento per attendere una risposta asincrona.</span><span class="sxs-lookup"><span data-stu-id="912b3-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="912b3-132">I programmi client che usano un APC per ricevere una notifica di una risposta asincrona si trovano in genere in uno stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="912b3-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="912b3-133">Il frammento di codice seguente mostra questo.</span><span class="sxs-lookup"><span data-stu-id="912b3-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="912b3-134">In questo caso, il programma client passa alla modalità di sospensione, consumando nessun ciclo della CPU, finché la libreria di runtime RPC non chiama l'APC (non mostrato).</span><span class="sxs-lookup"><span data-stu-id="912b3-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="912b3-135">Nell'esempio seguente viene illustrato un client che utilizza una porta di completamento di I/O per attendere una risposta asincrona.</span><span class="sxs-lookup"><span data-stu-id="912b3-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


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



<span data-ttu-id="912b3-136">Nell'esempio precedente, la chiamata a [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) attende per un periodo di tempo illimitato fino al completamento della chiamata asincrona di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="912b3-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="912b3-137">Un potenziale problema si verifica durante la scrittura di applicazioni multithread.</span><span class="sxs-lookup"><span data-stu-id="912b3-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="912b3-138">Se un thread richiama una chiamata di procedura remota e termina prima di ricevere una notifica che l'invio è stato completato, la chiamata di procedura remota potrebbe non riuscire e lo stub client potrebbe chiudere la connessione al server.</span><span class="sxs-lookup"><span data-stu-id="912b3-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="912b3-139">Pertanto, i thread che chiamano una procedura remota non devono terminare prima del completamento o dell'annullamento della chiamata quando il comportamento è indesiderato.</span><span class="sxs-lookup"><span data-stu-id="912b3-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 