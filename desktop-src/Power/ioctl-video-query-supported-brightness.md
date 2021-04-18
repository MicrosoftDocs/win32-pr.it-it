---
description: Recupera i livelli di retroilluminazione supportati.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: Codice di controllo IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312044"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="69604-103">\_Codice di \_ controllo della \_ luminosità supportato dalla query video IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="69604-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="69604-104">Recupera i livelli di retroilluminazione supportati.</span><span class="sxs-lookup"><span data-stu-id="69604-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="69604-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="69604-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="69604-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69604-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69604-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="69604-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-108">Handle per l'oggetto \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="69604-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="69604-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="69604-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="69604-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="69604-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="69604-111">The control code for the operation.</span></span> <span data-ttu-id="69604-112">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="69604-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="69604-113">Usare **la \_ \_ \_ \_ luminosità supportata da query video IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="69604-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="69604-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="69604-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-115">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="69604-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="69604-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="69604-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-117">Non utilizzato con questa operazione. impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="69604-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="69604-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="69604-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-119">Puntatore a un buffer che riceve una matrice dei livelli di alimentazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="69604-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="69604-120">Il buffer deve avere una lunghezza di 256 byte.</span><span class="sxs-lookup"><span data-stu-id="69604-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="69604-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="69604-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-122">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="69604-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="69604-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="69604-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-124">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di output restituiti.</span><span class="sxs-lookup"><span data-stu-id="69604-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="69604-125">Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il buffer insufficiente per l'errore del codice di errore \_ \_ e il numero di byte restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="69604-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="69604-126">Se il buffer di output è troppo piccolo per conservare tutti i dati, ma può inserire alcune voci, il sistema operativo viene restituito per quanto riguarda, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore del codice \_ di errore più \_ dati e *lpBytesReturned* indica la quantità di dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="69604-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="69604-127">L'applicazione deve chiamare nuovamente [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la stessa operazione, specificando un nuovo punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="69604-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="69604-128">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="69604-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="69604-129">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="69604-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="69604-130">Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="69604-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="69604-131">Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="69604-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="69604-132">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="69604-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="69604-133">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="69604-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="69604-134">Se *hDevice* è stato aperto con il flag \_ OVERLAPPED del flag file \_ , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="69604-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="69604-135">In questo caso, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="69604-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="69604-136">Se il dispositivo è stato aperto con il flag FILE \_ \_ sovrapposto e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="69604-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="69604-137">Se *hDevice* è stato aperto senza specificare il \_ flag Overlapped del flag file \_ , *lpOverlapped* viene ignorato e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="69604-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69604-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69604-138">Return value</span></span>

<span data-ttu-id="69604-139">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="69604-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="69604-140">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="69604-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="69604-141">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="69604-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="69604-142">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="69604-142">Remarks</span></span>

<span data-ttu-id="69604-143">Ogni elemento nella matrice *lpOutBuffer* è di lunghezza pari a un byte.</span><span class="sxs-lookup"><span data-stu-id="69604-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="69604-144">Pertanto, al momento della restituzione, il parametro *lpBytesReturned* indica il numero di livelli supportati.</span><span class="sxs-lookup"><span data-stu-id="69604-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="69604-145">Ogni livello è un valore compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="69604-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="69604-146">Maggiore è il valore, più luminoso è la retroilluminazione.</span><span class="sxs-lookup"><span data-stu-id="69604-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="69604-147">Tutti i livelli sono supportati se la fonte di alimentazione è AC o DC.</span><span class="sxs-lookup"><span data-stu-id="69604-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="69604-148">Il file di intestazione utilizzato per compilare applicazioni che includono questa funzionalità, Ntddvdeo. h, è incluso in Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="69604-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="69604-149">Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="69604-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="69604-150">In alternativa, è possibile definire questo codice di controllo come segue:</span><span class="sxs-lookup"><span data-stu-id="69604-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="69604-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69604-151">Requirements</span></span>



| <span data-ttu-id="69604-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="69604-152">Requirement</span></span> | <span data-ttu-id="69604-153">Valore</span><span class="sxs-lookup"><span data-stu-id="69604-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69604-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69604-154">Minimum supported client</span></span><br/> | <span data-ttu-id="69604-155">Windows Vista, \[ solo app desktop Windows XP con SP1\]</span><span class="sxs-lookup"><span data-stu-id="69604-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="69604-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69604-156">Minimum supported server</span></span><br/> | <span data-ttu-id="69604-157">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69604-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69604-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69604-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="69604-159"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="69604-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69604-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69604-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69604-161">Interfaccia di controllo retroilluminazione</span><span class="sxs-lookup"><span data-stu-id="69604-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="69604-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="69604-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

