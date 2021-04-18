---
description: Specifica un descrittore della coda di completamento utilizzato per la notifica di completamento I/O tramite le richieste di invio e ricezione con le estensioni I/O registrate di Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310442"
---
# <a name="rio_cq"></a><span data-ttu-id="19bbd-103">\_CQ Rio</span><span class="sxs-lookup"><span data-stu-id="19bbd-103">RIO\_CQ</span></span>

<span data-ttu-id="19bbd-104">Il typedef di **Rio \_ CQ** specifica un descrittore della coda di completamento utilizzato per la notifica di completamento i/o tramite le richieste di invio e ricezione con le estensioni i/o registrate di Winsock.</span><span class="sxs-lookup"><span data-stu-id="19bbd-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="19bbd-105">**\_CQ Rio**</span><span class="sxs-lookup"><span data-stu-id="19bbd-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="19bbd-106">Tipo di dati che specifica un descrittore della coda di completamento utilizzato per la notifica di completamento I/O dalle richieste di invio e ricezione.</span><span class="sxs-lookup"><span data-stu-id="19bbd-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19bbd-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="19bbd-107">Remarks</span></span>

<span data-ttu-id="19bbd-108">L'oggetto **Rio \_ CQ** viene utilizzato per la notifica di completamento i/o delle richieste di invio e ricezione della rete da parte delle estensioni i/o registrate di Winsock.</span><span class="sxs-lookup"><span data-stu-id="19bbd-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="19bbd-109">Un'applicazione può usare la funzione [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) per richiedere una notifica quando una coda di completamento di **Rio \_ CQ** non è vuota.</span><span class="sxs-lookup"><span data-stu-id="19bbd-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="19bbd-110">Un'applicazione può anche eseguire il polling dello stato in qualsiasi momento di una coda di completamento di **Rio \_ CQ** in modo non bloccante usando la funzione [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="19bbd-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="19bbd-111">L'oggetto **Rio \_ CQ** viene creato usando la funzione [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="19bbd-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="19bbd-112">Al momento della creazione, l'applicazione deve specificare le dimensioni della coda, che determina il numero di voci di completamento che è possibile memorizzare.</span><span class="sxs-lookup"><span data-stu-id="19bbd-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="19bbd-113">Quando un'applicazione chiama la funzione [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) per ottenere un handle di [**Rio \_ RQ**](riorqueue.md) , l'applicazione deve specificare un handle di **Rio \_ CQ** per i completamenti di invio e un handle di **Rio \_ CQ** per i completamenti della ricezione.</span><span class="sxs-lookup"><span data-stu-id="19bbd-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="19bbd-114">Questi handle possono essere identici quando è necessario utilizzare la stessa coda per il completamento dell'invio e della ricezione.</span><span class="sxs-lookup"><span data-stu-id="19bbd-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="19bbd-115">La funzione **RIOCreateRequestQueue** richiede anche un numero massimo di operazioni di invio e ricezione in attesa, che vengono addebitate in base alla capacità della coda o delle code di completamento associate.</span><span class="sxs-lookup"><span data-stu-id="19bbd-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="19bbd-116">Se la capacità rimanente per le code non è sufficiente, la chiamata di **RIOCreateRequestQueue** avrà esito negativo con [WSAENOBUFS](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="19bbd-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="19bbd-117">Il comportamento delle notifiche per una coda di completamento viene impostato al momento della creazione del **\_ CQ di Rio** .</span><span class="sxs-lookup"><span data-stu-id="19bbd-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="19bbd-118">Per una coda di completamento che usa un evento, il membro del **tipo** della struttura di [**\_ \_ completamento delle notifiche Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) viene impostato sul **\_ \_ completamento dell'evento Rio**.</span><span class="sxs-lookup"><span data-stu-id="19bbd-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="19bbd-119">Il membro **Event. EventHandle** deve contenere l'handle per un evento creato dalla funzione [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) o [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .</span><span class="sxs-lookup"><span data-stu-id="19bbd-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="19bbd-120">Per ricevere il completamento del [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l'applicazione deve attendere l'handle di evento specificato usando [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o una routine di attesa simile.</span><span class="sxs-lookup"><span data-stu-id="19bbd-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="19bbd-121">Se l'applicazione prevede di reimpostare e riutilizzare l'evento, l'applicazione può ridurre il sovraccarico impostando il membro **Event. NotifyReset** su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="19bbd-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="19bbd-122">In questo modo l'evento viene reimpostato automaticamente dalla funzione **RIONotify** quando si verifica la notifica.</span><span class="sxs-lookup"><span data-stu-id="19bbd-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="19bbd-123">In questo modo è possibile ridurre la necessità di chiamare la funzione [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) per reimpostare l'evento tra le chiamate alla funzione **RIONotify** .</span><span class="sxs-lookup"><span data-stu-id="19bbd-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="19bbd-124">Per una coda di completamento che usa una porta di completamento di I/O, il membro del **tipo** della struttura di [**\_ \_ completamento delle notifiche Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) è impostato sul **\_ \_ completamento IOCP di Rio**.</span><span class="sxs-lookup"><span data-stu-id="19bbd-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="19bbd-125">Il membro **IOCP. IocpHandle** deve contenere l'handle per una porta di completamento i/O creata dalla funzione [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) .</span><span class="sxs-lookup"><span data-stu-id="19bbd-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="19bbd-126">Per ricevere il completamento del [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l'applicazione deve chiamare la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) .</span><span class="sxs-lookup"><span data-stu-id="19bbd-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="19bbd-127">L'applicazione deve fornire un oggetto [**sovrapposto**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicato per la coda di completamento e può anche usare il membro **IOCP. CompletionKey** per distinguere le richieste **RIONotify** nella coda di completamento da altri completamenti di i/O, inclusi i completamenti **RIONotify** per altre code di completamento.</span><span class="sxs-lookup"><span data-stu-id="19bbd-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="19bbd-128">Ai fini dell'efficienza, l'accesso alle code di completamento (**struct \_ CQ** ) e le code di richiesta (struct di [**Rio \_ RQ**](riorqueue.md) ) non sono protette dalle primitive di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="19bbd-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="19bbd-129">Se è necessario accedere a una coda di completamento o di richiesta da più thread, l'accesso deve essere coordinato da una sezione critica, da un blocco Write reader sottile o da un meccanismo simile.</span><span class="sxs-lookup"><span data-stu-id="19bbd-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="19bbd-130">Questo blocco non è necessario per l'accesso da un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="19bbd-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="19bbd-131">Thread diversi possono accedere a code di completamento/richieste separate senza blocchi.</span><span class="sxs-lookup"><span data-stu-id="19bbd-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="19bbd-132">La necessità di sincronizzazione avviene solo quando più thread tentano di accedere alla stessa coda.</span><span class="sxs-lookup"><span data-stu-id="19bbd-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="19bbd-133">La sincronizzazione è necessaria anche se più thread inviano e ricevono lo stesso socket perché le operazioni di invio e ricezione utilizzano la coda di richieste del socket.</span><span class="sxs-lookup"><span data-stu-id="19bbd-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="19bbd-134">Se più thread tentano di accedere allo stesso valore di **Rio \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l'accesso deve essere coordinato da una sezione critica, da un blocco writer reader sottile o da un meccanismo di esclusione reciproca simile.</span><span class="sxs-lookup"><span data-stu-id="19bbd-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="19bbd-135">Se le code di completamento non sono condivise, l'esclusione reciproca non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="19bbd-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="19bbd-136">Quando una coda di completamento non è più necessaria, un'applicazione può chiuderla usando la funzione [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19bbd-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="19bbd-137">Il typedef di **Rio \_ CQ** è definito nel file di intestazione *Mswsockdef. h* , che viene incluso automaticamente nel file di intestazione *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="19bbd-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="19bbd-138">Il file di intestazione *Mswsockdef. h* non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="19bbd-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="19bbd-139">Thread safety</span><span class="sxs-lookup"><span data-stu-id="19bbd-139">Thread Safety</span></span>

<span data-ttu-id="19bbd-140">Se più thread tentano di accedere allo stesso valore di **Rio \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l'accesso deve essere coordinato da una sezione critica, da un blocco writer reader sottile o da un meccanismo di esclusione reciproca simile.</span><span class="sxs-lookup"><span data-stu-id="19bbd-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="19bbd-141">Se le code di completamento non sono condivise, l'esclusione reciproca non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="19bbd-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="19bbd-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19bbd-142">Requirements</span></span>



| <span data-ttu-id="19bbd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="19bbd-143">Requirement</span></span> | <span data-ttu-id="19bbd-144">Valore</span><span class="sxs-lookup"><span data-stu-id="19bbd-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19bbd-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19bbd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="19bbd-146">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="19bbd-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="19bbd-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19bbd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="19bbd-148">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="19bbd-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="19bbd-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19bbd-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="19bbd-150"><dt>Mswsockdef. h (include mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19bbd-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19bbd-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19bbd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19bbd-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="19bbd-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="19bbd-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="19bbd-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="19bbd-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="19bbd-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="19bbd-155">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="19bbd-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="19bbd-156">**OVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="19bbd-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="19bbd-157">**\_completamento notifiche \_ Rio**</span><span class="sxs-lookup"><span data-stu-id="19bbd-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="19bbd-158">**\_tipo di \_ completamento \_ notifica Rio**</span><span class="sxs-lookup"><span data-stu-id="19bbd-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="19bbd-159">**RIO \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="19bbd-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="19bbd-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19bbd-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="19bbd-161">**RIOCreateCompletionQueue**</span><span class="sxs-lookup"><span data-stu-id="19bbd-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="19bbd-162">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="19bbd-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="19bbd-163">**RIODequeueCompletion**</span><span class="sxs-lookup"><span data-stu-id="19bbd-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="19bbd-164">**RIONotify**</span><span class="sxs-lookup"><span data-stu-id="19bbd-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="19bbd-165">**WSACreateEvent**</span><span class="sxs-lookup"><span data-stu-id="19bbd-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="19bbd-166">**WSAResetEvent**</span><span class="sxs-lookup"><span data-stu-id="19bbd-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="19bbd-167">**WSAWaitForMultipleEvents**</span><span class="sxs-lookup"><span data-stu-id="19bbd-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
