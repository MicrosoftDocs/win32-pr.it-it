---
description: Imposta varie informazioni sulla batteria.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: Codice di controllo IOCTL_BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881725"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="419fc-103">\_Codice di \_ \_ controllo delle informazioni del set di batterie IOCTL</span><span class="sxs-lookup"><span data-stu-id="419fc-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="419fc-104">Imposta varie informazioni sulla batteria.</span><span class="sxs-lookup"><span data-stu-id="419fc-104">Sets various battery information.</span></span> <span data-ttu-id="419fc-105">La struttura del parametro di input, [**\_ \_ informazioni sui set di batteria**](battery-set-information-str.md), indica le informazioni sullo stato della batteria da impostare.</span><span class="sxs-lookup"><span data-stu-id="419fc-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="419fc-106">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="419fc-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="419fc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="419fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419fc-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="419fc-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-109">Handle per la batteria in cui devono essere impostate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="419fc-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="419fc-110">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="419fc-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="419fc-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-112">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="419fc-112">The control code for the operation.</span></span> <span data-ttu-id="419fc-113">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="419fc-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="419fc-114">Usare **\_ \_ \_ le informazioni sul set di batterie IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="419fc-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="419fc-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-116">Puntatore a una struttura [**di \_ \_ informazioni sul set di batterie**](battery-set-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="419fc-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-117">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="419fc-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-118">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="419fc-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="419fc-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-120">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="419fc-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="419fc-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-122">Non utilizzato con questa operazione. impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="419fc-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="419fc-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-124">Puntatore a una variabile che riceve le dimensioni dei dati restituiti nel buffer *lpOutBuffer* , in byte.</span><span class="sxs-lookup"><span data-stu-id="419fc-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="419fc-125">Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il buffer insufficiente per l'errore del codice di errore \_ \_ e il numero di byte restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="419fc-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="419fc-126">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**, anche se *lpOutBuffer* è **null**.</span><span class="sxs-lookup"><span data-stu-id="419fc-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="419fc-127">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="419fc-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="419fc-128">Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="419fc-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="419fc-129">Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="419fc-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="419fc-130">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="419fc-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="419fc-131">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="419fc-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="419fc-132">Se *hDevice* è stato aperto con il flag \_ OVERLAPPED del flag file \_ , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="419fc-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="419fc-133">In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="419fc-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="419fc-134">Se il dispositivo è stato aperto con il flag FILE \_ \_ sovrapposto e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="419fc-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="419fc-135">Se *hDevice* è stato aperto senza specificare il \_ flag Overlapped del flag file \_ , *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="419fc-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419fc-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="419fc-136">Return value</span></span>

<span data-ttu-id="419fc-137">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="419fc-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="419fc-138">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="419fc-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="419fc-139">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="419fc-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="419fc-140">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="419fc-140">Remarks</span></span>

<span data-ttu-id="419fc-141">Tutte le richieste per impostare le informazioni sulla batteria vengono completate con lo stato del file di errore \_ \_ non \_ trovato se il tag della batteria della richiesta non corrisponde a quello del tag della batteria corrente.</span><span class="sxs-lookup"><span data-stu-id="419fc-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="419fc-142">Per le implicazioni dell'I/O sovrapposto in questa operazione, vedere la sezione Osservazioni dell'argomento [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="419fc-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="419fc-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="419fc-143">Requirements</span></span>



| <span data-ttu-id="419fc-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="419fc-144">Requirement</span></span> | <span data-ttu-id="419fc-145">Valore</span><span class="sxs-lookup"><span data-stu-id="419fc-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="419fc-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="419fc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="419fc-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="419fc-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="419fc-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="419fc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="419fc-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="419fc-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="419fc-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="419fc-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="419fc-151"><dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="419fc-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="419fc-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="419fc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419fc-153">Informazioni sulla batteria</span><span class="sxs-lookup"><span data-stu-id="419fc-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="419fc-154">Codici di controllo del risparmio energia</span><span class="sxs-lookup"><span data-stu-id="419fc-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="419fc-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="419fc-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="419fc-156">**\_informazioni sui set di batteria \_**</span><span class="sxs-lookup"><span data-stu-id="419fc-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="419fc-157">**\_ \_ informazioni sulle query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="419fc-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="419fc-158">**\_stato della \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="419fc-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="419fc-159">**\_tag di \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="419fc-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

