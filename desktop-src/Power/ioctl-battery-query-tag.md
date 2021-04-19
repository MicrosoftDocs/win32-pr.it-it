---
description: Recupera il tag corrente delle batterie.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: Codice di controllo IOCTL_BATTERY_QUERY_TAG (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312047"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="3566c-103">\_Codice di \_ \_ controllo tag di query della batteria IOCTL</span><span class="sxs-lookup"><span data-stu-id="3566c-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="3566c-104">Recupera il tag corrente della batteria.</span><span class="sxs-lookup"><span data-stu-id="3566c-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="3566c-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="3566c-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="3566c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3566c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3566c-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="3566c-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-108">Handle per la batteria da cui deve essere recuperato il tag.</span><span class="sxs-lookup"><span data-stu-id="3566c-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="3566c-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="3566c-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="3566c-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="3566c-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3566c-111">The control code for the operation.</span></span> <span data-ttu-id="3566c-112">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="3566c-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="3566c-113">Usare **il \_ \_ \_ tag di query della batteria IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3566c-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3566c-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="3566c-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-115">Puntatore a un buffer di input **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="3566c-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="3566c-116">Il valore indica il numero di millisecondi di attesa in assenza di batteria.</span><span class="sxs-lookup"><span data-stu-id="3566c-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="3566c-117">Il valore-1 indica che la richiesta attenderà per un tempo illimitato (o fino a quando non viene annullata da un altro evento).</span><span class="sxs-lookup"><span data-stu-id="3566c-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="3566c-118">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3566c-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-119">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="3566c-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3566c-120">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="3566c-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-121">Puntatore a un buffer di output **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="3566c-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="3566c-122">In caso di esito positivo, questo buffer contiene il tag corrente della batteria, che può essere qualsiasi valore eccetto \_ tag batteria \_ non valido.</span><span class="sxs-lookup"><span data-stu-id="3566c-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="3566c-123">In caso di esito negativo, se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il file di errore del codice di errore **\_ \_ non \_ trovato**, questo buffer contiene il valore **tag della batteria non \_ \_ valido**.</span><span class="sxs-lookup"><span data-stu-id="3566c-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="3566c-124">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3566c-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-125">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="3566c-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3566c-126">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="3566c-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-127">Puntatore a una variabile che riceve la dimensione dei dati archiviati nel buffer *lpOutBuffer* , in byte.</span><span class="sxs-lookup"><span data-stu-id="3566c-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="3566c-128">Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il **\_ \_ buffer insufficiente** nell'errore del codice di errore e il numero di byte restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3566c-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="3566c-129">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3566c-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="3566c-130">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3566c-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="3566c-131">Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="3566c-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="3566c-132">Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3566c-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="3566c-133">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="3566c-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="3566c-134">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="3566c-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="3566c-135">Se *hDevice* è stato aperto con il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="3566c-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="3566c-136">In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="3566c-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="3566c-137">Se il dispositivo è stato aperto con il flag **file \_ \_ sovrapposto** e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="3566c-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="3566c-138">Se *hDevice* è stato aperto senza specificare il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3566c-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3566c-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3566c-139">Return value</span></span>

<span data-ttu-id="3566c-140">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3566c-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="3566c-141">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3566c-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="3566c-142">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3566c-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3566c-143">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3566c-143">Remarks</span></span>

<span data-ttu-id="3566c-144">Questa batteria IOCTL recupera il tag corrente della batteria.</span><span class="sxs-lookup"><span data-stu-id="3566c-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="3566c-145">Il tag della batteria è un valore univoco diverso da zero che cambia quando la batteria fisica viene reinserita, sostituita o sottoposta a qualsiasi modifica delle caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="3566c-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="3566c-146">Vedere la sezione relativa ai tag della batteria nell'argomento Panoramica [delle informazioni](battery-information.md) sulla batteria per maggiori dettagli su quando viene modificato un tag della batteria, su come rilevare la modifica e su come un'applicazione deve continuare dopo la modifica di un tag della batteria.</span><span class="sxs-lookup"><span data-stu-id="3566c-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="3566c-147">Quando non è presente una batteria, la richiesta attende l'ora indicata e, se non è ancora presente una batteria, restituirà il file di **errore \_ \_ non \_ trovato** e imposterà il tag della batteria su **tag della batteria non \_ \_ valido**.</span><span class="sxs-lookup"><span data-stu-id="3566c-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="3566c-148">(Per altre informazioni, vedere informazioni sulla batteria).</span><span class="sxs-lookup"><span data-stu-id="3566c-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="3566c-149">Per tutte le richieste di altre informazioni sulla batteria è necessario che il chiamante fornisca il tag della batteria corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3566c-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="3566c-150">In questo modo il chiamante riceve informazioni per la stessa batteria per ogni richiesta e garantisce che il chiamante sia a conoscenza delle modifiche della batteria senza il polling costante.</span><span class="sxs-lookup"><span data-stu-id="3566c-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="3566c-151">Per le implicazioni dell'I/O sovrapposto in questa operazione, vedere la sezione Osservazioni dell'argomento [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="3566c-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="3566c-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="3566c-152">Examples</span></span>

<span data-ttu-id="3566c-153">Per un esempio, vedere [enumerazione dei dispositivi a batteria](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="3566c-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3566c-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3566c-154">Requirements</span></span>



| <span data-ttu-id="3566c-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3566c-155">Requirement</span></span> | <span data-ttu-id="3566c-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3566c-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3566c-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3566c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3566c-158">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3566c-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="3566c-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3566c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3566c-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3566c-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="3566c-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3566c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="3566c-162"><dt>Poclass. h; </dt> <dt>BatClass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="3566c-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3566c-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3566c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3566c-164">Informazioni sulla batteria</span><span class="sxs-lookup"><span data-stu-id="3566c-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="3566c-165">Codici di controllo del risparmio energia</span><span class="sxs-lookup"><span data-stu-id="3566c-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="3566c-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="3566c-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="3566c-167">**\_ \_ informazioni sulle query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3566c-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="3566c-168">**\_stato della \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3566c-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="3566c-169">**\_ \_ informazioni sui set di batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3566c-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

