---
title: Codice di controllo FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: Il codice di controllo FSCTL_DFS_GET_PKT_ENTRY_STATE può ottenere le stesse informazioni della funzione NetDfsGetClientInfo, ma può fornire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524033"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="2168e-103">Codice di controllo FSCTL_DFS_GET_PKT_ENTRY_STATE</span><span class="sxs-lookup"><span data-stu-id="2168e-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="2168e-104">Il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** può ottenere le stesse informazioni della funzione [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , ma può fornire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS.</span><span class="sxs-lookup"><span data-stu-id="2168e-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="2168e-105">Non è consigliabile usare il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a meno che non si verifichino problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2168e-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="2168e-106">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2168e-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="2168e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2168e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2168e-108">*hDevice* [in]</span><span class="sxs-lookup"><span data-stu-id="2168e-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-109">Handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2168e-109">A handle to the device.</span></span> <span data-ttu-id="2168e-110">Per ottenere un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="2168e-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="2168e-111">*dwIoControlCode* [in]</span><span class="sxs-lookup"><span data-stu-id="2168e-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-112">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2168e-112">The control code for the operation.</span></span> <span data-ttu-id="2168e-113">Usare **FSCTL_DFS_GET_PKT_ENTRY_STATE** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2168e-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2168e-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="2168e-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="2168e-115">Indirizzo di una struttura [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) e delle stringhe Unicode 1-3 che seguono.</span><span class="sxs-lookup"><span data-stu-id="2168e-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="2168e-116">*nInBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="2168e-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-117">Dimensione, in byte, del buffer a cui punta il parametro *lpInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="2168e-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2168e-118">*lpOutBuffer* [out]</span><span class="sxs-lookup"><span data-stu-id="2168e-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-119">Indirizzo di una struttura di **DFS_INFO_ \#** e di eventuali stringhe e strutture a cui punta la struttura di **DFS_INFO_ \#** .</span><span class="sxs-lookup"><span data-stu-id="2168e-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="2168e-120">La struttura specifica restituita dipende dal membro del **livello** nella struttura [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) passata nel buffer di input.</span><span class="sxs-lookup"><span data-stu-id="2168e-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2168e-121">*nOutBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="2168e-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-122">Dimensione, in byte, del buffer a cui punta il parametro *lpOutBuffer* .</span><span class="sxs-lookup"><span data-stu-id="2168e-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="2168e-123">A causa delle stringhe e delle strutture a cui fa riferimento la struttura di **DFS_INFO_ \#** restituita anch ' essa nel buffer di output, il buffer deve essere maggiore della struttura **DFS_INFO_ \#** specificata.</span><span class="sxs-lookup"><span data-stu-id="2168e-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="2168e-124">*lpBytesReturned* [out]</span><span class="sxs-lookup"><span data-stu-id="2168e-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-125">Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="2168e-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="2168e-126">Se il buffer di output è troppo piccolo, ma almeno sufficientemente grande da contenere un **valore DWORD**, la chiamata ha esito negativo, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR_MORE_DATA** e il primo **valore DWORD** del buffer di output contiene le dimensioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="2168e-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="2168e-127">Se il buffer di output non può mantenere un **valore DWORD** , la chiamata ha esito negativo con **ERROR_INSUFFICIENT_BUFFER** e *lpBytesReturned* è zero.</span><span class="sxs-lookup"><span data-stu-id="2168e-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="2168e-128">Se *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2168e-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="2168e-129">Anche quando un'operazione non restituisce dati di output e *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="2168e-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="2168e-130">Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.</span><span class="sxs-lookup"><span data-stu-id="2168e-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="2168e-131">Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2168e-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="2168e-132">Se questo parametro non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="2168e-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="2168e-133">Per recuperare il numero di byte restituiti, chiamare [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="2168e-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="2168e-134">Se il parametro *hDevice* è associato a una porta di completamento di I/O, è possibile recuperare il numero di byte restituiti chiamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="2168e-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="2168e-135">*lpOverlapped* [in]</span><span class="sxs-lookup"><span data-stu-id="2168e-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="2168e-136">Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="2168e-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="2168e-137">Se *hDevice* è stato aperto senza specificare **FILE_FLAG_OVERLAPPED**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2168e-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="2168e-138">Se *hDevice* è stato aperto con il FLAG di **FILE_FLAG_OVERLAPPED** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="2168e-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="2168e-139">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="2168e-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="2168e-140">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="2168e-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="2168e-141">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2168e-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="2168e-142">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2168e-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2168e-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2168e-143">Return value</span></span>

<span data-ttu-id="2168e-144">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="2168e-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="2168e-145">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="2168e-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="2168e-146">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2168e-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="2168e-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2168e-147">Requirements</span></span>

| <span data-ttu-id="2168e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="2168e-148">Requirement</span></span> | <span data-ttu-id="2168e-149">Valore</span><span class="sxs-lookup"><span data-stu-id="2168e-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2168e-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2168e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="2168e-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2168e-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="2168e-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2168e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="2168e-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2168e-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="2168e-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2168e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="2168e-155"><dt>LmDfs. h (include LmDfs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2168e-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="2168e-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2168e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2168e-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="2168e-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="2168e-158">**NetDfsGetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="2168e-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
