---
description: Determina se un volume è un volume CSV.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: Codice di controllo IOCTL_VOLUME_IS_CSV (Ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348541"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="6f10c-103">Il \_ volume IOCTL \_ è \_ codice di controllo CSV</span><span class="sxs-lookup"><span data-stu-id="6f10c-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="6f10c-104">Determina se un volume è un volume CSV.</span><span class="sxs-lookup"><span data-stu-id="6f10c-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="6f10c-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="6f10c-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="6f10c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f10c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f10c-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6f10c-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-108">Handle per il volume.</span><span class="sxs-lookup"><span data-stu-id="6f10c-108">A handle to the volume.</span></span> <span data-ttu-id="6f10c-109">Per recuperare un handle del volume, chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="6f10c-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="6f10c-110">Solo gli amministratori possono aprire gli handle del volume.</span><span class="sxs-lookup"><span data-stu-id="6f10c-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="6f10c-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-112">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6f10c-112">The control code for the operation.</span></span> <span data-ttu-id="6f10c-113">Per questa operazione, usare il **\_ volume IOCTL \_ è \_ CSV** .</span><span class="sxs-lookup"><span data-stu-id="6f10c-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="6f10c-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-115">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="6f10c-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="6f10c-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-117">Non utilizzato con questa operazione. impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="6f10c-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="6f10c-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-119">Puntatore a **true** se il volume è un volume CSV; in caso contrario, la chiamata di funzione non riesce.</span><span class="sxs-lookup"><span data-stu-id="6f10c-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="6f10c-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-121">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="6f10c-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="6f10c-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-123">Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="6f10c-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="6f10c-124">Se *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6f10c-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="6f10c-125">Anche quando un'operazione non restituisce dati di output e *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="6f10c-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="6f10c-126">Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.</span><span class="sxs-lookup"><span data-stu-id="6f10c-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="6f10c-127">Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6f10c-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="6f10c-128">Se questo parametro non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="6f10c-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="6f10c-129">Per recuperare il numero di byte restituiti, chiamare [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="6f10c-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="6f10c-130">Se *hDevice* è associato a una porta di completamento di I/O, è possibile recuperare il numero di byte restituiti chiamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="6f10c-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="6f10c-131">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="6f10c-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="6f10c-132">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="6f10c-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="6f10c-133">Se *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6f10c-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="6f10c-134">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="6f10c-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="6f10c-135">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="6f10c-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="6f10c-136">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="6f10c-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="6f10c-137">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6f10c-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="6f10c-138">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="6f10c-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f10c-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f10c-139">Return value</span></span>

<span data-ttu-id="6f10c-140">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6f10c-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="6f10c-141">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="6f10c-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="6f10c-142">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="6f10c-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f10c-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f10c-143">Requirements</span></span>



| <span data-ttu-id="6f10c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f10c-144">Requirement</span></span> | <span data-ttu-id="6f10c-145">Valore</span><span class="sxs-lookup"><span data-stu-id="6f10c-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f10c-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f10c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6f10c-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6f10c-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="6f10c-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f10c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6f10c-149">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6f10c-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6f10c-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f10c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f10c-151"><dt>Ntddvol. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f10c-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f10c-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f10c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f10c-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="6f10c-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="6f10c-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="6f10c-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="6f10c-155">Codici di controllo della gestione del volume</span><span class="sxs-lookup"><span data-stu-id="6f10c-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

