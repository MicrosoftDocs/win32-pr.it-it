---
description: Attende che tutti i volumi del disco specificato siano pronti per l'uso.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: Codice di controllo IOCTL_DISK_ARE_VOLUMES_READY (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317779"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="7c6c0-103">Il \_ disco IOCTL \_ è un codice di \_ \_ controllo pronto per i volumi</span><span class="sxs-lookup"><span data-stu-id="7c6c0-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="7c6c0-104">Attende che tutti i volumi del disco specificato siano pronti per l'uso.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="7c6c0-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="7c6c0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c6c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6c0-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-108">Handle per il disco.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-108">A handle to the disk.</span></span>

<span data-ttu-id="7c6c0-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="7c6c0-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-111">The control code for the operation.</span></span>

<span data-ttu-id="7c6c0-112">USA **il \_ disco IOCTL \_ sono i \_ volumi \_ pronti** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-114">Non utilizzato con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-114">Not used with this operation.</span></span> <span data-ttu-id="7c6c0-115">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-117">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="7c6c0-118">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-120">Non utilizzato con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-120">Not used with this operation.</span></span> <span data-ttu-id="7c6c0-121">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-122">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-123">Non utilizzato con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-123">Not used with this operation.</span></span> <span data-ttu-id="7c6c0-124">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-126">Non utilizzato con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-126">Not used with this operation.</span></span> <span data-ttu-id="7c6c0-127">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c6c0-128">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="7c6c0-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6c0-129">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="7c6c0-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="7c6c0-130">Se *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="7c6c0-131">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="7c6c0-132">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="7c6c0-133">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="7c6c0-134">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="7c6c0-135">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6c0-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c6c0-136">Return value</span></span>

<span data-ttu-id="7c6c0-137">Se l'operazione viene completata correttamente, a indicare che tutti i volumi sul disco sono pronti per l'uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="7c6c0-138">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="7c6c0-139">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6c0-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c6c0-140">Requirements</span></span>



| <span data-ttu-id="7c6c0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c6c0-141">Requirement</span></span> | <span data-ttu-id="7c6c0-142">Valore</span><span class="sxs-lookup"><span data-stu-id="7c6c0-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6c0-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c6c0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6c0-144">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c6c0-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7c6c0-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c6c0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6c0-146">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c6c0-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c6c0-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c6c0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6c0-148"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6c0-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c6c0-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c6c0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6c0-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="7c6c0-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="7c6c0-151">Codici di controllo di gestione disco</span><span class="sxs-lookup"><span data-stu-id="7c6c0-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

