---
description: Recupera lo stato corrente della batteria.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: Codice di controllo IOCTL_BATTERY_QUERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312048"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="53c80-103">\_Codice di \_ \_ controllo stato query IOCTL Battery</span><span class="sxs-lookup"><span data-stu-id="53c80-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="53c80-104">Recupera lo stato corrente della batteria.</span><span class="sxs-lookup"><span data-stu-id="53c80-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="53c80-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="53c80-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="53c80-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53c80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c80-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="53c80-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-108">Handle per la batteria da cui devono essere restituite le informazioni.</span><span class="sxs-lookup"><span data-stu-id="53c80-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="53c80-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="53c80-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="53c80-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="53c80-111">The control code for the operation.</span></span> <span data-ttu-id="53c80-112">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="53c80-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="53c80-113">Usare **\_ \_ \_ lo stato di query della batteria IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="53c80-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="53c80-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-115">Puntatore a una struttura [**di \_ \_ stato di attesa della batteria**](battery-wait-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="53c80-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="53c80-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-117">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="53c80-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="53c80-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-119">Puntatore a una struttura [**di \_ stato della batteria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="53c80-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="53c80-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-121">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="53c80-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="53c80-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-123">Puntatore a una variabile che riceve la dimensione dei dati restituiti nel buffer *lpOutBuffer* , in byte.</span><span class="sxs-lookup"><span data-stu-id="53c80-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="53c80-124">Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il **\_ \_ buffer insufficiente** nell'errore del codice di errore e il numero di byte restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="53c80-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="53c80-125">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="53c80-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="53c80-126">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="53c80-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="53c80-127">Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="53c80-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="53c80-128">Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="53c80-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="53c80-129">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="53c80-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="53c80-130">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="53c80-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="53c80-131">Se *hDevice* è stato aperto con il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="53c80-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="53c80-132">In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="53c80-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="53c80-133">Se il dispositivo è stato aperto con il flag **file \_ \_ sovrapposto** e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="53c80-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="53c80-134">Se *hDevice* è stato aperto senza specificare il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="53c80-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c80-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53c80-135">Return value</span></span>

<span data-ttu-id="53c80-136">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="53c80-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="53c80-137">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="53c80-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="53c80-138">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="53c80-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="53c80-139">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="53c80-139">Remarks</span></span>

<span data-ttu-id="53c80-140">Questa batteria IOCTL recupera lo stato della batteria al momento della restituzione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="53c80-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="53c80-141">La struttura del parametro di input, [**\_ \_ stato di attesa della**](battery-wait-status-str.md)batteria, indica quando lo stato della batteria deve essere elaborato e restituito.</span><span class="sxs-lookup"><span data-stu-id="53c80-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="53c80-142">Le richieste di stato della batteria possono essere per la restituzione immediata oppure possono essere impostate per attendere una determinata condizione prima del completamento.</span><span class="sxs-lookup"><span data-stu-id="53c80-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="53c80-143">Ad esempio, è possibile effettuare una richiesta di informazioni sulla batteria per attendere che la capacità della batteria raggiunga un punto specificato o che lo stato della batteria venga modificato.</span><span class="sxs-lookup"><span data-stu-id="53c80-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="53c80-144">Tutte le richieste di informazioni sulla batteria vengono completate con lo stato del **file di errore \_ \_ non \_ trovato** ogni volta che l'elemento **BatteryTag** della richiesta non corrisponde a quello del tag della batteria corrente.</span><span class="sxs-lookup"><span data-stu-id="53c80-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="53c80-145">Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) . Viene usato per garantire che le informazioni della batteria restituita corrispondano a quelle della batteria richiesta.</span><span class="sxs-lookup"><span data-stu-id="53c80-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="53c80-146">Per le implicazioni dell'I/O sovrapposto in questa operazione, vedere la sezione Osservazioni dell'argomento [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="53c80-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="53c80-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="53c80-147">Examples</span></span>

<span data-ttu-id="53c80-148">Per un esempio, vedere [enumerazione dei dispositivi a batteria](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="53c80-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53c80-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53c80-149">Requirements</span></span>



| <span data-ttu-id="53c80-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c80-150">Requirement</span></span> | <span data-ttu-id="53c80-151">Valore</span><span class="sxs-lookup"><span data-stu-id="53c80-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c80-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c80-152">Minimum supported client</span></span><br/> | <span data-ttu-id="53c80-153">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="53c80-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="53c80-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c80-154">Minimum supported server</span></span><br/> | <span data-ttu-id="53c80-155">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53c80-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="53c80-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53c80-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c80-157"><dt>Poclass. h; </dt> <dt>BatClass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="53c80-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c80-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53c80-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c80-159">Informazioni sulla batteria</span><span class="sxs-lookup"><span data-stu-id="53c80-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="53c80-160">Codici di controllo del risparmio energia</span><span class="sxs-lookup"><span data-stu-id="53c80-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="53c80-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="53c80-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="53c80-162">**stato della batteria \_**</span><span class="sxs-lookup"><span data-stu-id="53c80-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="53c80-163">**\_stato di attesa della batteria \_**</span><span class="sxs-lookup"><span data-stu-id="53c80-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="53c80-164">**\_ \_ informazioni sulle query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53c80-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="53c80-165">**\_tag di \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53c80-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="53c80-166">**\_ \_ informazioni sui set di batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53c80-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

