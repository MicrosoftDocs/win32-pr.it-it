---
description: Imposta i livelli di retroilluminazione AC e DC correnti.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: Codice di controllo IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967494"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="84a5a-103">\_Codice di \_ controllo \_ della \_ luminosità del set di video IOCTL</span><span class="sxs-lookup"><span data-stu-id="84a5a-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="84a5a-104">Imposta i livelli di retroilluminazione AC e DC correnti.</span><span class="sxs-lookup"><span data-stu-id="84a5a-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="84a5a-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="84a5a-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="84a5a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84a5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a5a-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="84a5a-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-108">Handle per l'oggetto \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="84a5a-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="84a5a-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="84a5a-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="84a5a-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="84a5a-111">The control code for the operation.</span></span> <span data-ttu-id="84a5a-112">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="84a5a-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="84a5a-113">Usare **la \_ \_ luminosità di \_ visualizzazione \_ del set di video IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="84a5a-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="84a5a-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-115">Puntatore a una struttura [**di \_ luminosità della visualizzazione**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="84a5a-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="84a5a-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-117">Dimensioni del buffer a cui punta *lpOutBuffer* in byte.</span><span class="sxs-lookup"><span data-stu-id="84a5a-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="84a5a-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-119">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="84a5a-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="84a5a-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-121">Non utilizzato con questa operazione. impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="84a5a-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="84a5a-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-123">Puntatore a una variabile che riceve il numero effettivo di byte restituiti dalla funzione nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="84a5a-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="84a5a-124">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* viene utilizzato internamente e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="84a5a-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="84a5a-125">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="84a5a-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="84a5a-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="84a5a-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="84a5a-127">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="84a5a-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="84a5a-128">Se *hDevice* è stato aperto con il flag \_ OVERLAPPED del flag file \_ , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="84a5a-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="84a5a-129">In questo caso, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="84a5a-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="84a5a-130">Se il dispositivo è stato aperto con il flag FILE \_ \_ sovrapposto e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="84a5a-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="84a5a-131">Se *hDevice* è stato aperto senza specificare il \_ flag Overlapped del flag file \_ , *lpOverlapped* viene ignorato e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="84a5a-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a5a-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84a5a-132">Return value</span></span>

<span data-ttu-id="84a5a-133">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="84a5a-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="84a5a-134">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="84a5a-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="84a5a-135">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="84a5a-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="84a5a-136">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="84a5a-136">Remarks</span></span>

<span data-ttu-id="84a5a-137">I valori specificati nei membri **ucACBrightness** e **ucDCBrightness** della struttura di [**\_ luminosità dello schermo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) devono essere stati restituiti in precedenza [**dalla \_ \_ \_ \_ luminosità supportata dalla query IOCTL video**](ioctl-video-query-supported-brightness.md).</span><span class="sxs-lookup"><span data-stu-id="84a5a-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="84a5a-138">Se, ad esempio, i valori supportati sono 10, 20, 30, 40, 50, 60, 70, 80, 90 e 100, l'utilizzo di un valore di 33 è un errore.</span><span class="sxs-lookup"><span data-stu-id="84a5a-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="84a5a-139">Il file di intestazione utilizzato per compilare applicazioni che includono questa funzionalità, Ntddvdeo. h, è incluso in Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="84a5a-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="84a5a-140">Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="84a5a-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="84a5a-141">In alternativa, è possibile definire questo codice di controllo come segue:</span><span class="sxs-lookup"><span data-stu-id="84a5a-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="84a5a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84a5a-142">Requirements</span></span>



| <span data-ttu-id="84a5a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a5a-143">Requirement</span></span> | <span data-ttu-id="84a5a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="84a5a-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84a5a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a5a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="84a5a-146">Windows Vista, \[ solo app desktop Windows XP con SP1\]</span><span class="sxs-lookup"><span data-stu-id="84a5a-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="84a5a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a5a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="84a5a-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84a5a-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84a5a-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84a5a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a5a-150"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a5a-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a5a-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84a5a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a5a-152">Interfaccia di controllo retroilluminazione</span><span class="sxs-lookup"><span data-stu-id="84a5a-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="84a5a-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="84a5a-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="84a5a-154">[**\_luminosità visualizzazione**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84a5a-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84a5a-155">**\_ \_ \_ luminosità visualizzazione query video \_ IOCTL**</span><span class="sxs-lookup"><span data-stu-id="84a5a-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="84a5a-156">**\_ \_ luminosità supportata dalla query video \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="84a5a-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

