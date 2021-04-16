---
description: Contrassegna le operazioni di I/O sincrone in sospeso emesse dal thread specificato come annullato.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Funzione CancelSynchronousIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530006"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="5a02d-103">CancelSynchronousIo (funzione)</span><span class="sxs-lookup"><span data-stu-id="5a02d-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="5a02d-104">Contrassegna le operazioni di I/O sincrone in sospeso emesse dal thread specificato come annullato.</span><span class="sxs-lookup"><span data-stu-id="5a02d-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a02d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a02d-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="5a02d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a02d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a02d-107">*hThread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a02d-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a02d-108">Handle per il thread.</span><span class="sxs-lookup"><span data-stu-id="5a02d-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a02d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a02d-109">Return value</span></span>

<span data-ttu-id="5a02d-110">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5a02d-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="5a02d-111">Se la funzione ha esito negativo, il valore restituito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5a02d-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="5a02d-112">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="5a02d-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="5a02d-113">Se questa funzione non riesce a trovare una richiesta di annullamento, il valore restituito è 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore \_ non \_ trovato**.</span><span class="sxs-lookup"><span data-stu-id="5a02d-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a02d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a02d-114">Remarks</span></span>

<span data-ttu-id="5a02d-115">Il chiamante deve avere il diritto di [ \_ terminare](/windows/desktop/ProcThread/thread-security-and-access-rights) l'accesso al thread.</span><span class="sxs-lookup"><span data-stu-id="5a02d-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="5a02d-116">Se sono in corso operazioni di I/O in sospeso per il thread specificato, la funzione **CancelSynchronousIo** le contrassegna per l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="5a02d-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="5a02d-117">La maggior parte dei tipi di operazioni può essere annullata immediatamente; altre operazioni possono continuare verso il completamento prima di essere effettivamente annullate e il chiamante riceve una notifica.</span><span class="sxs-lookup"><span data-stu-id="5a02d-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="5a02d-118">La funzione **CancelSynchronousIo** non attende il completamento di tutte le operazioni annullate.</span><span class="sxs-lookup"><span data-stu-id="5a02d-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="5a02d-119">Per ulteriori informazioni, vedere [linee guida di completamento/annullamento di I/O](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="5a02d-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="5a02d-120">L'operazione annullata è stata completata con uno dei tre stati seguenti: è necessario controllare lo stato di completamento per determinare lo stato di completamento.</span><span class="sxs-lookup"><span data-stu-id="5a02d-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="5a02d-121">I tre Stati sono:</span><span class="sxs-lookup"><span data-stu-id="5a02d-121">The three statuses are:</span></span>

-   <span data-ttu-id="5a02d-122">**L'operazione è stata completata normalmente.**</span><span class="sxs-lookup"><span data-stu-id="5a02d-122">**The operation completed normally.**</span></span> <span data-ttu-id="5a02d-123">Questa situazione può verificarsi anche se l'operazione è stata annullata, perché la richiesta di annullamento potrebbe non essere stata inviata in tempo per annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5a02d-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="5a02d-124">**L'operazione è stata annullata.**</span><span class="sxs-lookup"><span data-stu-id="5a02d-124">**The operation was canceled.**</span></span> <span data-ttu-id="5a02d-125">La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **operazione di errore \_ \_ interrotta**.</span><span class="sxs-lookup"><span data-stu-id="5a02d-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="5a02d-126">**L'operazione non è riuscita con un altro errore.**</span><span class="sxs-lookup"><span data-stu-id="5a02d-126">**The operation failed with another error.**</span></span> <span data-ttu-id="5a02d-127">La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore pertinente.</span><span class="sxs-lookup"><span data-stu-id="5a02d-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="5a02d-128">In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a02d-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="5a02d-129">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="5a02d-129">Technology</span></span>                                           | <span data-ttu-id="5a02d-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="5a02d-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="5a02d-131">Protocollo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="5a02d-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="5a02d-132">Sì</span><span class="sxs-lookup"><span data-stu-id="5a02d-132">Yes</span></span><br/> |
| <span data-ttu-id="5a02d-133">Failover trasparente SMB 3,0 (failover)</span><span class="sxs-lookup"><span data-stu-id="5a02d-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="5a02d-134">Sì</span><span class="sxs-lookup"><span data-stu-id="5a02d-134">Yes</span></span><br/> |
| <span data-ttu-id="5a02d-135">SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)</span><span class="sxs-lookup"><span data-stu-id="5a02d-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="5a02d-136">Sì</span><span class="sxs-lookup"><span data-stu-id="5a02d-136">Yes</span></span><br/> |
| <span data-ttu-id="5a02d-137">File System Volume condiviso cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="5a02d-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="5a02d-138">Sì</span><span class="sxs-lookup"><span data-stu-id="5a02d-138">Yes</span></span><br/> |
| <span data-ttu-id="5a02d-139">Resilient file System (ReFS)</span><span class="sxs-lookup"><span data-stu-id="5a02d-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="5a02d-140">Sì</span><span class="sxs-lookup"><span data-stu-id="5a02d-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a02d-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a02d-141">Requirements</span></span>



| <span data-ttu-id="5a02d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a02d-142">Requirement</span></span> | <span data-ttu-id="5a02d-143">Valore</span><span class="sxs-lookup"><span data-stu-id="5a02d-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a02d-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a02d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5a02d-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a02d-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="5a02d-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a02d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5a02d-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a02d-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="5a02d-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a02d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a02d-149"><dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluso Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a02d-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5a02d-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a02d-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a02d-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a02d-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="5a02d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5a02d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a02d-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a02d-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="5a02d-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a02d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a02d-155">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="5a02d-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="5a02d-156">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="5a02d-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="5a02d-157">Funzioni di gestione file</span><span class="sxs-lookup"><span data-stu-id="5a02d-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="5a02d-158">I/O sincrono e asincrono</span><span class="sxs-lookup"><span data-stu-id="5a02d-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

