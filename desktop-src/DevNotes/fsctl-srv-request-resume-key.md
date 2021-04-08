---
description: Il \_ \_ \_ codice di controllo della chiave Resume della richiesta FSCTL SRV \_ viene usato per recuperare un riferimento a un file opaco da usare con il \_ codice di controllo IOCTL copychunk esegue.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Codice di controllo FSCTL_SRV_REQUEST_RESUME_KEY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877305"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="41574-103">FSCTL \_ il \_ codice di controllo della chiave di ripresa della richiesta SRV \_ \_</span><span class="sxs-lookup"><span data-stu-id="41574-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="41574-104">Il codice di controllo della **\_ \_ \_ \_ chiave Resume della richiesta FSCTL SRV** viene usato per recuperare un riferimento a un file opaco da usare con il codice di controllo [**IOCTL \_ copychunk esegue**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="41574-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="41574-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="41574-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="41574-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41574-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41574-107">*hDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41574-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-108">Handle per il file per il quale deve essere richiesta la chiave del file di origine.</span><span class="sxs-lookup"><span data-stu-id="41574-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="41574-109">Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="41574-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="41574-110">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41574-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="41574-111">The control code for the operation.</span></span> <span data-ttu-id="41574-112">Usare **la \_ \_ chiave di \_ ripresa \_ della richiesta SRV FSCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="41574-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="41574-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="41574-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="41574-114">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="41574-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="41574-115">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41574-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-116">Non utilizzato con questa operazione. impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="41574-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="41574-117">*lpOutBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41574-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-118">Un puntatore al buffer di output, una struttura di **\_ chiavi di \_ ripresa \_ della richiesta SRV** .</span><span class="sxs-lookup"><span data-stu-id="41574-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="41574-119">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="41574-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="41574-120">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41574-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-121">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="41574-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41574-122">*lpBytesReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41574-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-123">Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="41574-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="41574-124">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente** e *lpBytesReturned* è zero.</span><span class="sxs-lookup"><span data-stu-id="41574-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="41574-125">Se il parametro *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="41574-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="41574-126">Anche quando un'operazione non restituisce dati di output e il parametro *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="41574-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="41574-127">Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.</span><span class="sxs-lookup"><span data-stu-id="41574-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="41574-128">Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="41574-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="41574-129">Se *lpOverlapped* non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="41574-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="41574-130">Per recuperare il numero di byte restituiti, chiamare la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="41574-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="41574-131">Se il parametro *hDevice* è associato a una porta di completamento di i/O, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="41574-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="41574-132">*lpOverlapped* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41574-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41574-133">Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="41574-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="41574-134">Se il parametro *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="41574-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="41574-135">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="41574-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="41574-136">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="41574-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="41574-137">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="41574-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="41574-138">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="41574-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="41574-139">In caso contrario, la funzione non viene restituita fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="41574-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41574-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41574-140">Return value</span></span>

<span data-ttu-id="41574-141">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="41574-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="41574-142">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="41574-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="41574-143">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="41574-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="41574-144">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="41574-144">Remarks</span></span>

<span data-ttu-id="41574-145">A questo codice di controllo non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="41574-145">This control code has no associated header file.</span></span> <span data-ttu-id="41574-146">È necessario definire il codice di controllo e le strutture di dati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="41574-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="41574-147">Questi membri possono essere descritti come segue.</span><span class="sxs-lookup"><span data-stu-id="41574-147">These members can be described as follows.</span></span>



| <span data-ttu-id="41574-148">Membro</span><span class="sxs-lookup"><span data-stu-id="41574-148">Member</span></span>                                                                                                                       | <span data-ttu-id="41574-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41574-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41574-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span><span class="sxs-lookup"><span data-stu-id="41574-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="41574-151">Valore opaco che identifica il file di origine nel server.</span><span class="sxs-lookup"><span data-stu-id="41574-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="41574-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="41574-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="41574-153">Valore opaco che identifica l'ora in cui è stato aperto il file.</span><span class="sxs-lookup"><span data-stu-id="41574-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="41574-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**PID**</span><span class="sxs-lookup"><span data-stu-id="41574-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="41574-155">Valore opaco che identifica il processo che ha aperto il file.</span><span class="sxs-lookup"><span data-stu-id="41574-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="41574-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Chiave**</span><span class="sxs-lookup"><span data-stu-id="41574-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="41574-157">Struttura **di \_ \_ chiavi di ripresa SRV** .</span><span class="sxs-lookup"><span data-stu-id="41574-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="41574-158">Per eseguire un'operazione di copia sul lato server, usare questa struttura con il codice di controllo [**IOCTL \_ copychunk esegue**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="41574-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="41574-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span><span class="sxs-lookup"><span data-stu-id="41574-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="41574-160">Questo membro è riservato per l'utilizzo del sistema; Non usare.</span><span class="sxs-lookup"><span data-stu-id="41574-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="41574-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contesto**</span><span class="sxs-lookup"><span data-stu-id="41574-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="41574-162">Questo membro è riservato per l'utilizzo del sistema; Non usare.</span><span class="sxs-lookup"><span data-stu-id="41574-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="41574-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41574-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41574-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="41574-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="41574-165">**\_COPYCHUNK esegue IOCTL**</span><span class="sxs-lookup"><span data-stu-id="41574-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
