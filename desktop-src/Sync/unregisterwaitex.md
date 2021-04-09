---
description: Annulla un'operazione di attesa registrata rilasciata dalla funzione RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Funzione Unregisterwaitex ha provocato (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882049"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="9de5f-103">Unregisterwaitex ha provocato (funzione)</span><span class="sxs-lookup"><span data-stu-id="9de5f-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="9de5f-104">Annulla un'operazione di attesa registrata rilasciata dalla funzione [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="9de5f-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9de5f-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="9de5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9de5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de5f-107">*WaitHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de5f-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de5f-108">Handle di attesa.</span><span class="sxs-lookup"><span data-stu-id="9de5f-108">The wait handle.</span></span> <span data-ttu-id="9de5f-109">Questo handle viene restituito dalla funzione [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="9de5f-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="9de5f-110">*CompletionEvent* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9de5f-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9de5f-111">Handle per l'oggetto evento da segnalare quando è stata annullata la registrazione dell'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="9de5f-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="9de5f-112">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9de5f-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="9de5f-113">Se questo parametro è **un \_ \_ valore di handle non valido**, la funzione attende il completamento di tutte le funzioni di callback prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="9de5f-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="9de5f-114">Se questo parametro è **null**, la funzione contrassegna il timer per l'eliminazione e restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="9de5f-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="9de5f-115">Tuttavia, la maggior parte dei chiamanti deve attendere il completamento della funzione di callback in modo che possano eseguire tutte le operazioni di pulizia necessarie.</span><span class="sxs-lookup"><span data-stu-id="9de5f-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="9de5f-116">Se il chiamante fornisce questo evento e la funzione ha esito positivo o se la funzione ha esito negativo con **errore \_ io \_ in sospeso**, non chiudere l'evento fino a quando non viene segnalato.</span><span class="sxs-lookup"><span data-stu-id="9de5f-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de5f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9de5f-117">Return value</span></span>

<span data-ttu-id="9de5f-118">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9de5f-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="9de5f-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="9de5f-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="9de5f-120">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9de5f-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9de5f-121">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9de5f-121">Remarks</span></span>

<span data-ttu-id="9de5f-122">Non è possibile effettuare una chiamata di blocco a **unregisterwaitex ha provocato** dall'interno di una funzione di callback per la stessa operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="9de5f-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="9de5f-123">In caso contrario, il callback sarà in attesa del completamento.</span><span class="sxs-lookup"><span data-stu-id="9de5f-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="9de5f-124">In generale, una chiamata di blocco a **unregisterwaitex ha provocato** crea una dipendenza tra il thread corrente e il callback. Pertanto, per effettuare una chiamata di annullamento della registrazione del blocco su un'altra operazione di attesa, è necessario assicurarsi che le funzioni di callback non dipendano l'una dall'altra e che la seconda operazione di attesa non esegua anche una chiamata di annullamento della registrazione di blocco alla prima operazione.</span><span class="sxs-lookup"><span data-stu-id="9de5f-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="9de5f-125">Prestare attenzione quando si esegue una chiamata **unregisterwaitex ha provocato** di blocco su un thread permanente.</span><span class="sxs-lookup"><span data-stu-id="9de5f-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="9de5f-126">Se l'operazione di attesa di cui è stata annullata la registrazione è stata creata con **WT \_ EXECUTEINPERSISTENTTHREAD**, potrebbe verificarsi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="9de5f-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="9de5f-127">Dopo aver eseguito una chiamata non di blocco a **unregisterwaitex ha provocato**, non è possibile accodare nessuna nuova funzione di callback associata a *WaitHandle* .</span><span class="sxs-lookup"><span data-stu-id="9de5f-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="9de5f-128">Tuttavia, potrebbero essere presenti funzioni di callback in sospeso già accodate ai thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9de5f-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="9de5f-129">In alcune condizioni, la funzione avrà esito negativo con **errore \_ io \_ in sospeso** se *CompletionEvent* è **null**.</span><span class="sxs-lookup"><span data-stu-id="9de5f-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="9de5f-130">Indica che sono presenti funzioni di callback in attesa.</span><span class="sxs-lookup"><span data-stu-id="9de5f-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="9de5f-131">Tali callback verranno eseguiti o durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9de5f-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="9de5f-132">Se *CompletionEvent* è un handle per un evento fornito dal chiamante, è possibile che la funzione abbia esito positivo, esito negativo con errore i/o **\_ \_ in sospeso** o esito negativo con un codice di errore diverso.</span><span class="sxs-lookup"><span data-stu-id="9de5f-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="9de5f-133">Se la funzione ha esito positivo o se la funzione ha esito negativo con **errore \_ io \_ in sospeso**, il chiamante deve sempre attendere fino a quando l'evento non viene segnalato per chiudere l'evento.</span><span class="sxs-lookup"><span data-stu-id="9de5f-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="9de5f-134">Se la funzione ha esito negativo con un codice di errore diverso, non è necessario attendere fino a quando l'evento non viene segnalato per chiudere l'evento.</span><span class="sxs-lookup"><span data-stu-id="9de5f-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="9de5f-135">**Windows XP:** Se *CompletionEvent* è un handle per un evento fornito dal chiamante e la funzione ha esito negativo con **errore \_ io \_ in sospeso**, il chiamante deve attendere fino a quando l'evento non viene segnalato per chiudere l'evento.</span><span class="sxs-lookup"><span data-stu-id="9de5f-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="9de5f-136">Questo comportamento è stato modificato a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9de5f-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="9de5f-137">Per compilare un'applicazione che usa questa funzione, definire **\_ Win32 \_ WinNT** come 0x0500 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9de5f-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="9de5f-138">Per ulteriori informazioni, vedere [utilizzo delle intestazioni di Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="9de5f-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9de5f-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9de5f-139">Requirements</span></span>



| <span data-ttu-id="9de5f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9de5f-140">Requirement</span></span> | <span data-ttu-id="9de5f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="9de5f-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de5f-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9de5f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9de5f-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9de5f-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9de5f-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9de5f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9de5f-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9de5f-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9de5f-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9de5f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de5f-147"><dt>Threadpoollegacyapiset. h in Windows 8 e Windows Server 2012 (incluso Windows. h); </dt> <dt>Winbase. h in Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP e Windows server 2003 (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9de5f-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9de5f-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="9de5f-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="9de5f-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9de5f-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9de5f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9de5f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9de5f-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9de5f-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="9de5f-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9de5f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de5f-153">**RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="9de5f-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="9de5f-154">Funzioni di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9de5f-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="9de5f-155">Pooling dei thread</span><span class="sxs-lookup"><span data-stu-id="9de5f-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
