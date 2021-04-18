---
description: Il \_ LMR IOCTL \_ Disabilita \_ il \_ codice di controllo del buffer locale Disabilita la memorizzazione nella cache locale dei dati in memoria durante la lettura o la scrittura di dati in un file remoto. Si tratta di un codice di controllo definito internamente non disponibile in un'intestazione pubblica.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Codice di controllo IOCTL_LMR_DISABLE_LOCAL_BUFFERING
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304408"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="01495-104">IOCTL \_ LMR \_ disabilitare \_ il \_ codice di controllo del buffer locale</span><span class="sxs-lookup"><span data-stu-id="01495-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="01495-105">Il LMR IOCTL Disabilita il codice di controllo del **\_ \_ \_ \_ buffer locale Disabilita** la memorizzazione nella cache locale dei dati in memoria durante la lettura o la scrittura di dati in un file remoto.</span><span class="sxs-lookup"><span data-stu-id="01495-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="01495-106">Si tratta di un codice di controllo definito internamente non disponibile in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="01495-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="01495-107">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="01495-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="01495-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01495-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01495-109">*hDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01495-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-110">Handle per il file remoto.</span><span class="sxs-lookup"><span data-stu-id="01495-110">A handle to the remote file.</span></span> <span data-ttu-id="01495-111">Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="01495-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="01495-112">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01495-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-113">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="01495-113">The control code for the operation.</span></span> <span data-ttu-id="01495-114">Usare il valore 0x140390 per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="01495-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="01495-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="01495-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="01495-116">Non utilizzato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="01495-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01495-117">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01495-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-118">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="01495-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="01495-119">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="01495-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="01495-120">*lpOutBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01495-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-121">Non utilizzato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="01495-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01495-122">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01495-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-123">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="01495-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="01495-124">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="01495-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="01495-125">*lpBytesReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01495-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-126">Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="01495-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="01495-127">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente** e *lpBytesReturned* è zero.</span><span class="sxs-lookup"><span data-stu-id="01495-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="01495-128">Se il parametro *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="01495-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="01495-129">Anche quando un'operazione non restituisce dati di output e il parametro *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="01495-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="01495-130">Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.</span><span class="sxs-lookup"><span data-stu-id="01495-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="01495-131">Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="01495-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="01495-132">Se *lpOverlapped* non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="01495-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="01495-133">Per recuperare il numero di byte restituiti, chiamare la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="01495-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="01495-134">Se il parametro *hDevice* è associato a una porta di completamento di i/O, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="01495-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="01495-135">*lpOverlapped* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01495-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01495-136">Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="01495-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="01495-137">Se il parametro *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="01495-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="01495-138">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="01495-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="01495-139">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="01495-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="01495-140">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="01495-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="01495-141">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="01495-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="01495-142">In caso contrario, la funzione non viene restituita fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="01495-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01495-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01495-143">Return value</span></span>

<span data-ttu-id="01495-144">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="01495-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="01495-145">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="01495-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="01495-146">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="01495-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="01495-147">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="01495-147">Remarks</span></span>

<span data-ttu-id="01495-148">Il LMR IOCTL Disabilita il codice di controllo del **\_ \_ \_ \_ buffer locale** viene definito internamente dal sistema come 0x140390 e non in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="01495-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="01495-149">Viene usato da applicazioni per scopi specifici per disabilitare la memorizzazione nella cache locale dei dati in memoria sul lato client durante la lettura o la scrittura di dati in un file remoto.</span><span class="sxs-lookup"><span data-stu-id="01495-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="01495-150">Quando il buffering locale è disabilitato, l'impostazione rimane attiva fino a quando tutti gli handle aperti del file non vengono chiusi e il redirector pulisce le relative strutture di dati interne.</span><span class="sxs-lookup"><span data-stu-id="01495-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="01495-151">Le applicazioni generiche non devono utilizzare **IOCTL \_ LMR \_ disabilitare \_ il \_ buffering locale**, perché può comportare un eccessivo traffico di rete e una perdita di prestazioni associata.</span><span class="sxs-lookup"><span data-stu-id="01495-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="01495-152">Il LMR IOCTL disabilitare il codice di controllo del **\_ \_ \_ \_ buffer locale** deve essere usato solo in applicazioni specializzate che trasferiscono grandi quantità di dati in rete, tentando di ottimizzare l'uso della larghezza di banda di rete.</span><span class="sxs-lookup"><span data-stu-id="01495-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="01495-153">Le funzioni [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) , ad esempio, utilizzano **IOCTL \_ LMR disabilitare il \_ \_ \_ buffering locale** per migliorare le prestazioni di copia dei file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="01495-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="01495-154">**IOCTL \_ LMR \_ Disabilita \_ la \_ memorizzazione nel buffer locale** non è implementata dai file system locali e avrà esito negativo e verrà restituita una funzione di errore **\_ non valida \_**.</span><span class="sxs-lookup"><span data-stu-id="01495-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="01495-155">Il rilascio del LMR IOCTL Disabilita il codice di controllo del **\_ \_ \_ \_ buffer locale** negli handle di directory remota avrà esito negativo e l'errore di errore **non è \_ \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="01495-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="01495-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01495-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01495-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="01495-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
