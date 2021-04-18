---
description: Contrassegna tutte le operazioni di I/O in attesa per l'handle di file specificato. La funzione Annulla solo le operazioni di I/O nel processo corrente, indipendentemente dal thread che ha creato l'operazione di I/O.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Funzione CancelIoEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311146"
---
# <a name="cancelioex-function"></a><span data-ttu-id="86cb9-104">CancelIoEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="86cb9-104">CancelIoEx function</span></span>

<span data-ttu-id="86cb9-105">Contrassegna tutte le operazioni di I/O in attesa per l'handle di file specificato.</span><span class="sxs-lookup"><span data-stu-id="86cb9-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="86cb9-106">La funzione Annulla solo le operazioni di I/O nel processo corrente, indipendentemente dal thread che ha creato l'operazione di I/O.</span><span class="sxs-lookup"><span data-stu-id="86cb9-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cb9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86cb9-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="86cb9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="86cb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86cb9-109">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86cb9-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cb9-110">Handle per il file.</span><span class="sxs-lookup"><span data-stu-id="86cb9-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="86cb9-111">*lpOverlapped* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="86cb9-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86cb9-112">Puntatore a una struttura di dati [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) che contiene i dati utilizzati per l'I/O asincrono.</span><span class="sxs-lookup"><span data-stu-id="86cb9-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="86cb9-113">Se questo parametro è **null**, tutte le richieste di i/O per il parametro *hFile* vengono annullate.</span><span class="sxs-lookup"><span data-stu-id="86cb9-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="86cb9-114">Se questo parametro non è **null**, solo le richieste di I/O specifiche rilasciate per il file con la struttura sovrapposta *lpOverlapped* specificata vengono contrassegnate come annullate, vale a dire che è possibile annullare una o più richieste, mentre la funzione [**CancelIo**](cancelio.md) Annulla tutte le richieste in sospeso in un handle di file.</span><span class="sxs-lookup"><span data-stu-id="86cb9-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86cb9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86cb9-115">Return value</span></span>

<span data-ttu-id="86cb9-116">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="86cb9-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="86cb9-117">L'operazione di annullamento per tutte le operazioni di I/O in sospeso emesse dal processo chiamante per l'handle di file specificato è stata richiesta correttamente.</span><span class="sxs-lookup"><span data-stu-id="86cb9-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="86cb9-118">L'applicazione non deve liberare o riutilizzare la struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata alle operazioni di i/O annullate fino a quando non sono state completate.</span><span class="sxs-lookup"><span data-stu-id="86cb9-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="86cb9-119">Il thread può utilizzare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare quando le operazioni di i/O sono state completate.</span><span class="sxs-lookup"><span data-stu-id="86cb9-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="86cb9-120">Se la funzione ha esito negativo, il valore restituito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="86cb9-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="86cb9-121">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="86cb9-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="86cb9-122">Se questa funzione non riesce a trovare una richiesta di annullamento, il valore restituito è 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore \_ non \_ trovato**.</span><span class="sxs-lookup"><span data-stu-id="86cb9-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86cb9-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="86cb9-123">Remarks</span></span>

<span data-ttu-id="86cb9-124">La funzione **CancelIoEx** consente di annullare le richieste in thread diversi dal thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="86cb9-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="86cb9-125">La funzione [**CancelIo**](cancelio.md) Annulla solo le richieste nello stesso thread che ha chiamato la funzione **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="86cb9-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="86cb9-126">**CancelIoEx** Annulla solo l'i/O in attesa sull'handle, non modifica lo stato dell'handle; Ciò significa che non è possibile fare affidamento sullo stato dell'handle perché non è possibile sapere se l'operazione è stata completata o annullata correttamente.</span><span class="sxs-lookup"><span data-stu-id="86cb9-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="86cb9-127">Se sono in corso operazioni di I/O in sospeso per l'handle di file specificato, la funzione **CancelIoEx** le contrassegna per l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="86cb9-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="86cb9-128">La maggior parte dei tipi di operazioni può essere annullata immediatamente; altre operazioni possono continuare verso il completamento prima di essere effettivamente annullate e il chiamante riceve una notifica.</span><span class="sxs-lookup"><span data-stu-id="86cb9-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="86cb9-129">La funzione **CancelIoEx** non attende il completamento di tutte le operazioni annullate.</span><span class="sxs-lookup"><span data-stu-id="86cb9-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="86cb9-130">Se l'handle di file è associato a una porta di completamento, un pacchetto di completamento I/O non viene accodato alla porta se un'operazione sincrona viene annullata correttamente.</span><span class="sxs-lookup"><span data-stu-id="86cb9-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="86cb9-131">Per le operazioni asincrone ancora in sospeso, l'operazione di annullamento Accoda un pacchetto di completamento di I/O.</span><span class="sxs-lookup"><span data-stu-id="86cb9-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="86cb9-132">L'operazione annullata è stata completata con uno dei tre stati seguenti: è necessario controllare lo stato di completamento per determinare lo stato di completamento.</span><span class="sxs-lookup"><span data-stu-id="86cb9-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="86cb9-133">I tre Stati sono:</span><span class="sxs-lookup"><span data-stu-id="86cb9-133">The three statuses are:</span></span>

-   <span data-ttu-id="86cb9-134">L'operazione è stata completata normalmente.</span><span class="sxs-lookup"><span data-stu-id="86cb9-134">The operation completed normally.</span></span> <span data-ttu-id="86cb9-135">Questa situazione può verificarsi anche se l'operazione è stata annullata, perché la richiesta di annullamento potrebbe non essere stata inviata in tempo per annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="86cb9-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="86cb9-136">L'operazione è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="86cb9-136">The operation was canceled.</span></span> <span data-ttu-id="86cb9-137">La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **operazione di errore \_ \_ interrotta**.</span><span class="sxs-lookup"><span data-stu-id="86cb9-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="86cb9-138">L'operazione non è riuscita con un altro errore.</span><span class="sxs-lookup"><span data-stu-id="86cb9-138">The operation failed with another error.</span></span> <span data-ttu-id="86cb9-139">La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore pertinente.</span><span class="sxs-lookup"><span data-stu-id="86cb9-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="86cb9-140">In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.</span><span class="sxs-lookup"><span data-stu-id="86cb9-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="86cb9-141">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="86cb9-141">Technology</span></span>                                           | <span data-ttu-id="86cb9-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="86cb9-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="86cb9-143">Protocollo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="86cb9-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="86cb9-144">Sì</span><span class="sxs-lookup"><span data-stu-id="86cb9-144">Yes</span></span><br/> |
| <span data-ttu-id="86cb9-145">Failover trasparente SMB 3,0 (failover)</span><span class="sxs-lookup"><span data-stu-id="86cb9-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="86cb9-146">Sì</span><span class="sxs-lookup"><span data-stu-id="86cb9-146">Yes</span></span><br/> |
| <span data-ttu-id="86cb9-147">SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)</span><span class="sxs-lookup"><span data-stu-id="86cb9-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="86cb9-148">Sì</span><span class="sxs-lookup"><span data-stu-id="86cb9-148">Yes</span></span><br/> |
| <span data-ttu-id="86cb9-149">File System Volume condiviso cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="86cb9-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="86cb9-150">Sì</span><span class="sxs-lookup"><span data-stu-id="86cb9-150">Yes</span></span><br/> |
| <span data-ttu-id="86cb9-151">Resilient file System (ReFS)</span><span class="sxs-lookup"><span data-stu-id="86cb9-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="86cb9-152">Sì</span><span class="sxs-lookup"><span data-stu-id="86cb9-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="86cb9-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86cb9-153">Requirements</span></span>



| <span data-ttu-id="86cb9-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="86cb9-154">Requirement</span></span> | <span data-ttu-id="86cb9-155">Valore</span><span class="sxs-lookup"><span data-stu-id="86cb9-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86cb9-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86cb9-156">Minimum supported client</span></span><br/> | <span data-ttu-id="86cb9-157">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86cb9-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="86cb9-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86cb9-158">Minimum supported server</span></span><br/> | <span data-ttu-id="86cb9-159">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="86cb9-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="86cb9-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86cb9-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="86cb9-161"><dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluso Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86cb9-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="86cb9-162">Libreria</span><span class="sxs-lookup"><span data-stu-id="86cb9-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="86cb9-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="86cb9-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="86cb9-164">DLL</span><span class="sxs-lookup"><span data-stu-id="86cb9-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86cb9-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86cb9-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="86cb9-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86cb9-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cb9-167">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="86cb9-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="86cb9-168">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="86cb9-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="86cb9-169">Annullamento di operazioni di I/O in sospeso</span><span class="sxs-lookup"><span data-stu-id="86cb9-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="86cb9-170">Funzioni di gestione file</span><span class="sxs-lookup"><span data-stu-id="86cb9-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="86cb9-171">I/O sincrono e asincrono</span><span class="sxs-lookup"><span data-stu-id="86cb9-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

