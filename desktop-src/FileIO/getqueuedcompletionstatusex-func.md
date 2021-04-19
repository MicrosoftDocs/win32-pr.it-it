---
description: Recupera più voci di porta di completamento simultaneamente.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Funzione GetQueuedCompletionStatusEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317790"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="58edc-103">GetQueuedCompletionStatusEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="58edc-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="58edc-104">Recupera più voci di porta di completamento simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="58edc-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="58edc-105">Attende il completamento delle operazioni di I/O in sospeso associate alla porta di completamento specificata.</span><span class="sxs-lookup"><span data-stu-id="58edc-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="58edc-106">Per rimuovere dalla coda I pacchetti di completamento I/O uno alla volta, utilizzare la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="58edc-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="58edc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58edc-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="58edc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58edc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58edc-109">*Tentato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58edc-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58edc-110">Handle per la porta di completamento.</span><span class="sxs-lookup"><span data-stu-id="58edc-110">A handle to the completion port.</span></span> <span data-ttu-id="58edc-111">Per creare una porta di completamento, utilizzare la funzione [**CreateIoCompletionPort**](createiocompletionport.md) .</span><span class="sxs-lookup"><span data-stu-id="58edc-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="58edc-112">*lpCompletionPortEntries* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58edc-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58edc-113">In fase di input punta a una matrice preallocata di strutture di [**\_ immissione sovrapposte**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .</span><span class="sxs-lookup"><span data-stu-id="58edc-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="58edc-114">Nell'output, riceve una matrice di strutture di [**\_ immissione sovrapposte**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) che contengono le voci.</span><span class="sxs-lookup"><span data-stu-id="58edc-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="58edc-115">Il numero di elementi della matrice è fornito da *ulNumEntriesRemoved*.</span><span class="sxs-lookup"><span data-stu-id="58edc-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="58edc-116">Numero di byte trasferiti durante ogni I/O, chiave di completamento che indica in quale file si è verificata ogni I/O e l'indirizzo della struttura sovrapposta utilizzato in ogni I/o originale viene restituito nella matrice *lpCompletionPortEntries* .</span><span class="sxs-lookup"><span data-stu-id="58edc-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="58edc-117">*ulCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58edc-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58edc-118">Numero massimo di voci da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="58edc-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="58edc-119">*ulNumEntriesRemoved* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58edc-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58edc-120">Puntatore a una variabile che riceve il numero di voci effettivamente rimosse.</span><span class="sxs-lookup"><span data-stu-id="58edc-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="58edc-121">*dwMilliseconds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58edc-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58edc-122">Numero di millisecondi che il chiamante è disposto ad attendere per la visualizzazione di un pacchetto di completamento nella porta di completamento.</span><span class="sxs-lookup"><span data-stu-id="58edc-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="58edc-123">Se un pacchetto di completamento non viene visualizzato entro il tempo specificato, si verifica il timeout della funzione e viene restituito **false**.</span><span class="sxs-lookup"><span data-stu-id="58edc-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="58edc-124">Se *dwMilliseconds* è **infinito** (0xFFFFFFFF), la funzione non si timeout mai. Se *dwMilliseconds* è zero e non è presente alcuna operazione di I/O da rimuovere dalla coda, si verifica immediatamente il timeout della funzione.</span><span class="sxs-lookup"><span data-stu-id="58edc-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="58edc-125">*fAlertable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58edc-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58edc-126">Se questo parametro è **false**, la funzione non viene restituita fino a quando non è trascorso il periodo di timeout o viene recuperata una voce.</span><span class="sxs-lookup"><span data-stu-id="58edc-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="58edc-127">Se il parametro è **true** e non sono presenti voci disponibili, la funzione esegue un'attesa di avviso.</span><span class="sxs-lookup"><span data-stu-id="58edc-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="58edc-128">Il thread restituisce quando il sistema accoda una routine di completamento I/O o un APC al thread e il thread esegue la funzione.</span><span class="sxs-lookup"><span data-stu-id="58edc-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="58edc-129">Una routine di completamento viene accodata Quando la funzione [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) in cui è stata specificata è stata completata e il thread chiamante è il thread che ha avviato l'operazione.</span><span class="sxs-lookup"><span data-stu-id="58edc-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="58edc-130">Un APC viene accodato quando si chiama [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span><span class="sxs-lookup"><span data-stu-id="58edc-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58edc-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58edc-131">Return value</span></span>

<span data-ttu-id="58edc-132">Restituisce un valore diverso da zero (**true**) se ha esito positivo o zero (**false**) in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="58edc-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="58edc-133">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="58edc-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="58edc-134">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="58edc-134">Remarks</span></span>

<span data-ttu-id="58edc-135">Questa funzione associa un thread con la porta di completamento specificata.</span><span class="sxs-lookup"><span data-stu-id="58edc-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="58edc-136">Un thread può essere associato al massimo una porta di completamento.</span><span class="sxs-lookup"><span data-stu-id="58edc-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="58edc-137">Questa funzione restituisce **true** se almeno un'operazione di i/o in sospeso è stata completata, ma è possibile che una o più operazioni di i/o non siano riuscite.</span><span class="sxs-lookup"><span data-stu-id="58edc-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="58edc-138">Si noti che spetta all'utente di questa funzione controllare l'elenco delle voci restituite nel parametro *lpCompletionPortEntries* per determinare quali corrisponde a qualsiasi operazione di I/O non riuscita esaminando lo stato contenuto nel membro **lpOverlapped** in ogni [**\_ voce sovrapposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="58edc-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="58edc-139">Questa funzione restituisce **false** se nessuna operazione di I/O è stata rimessa in coda.</span><span class="sxs-lookup"><span data-stu-id="58edc-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="58edc-140">Ciò significa in genere che si è verificato un errore durante l'elaborazione dei parametri per questa chiamata o che l'handle *tentato* è stato chiuso o è altrimenti non valido.</span><span class="sxs-lookup"><span data-stu-id="58edc-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="58edc-141">La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fornisce informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="58edc-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="58edc-142">Se una chiamata a [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ha esito negativo perché l'handle associato è chiuso, la funzione restituisce **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà l' **errore \_ \_ Wait \_ 0**.</span><span class="sxs-lookup"><span data-stu-id="58edc-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="58edc-143">Le applicazioni server possono avere diversi thread che chiamano la funzione **GetQueuedCompletionStatusEx** per la stessa porta di completamento.</span><span class="sxs-lookup"><span data-stu-id="58edc-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="58edc-144">Quando le operazioni di I/O vengono completate, vengono accodate a questa porta in ordine First-in-First-out.</span><span class="sxs-lookup"><span data-stu-id="58edc-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="58edc-145">Se un thread è in attesa di questa chiamata, una o più richieste accodate completano la chiamata solo per quel thread.</span><span class="sxs-lookup"><span data-stu-id="58edc-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="58edc-146">Per ulteriori informazioni sulla teoria della porta di completamento I/O, sull'utilizzo e sulle funzioni associate, vedere [porte di completamento i/o](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="58edc-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="58edc-147">In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.</span><span class="sxs-lookup"><span data-stu-id="58edc-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="58edc-148">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="58edc-148">Technology</span></span>                                           | <span data-ttu-id="58edc-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="58edc-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="58edc-150">Protocollo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="58edc-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="58edc-151">Sì</span><span class="sxs-lookup"><span data-stu-id="58edc-151">Yes</span></span><br/> |
| <span data-ttu-id="58edc-152">Failover trasparente SMB 3,0 (failover)</span><span class="sxs-lookup"><span data-stu-id="58edc-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="58edc-153">Sì</span><span class="sxs-lookup"><span data-stu-id="58edc-153">Yes</span></span><br/> |
| <span data-ttu-id="58edc-154">SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)</span><span class="sxs-lookup"><span data-stu-id="58edc-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="58edc-155">Sì</span><span class="sxs-lookup"><span data-stu-id="58edc-155">Yes</span></span><br/> |
| <span data-ttu-id="58edc-156">File System Volume condiviso cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="58edc-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="58edc-157">Sì</span><span class="sxs-lookup"><span data-stu-id="58edc-157">Yes</span></span><br/> |
| <span data-ttu-id="58edc-158">Resilient file System (ReFS)</span><span class="sxs-lookup"><span data-stu-id="58edc-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="58edc-159">Sì</span><span class="sxs-lookup"><span data-stu-id="58edc-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="58edc-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58edc-160">Requirements</span></span>



| <span data-ttu-id="58edc-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="58edc-161">Requirement</span></span> | <span data-ttu-id="58edc-162">Valore</span><span class="sxs-lookup"><span data-stu-id="58edc-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58edc-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58edc-163">Minimum supported client</span></span><br/> | <span data-ttu-id="58edc-164">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="58edc-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="58edc-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58edc-165">Minimum supported server</span></span><br/> | <span data-ttu-id="58edc-166">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="58edc-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="58edc-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58edc-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="58edc-168"><dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluso Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58edc-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="58edc-169">Libreria</span><span class="sxs-lookup"><span data-stu-id="58edc-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="58edc-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="58edc-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="58edc-171">DLL</span><span class="sxs-lookup"><span data-stu-id="58edc-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58edc-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58edc-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="58edc-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58edc-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="58edc-174">**Argomenti introduttivi**</span><span class="sxs-lookup"><span data-stu-id="58edc-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="58edc-175">Funzioni di gestione file</span><span class="sxs-lookup"><span data-stu-id="58edc-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="58edc-176">Porte di completamento I/O</span><span class="sxs-lookup"><span data-stu-id="58edc-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="58edc-177">Uso delle intestazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="58edc-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="58edc-178">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="58edc-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="58edc-179">**ConnectNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="58edc-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="58edc-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="58edc-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="58edc-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="58edc-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="58edc-182">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="58edc-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="58edc-183">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="58edc-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="58edc-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="58edc-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="58edc-185">**PostQueuedCompletionStatus ha provocato**</span><span class="sxs-lookup"><span data-stu-id="58edc-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="58edc-186">**TransactNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="58edc-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="58edc-187">**WaitCommEvent**</span><span class="sxs-lookup"><span data-stu-id="58edc-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="58edc-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="58edc-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

