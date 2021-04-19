---
description: Recupera gli attributi del dispositivo disco specificato.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: Codice di controllo IOCTL_DISK_GET_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 613c73c2fd82e76768b0fc692b63b0761938a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317778"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a><span data-ttu-id="a1e5c-103">\_Codice di controllo del disco IOCTL \_ get \_ cluster \_ info</span><span class="sxs-lookup"><span data-stu-id="a1e5c-103">IOCTL\_DISK\_GET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="a1e5c-104">Recupera gli attributi del dispositivo disco specificato.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-104">Retrieves the attributes of the specified disk device.</span></span>

<span data-ttu-id="a1e5c-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="a1e5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e5c-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-108">Handle per il disco.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-108">A handle to the disk.</span></span>

<span data-ttu-id="a1e5c-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="a1e5c-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-111">The control code for the operation.</span></span>

<span data-ttu-id="a1e5c-112">USA **il \_ disco \_ IOCTL \_ ottenere \_ informazioni sul cluster** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-112">Use **IOCTL\_DISK\_GET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-114">Non utilizzato con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-114">Not used with this operation.</span></span> <span data-ttu-id="a1e5c-115">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-117">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="a1e5c-118">Impostare su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a1e5c-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-120">Puntatore a un buffer che riceve una struttura di dati di [**\_ \_ informazioni sul cluster del disco**](disk-cluster-info.md) .</span><span class="sxs-lookup"><span data-stu-id="a1e5c-120">A pointer to a buffer that receives a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-122">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-124">Non utilizzato con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-124">Not used with this operation.</span></span> <span data-ttu-id="a1e5c-125">Impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a1e5c-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="a1e5c-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e5c-127">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a1e5c-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a1e5c-128">Se *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="a1e5c-129">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="a1e5c-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a1e5c-130">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="a1e5c-131">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a1e5c-132">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="a1e5c-133">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e5c-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1e5c-134">Return value</span></span>

<span data-ttu-id="a1e5c-135">Se l'operazione viene completata correttamente, a indicare che tutti i volumi sul disco sono pronti per l'uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a1e5c-136">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a1e5c-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a1e5c-137">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a1e5c-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e5c-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1e5c-138">Requirements</span></span>



| <span data-ttu-id="a1e5c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e5c-139">Requirement</span></span> | <span data-ttu-id="a1e5c-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a1e5c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e5c-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e5c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e5c-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a1e5c-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="a1e5c-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e5c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e5c-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a1e5c-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1e5c-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1e5c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e5c-146"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1e5c-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1e5c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1e5c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e5c-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a1e5c-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="a1e5c-149">Codici di controllo di gestione disco</span><span class="sxs-lookup"><span data-stu-id="a1e5c-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="a1e5c-150">**\_informazioni sul cluster di dischi \_**</span><span class="sxs-lookup"><span data-stu-id="a1e5c-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="a1e5c-151">**\_informazioni sul \_ cluster del set di dischi IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a1e5c-151">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

