---
description: Annulla tutte le operazioni di input e output (I/O) in sospeso emesse dal thread chiamante per il file specificato.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Funzione CancelIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310809"
---
# <a name="cancelio-function"></a><span data-ttu-id="17179-103">CancelIo (funzione)</span><span class="sxs-lookup"><span data-stu-id="17179-103">CancelIo function</span></span>

<span data-ttu-id="17179-104">Annulla tutte le operazioni di input e output (I/O) in sospeso emesse dal thread chiamante per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="17179-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="17179-105">La funzione non annulla le operazioni di I/O rilasciate da altri thread per un handle di file.</span><span class="sxs-lookup"><span data-stu-id="17179-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="17179-106">Per annullare le operazioni di I/O da un altro thread, usare la funzione [**CancelIoEx**](cancelioex-func.md) .</span><span class="sxs-lookup"><span data-stu-id="17179-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="17179-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17179-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="17179-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="17179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17179-109">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17179-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17179-110">Handle per il file.</span><span class="sxs-lookup"><span data-stu-id="17179-110">A handle to the file.</span></span>

<span data-ttu-id="17179-111">La funzione Annulla tutte le operazioni di I/O in sospeso per questo handle di file.</span><span class="sxs-lookup"><span data-stu-id="17179-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17179-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17179-112">Return value</span></span>

<span data-ttu-id="17179-113">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="17179-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="17179-114">L'operazione di annullamento per tutte le operazioni di I/O in sospeso emesse dal thread chiamante per l'handle di file specificato è stata richiesta correttamente.</span><span class="sxs-lookup"><span data-stu-id="17179-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="17179-115">Il thread può utilizzare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare quando le operazioni di i/O sono state completate.</span><span class="sxs-lookup"><span data-stu-id="17179-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="17179-116">Se la funzione ha esito negativo, il valore restituito è zero (0).</span><span class="sxs-lookup"><span data-stu-id="17179-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="17179-117">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="17179-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="17179-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="17179-118">Remarks</span></span>

<span data-ttu-id="17179-119">Se sono in corso operazioni di I/O in sospeso per l'handle di file specificato e vengono rilasciate dal thread chiamante, la funzione **CancelIo** le Annulla.</span><span class="sxs-lookup"><span data-stu-id="17179-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="17179-120">**CancelIo** Annulla solo l'i/O in attesa sull'handle, non modifica lo stato dell'handle; Ciò significa che non è possibile fare affidamento sullo stato dell'handle perché non è possibile sapere se l'operazione è stata completata o annullata correttamente.</span><span class="sxs-lookup"><span data-stu-id="17179-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="17179-121">Le operazioni di I/O devono essere emesse come I/O sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="17179-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="17179-122">In caso contrario, le operazioni di I/O non restituiscono per consentire al thread di chiamare la funzione **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="17179-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="17179-123">La chiamata della funzione **CancelIo** con un handle di file non aperto con il **flag di file \_ \_ sovrapposto** non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="17179-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="17179-124">Tutte le operazioni di I/O annullate completate con l'operazione di errore Error sono state **\_ \_ interrotte** e tutte le notifiche di completamento per le operazioni di i/o vengono eseguite normalmente.</span><span class="sxs-lookup"><span data-stu-id="17179-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="17179-125">In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.</span><span class="sxs-lookup"><span data-stu-id="17179-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="17179-126">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="17179-126">Technology</span></span>                                           | <span data-ttu-id="17179-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="17179-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="17179-128">Protocollo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="17179-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="17179-129">Sì</span><span class="sxs-lookup"><span data-stu-id="17179-129">Yes</span></span><br/> |
| <span data-ttu-id="17179-130">Failover trasparente SMB 3,0 (failover)</span><span class="sxs-lookup"><span data-stu-id="17179-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="17179-131">Sì</span><span class="sxs-lookup"><span data-stu-id="17179-131">Yes</span></span><br/> |
| <span data-ttu-id="17179-132">SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)</span><span class="sxs-lookup"><span data-stu-id="17179-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="17179-133">Sì</span><span class="sxs-lookup"><span data-stu-id="17179-133">Yes</span></span><br/> |
| <span data-ttu-id="17179-134">File System Volume condiviso cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="17179-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="17179-135">Sì</span><span class="sxs-lookup"><span data-stu-id="17179-135">Yes</span></span><br/> |
| <span data-ttu-id="17179-136">Resilient file System (ReFS)</span><span class="sxs-lookup"><span data-stu-id="17179-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="17179-137">Sì</span><span class="sxs-lookup"><span data-stu-id="17179-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17179-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17179-138">Requirements</span></span>



| <span data-ttu-id="17179-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="17179-139">Requirement</span></span> | <span data-ttu-id="17179-140">Valore</span><span class="sxs-lookup"><span data-stu-id="17179-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17179-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17179-141">Minimum supported client</span></span><br/> | <span data-ttu-id="17179-142">App desktop di Windows XP \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="17179-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="17179-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17179-143">Minimum supported server</span></span><br/> | <span data-ttu-id="17179-144">App UWP per \[ app desktop di Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="17179-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="17179-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17179-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="17179-146"><dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP (incluso Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17179-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="17179-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="17179-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="17179-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="17179-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="17179-149">DLL</span><span class="sxs-lookup"><span data-stu-id="17179-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17179-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17179-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="17179-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17179-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17179-152">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="17179-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="17179-153">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="17179-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="17179-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="17179-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="17179-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="17179-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="17179-156">Funzioni di gestione file</span><span class="sxs-lookup"><span data-stu-id="17179-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="17179-157">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="17179-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="17179-158">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="17179-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="17179-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="17179-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="17179-160">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="17179-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="17179-161">I/O sincrono e asincrono</span><span class="sxs-lookup"><span data-stu-id="17179-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="17179-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="17179-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="17179-163">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="17179-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

