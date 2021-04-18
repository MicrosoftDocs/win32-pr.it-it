---
description: Recupera i livelli di retroilluminazione AC e DC correnti e lo stato di alimentazione corrente.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: Codice di controllo IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312045"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="fe082-103">\_ \_ \_ \_ Codice controllo luminosità visualizzazione query video IOCTL</span><span class="sxs-lookup"><span data-stu-id="fe082-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="fe082-104">\[Questo codice di controllo è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fe082-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe082-105">Il supporto per questo codice di controllo è stato rimosso in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe082-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="fe082-106">In alternativa, usare la classe [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) .\]</span><span class="sxs-lookup"><span data-stu-id="fe082-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="fe082-107">Recupera i livelli di retroilluminazione AC e DC correnti e lo stato di alimentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe082-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="fe082-108">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe082-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="fe082-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe082-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe082-110">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="fe082-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-111">Handle per l'oggetto \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="fe082-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="fe082-112">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="fe082-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-113">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="fe082-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-114">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe082-114">The control code for the operation.</span></span> <span data-ttu-id="fe082-115">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="fe082-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="fe082-116">Usare **la \_ \_ luminosità di \_ visualizzazione \_ della query video IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="fe082-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-117">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="fe082-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-118">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="fe082-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-119">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="fe082-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-120">Non utilizzato con questa operazione. impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="fe082-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-121">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="fe082-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-122">Puntatore a un buffer che riceverà una struttura [**di \_ luminosità della visualizzazione**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe082-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-123">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="fe082-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-124">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fe082-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="fe082-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di output restituiti.</span><span class="sxs-lookup"><span data-stu-id="fe082-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="fe082-127">Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il buffer insufficiente per l'errore del codice di errore \_ \_ e il numero di byte restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="fe082-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="fe082-128">Se il buffer di output è troppo piccolo per conservare tutti i dati, ma può inserire alcune voci, il sistema operativo viene restituito per quanto riguarda, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore del codice \_ di errore più \_ dati e *lpBytesReturned* indica la quantità di dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="fe082-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="fe082-129">L'applicazione deve chiamare nuovamente [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la stessa operazione, specificando un nuovo punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="fe082-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="fe082-130">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="fe082-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="fe082-131">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="fe082-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="fe082-132">Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="fe082-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="fe082-133">Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="fe082-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="fe082-134">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="fe082-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="fe082-135">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="fe082-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="fe082-136">Se *hDevice* è stato aperto con il flag \_ OVERLAPPED del flag file \_ , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="fe082-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="fe082-137">In questo caso, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="fe082-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="fe082-138">Se il dispositivo è stato aperto con il flag FILE \_ \_ sovrapposto e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="fe082-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="fe082-139">Se *hDevice* è stato aperto senza specificare il \_ flag Overlapped del flag file \_ , *lpOverlapped* viene ignorato e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="fe082-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe082-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe082-140">Return value</span></span>

<span data-ttu-id="fe082-141">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fe082-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="fe082-142">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fe082-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="fe082-143">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="fe082-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe082-144">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="fe082-144">Remarks</span></span>

<span data-ttu-id="fe082-145">Il file di intestazione utilizzato per compilare applicazioni che includono questa funzionalità, Ntddvdeo. h, è incluso in Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="fe082-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="fe082-146">Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="fe082-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="fe082-147">In alternativa, è possibile definire questo codice di controllo come segue:</span><span class="sxs-lookup"><span data-stu-id="fe082-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="fe082-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe082-148">Requirements</span></span>



| <span data-ttu-id="fe082-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe082-149">Requirement</span></span> | <span data-ttu-id="fe082-150">Valore</span><span class="sxs-lookup"><span data-stu-id="fe082-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe082-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe082-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fe082-152">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe082-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe082-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe082-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fe082-154">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe082-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe082-155">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fe082-155">End of client support</span></span><br/>    | <span data-ttu-id="fe082-156">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="fe082-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="fe082-157">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fe082-157">End of server support</span></span><br/>    | <span data-ttu-id="fe082-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe082-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="fe082-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe082-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe082-160"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe082-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe082-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe082-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe082-162">Interfaccia di controllo retroilluminazione</span><span class="sxs-lookup"><span data-stu-id="fe082-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="fe082-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="fe082-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="fe082-164">[**\_luminosità visualizzazione**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe082-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fe082-165">**\_ \_ luminosità schermo del set di video IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fe082-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

