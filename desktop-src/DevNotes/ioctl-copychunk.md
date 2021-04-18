---
description: Il \_ codice di controllo IOCTL copychunk esegue avvia una copia sul lato server di un intervallo di dati, detto anche blocco.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Codice di controllo IOCTL_COPYCHUNK
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304409"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="d1539-103">\_Codice di controllo IOCTL copychunk esegue</span><span class="sxs-lookup"><span data-stu-id="d1539-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="d1539-104">Il codice di controllo **IOCTL \_ copychunk esegue** avvia una copia sul lato server di un intervallo di dati, detto anche blocco.</span><span class="sxs-lookup"><span data-stu-id="d1539-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="d1539-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1539-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="d1539-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1539-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1539-107">*hDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1539-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-108">Handle per il file che è la destinazione dell'operazione di copia sul lato server.</span><span class="sxs-lookup"><span data-stu-id="d1539-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="d1539-109">Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="d1539-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-110">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1539-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d1539-111">The control code for the operation.</span></span> <span data-ttu-id="d1539-112">Utilizzare **IOCTL \_ copychunk esegue** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="d1539-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="d1539-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d1539-114">Puntatore al buffer di input, una struttura **di \_ \_ copia SRV copychunk esegue** .</span><span class="sxs-lookup"><span data-stu-id="d1539-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="d1539-115">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d1539-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-116">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1539-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-117">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="d1539-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-118">*lpOutBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1539-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-119">Puntatore al buffer di output, una struttura **di \_ \_ risposta SRV copychunk esegue** .</span><span class="sxs-lookup"><span data-stu-id="d1539-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="d1539-120">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d1539-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-121">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1539-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-122">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="d1539-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-123">*lpBytesReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1539-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-124">Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="d1539-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="d1539-125">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente** e *lpBytesReturned* è zero.</span><span class="sxs-lookup"><span data-stu-id="d1539-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="d1539-126">Se il parametro *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d1539-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="d1539-127">Anche quando un'operazione non restituisce dati di output e il parametro *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="d1539-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="d1539-128">Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.</span><span class="sxs-lookup"><span data-stu-id="d1539-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="d1539-129">Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d1539-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="d1539-130">Se *lpOverlapped* non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="d1539-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="d1539-131">Per recuperare il numero di byte restituiti, chiamare la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="d1539-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="d1539-132">Se il parametro *hDevice* è associato a una porta di completamento di i/O, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="d1539-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="d1539-133">*lpOverlapped* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1539-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1539-134">Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="d1539-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="d1539-135">Se il parametro *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d1539-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="d1539-136">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="d1539-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="d1539-137">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="d1539-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="d1539-138">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="d1539-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="d1539-139">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d1539-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="d1539-140">In caso contrario, la funzione non viene restituita fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="d1539-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1539-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1539-141">Return value</span></span>

<span data-ttu-id="d1539-142">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d1539-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="d1539-143">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="d1539-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="d1539-144">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d1539-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1539-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d1539-145">Remarks</span></span>

<span data-ttu-id="d1539-146">A questo codice di controllo non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d1539-146">This control code has no associated header file.</span></span> <span data-ttu-id="d1539-147">È necessario definire il codice di controllo e le strutture di dati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d1539-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="d1539-148">Questi membri possono essere descritti come segue.</span><span class="sxs-lookup"><span data-stu-id="d1539-148">These members can be described as follows.</span></span>



| <span data-ttu-id="d1539-149">Membro</span><span class="sxs-lookup"><span data-stu-id="d1539-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="d1539-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1539-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1539-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span><span class="sxs-lookup"><span data-stu-id="d1539-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="d1539-152">Offset, in byte, dall'inizio del file di origine al blocco da copiare.</span><span class="sxs-lookup"><span data-stu-id="d1539-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d1539-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span><span class="sxs-lookup"><span data-stu-id="d1539-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="d1539-154">Offset, in byte, dall'inizio del file di destinazione fino alla posizione in cui deve essere copiato il blocco.</span><span class="sxs-lookup"><span data-stu-id="d1539-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="d1539-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Lunghezza**</span><span class="sxs-lookup"><span data-stu-id="d1539-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="d1539-156">Numero di byte di dati nel blocco da copiare.</span><span class="sxs-lookup"><span data-stu-id="d1539-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="d1539-157">Deve essere maggiore di zero e minore o uguale a 1 MB.</span><span class="sxs-lookup"><span data-stu-id="d1539-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="d1539-158">**Lunghezza** \* **ChunkCount** deve essere minore o uguale a 16 MB.</span><span class="sxs-lookup"><span data-stu-id="d1539-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="d1539-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="d1539-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="d1539-160">Chiave che rappresenta il file di origine con i dati da copiare.</span><span class="sxs-lookup"><span data-stu-id="d1539-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="d1539-161">Questa chiave viene ottenuta tramite la [**\_ chiave di \_ \_ ripresa \_ della richiesta SRV FSCTL**](fsctl-srv-request-resume-key.md).</span><span class="sxs-lookup"><span data-stu-id="d1539-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="d1539-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span><span class="sxs-lookup"><span data-stu-id="d1539-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="d1539-163">Numero di blocchi da copiare.</span><span class="sxs-lookup"><span data-stu-id="d1539-163">The number of chunks to be copied.</span></span> <span data-ttu-id="d1539-164">Deve essere maggiore di zero e minore o uguale a 256.</span><span class="sxs-lookup"><span data-stu-id="d1539-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d1539-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservati**</span><span class="sxs-lookup"><span data-stu-id="d1539-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="d1539-166">Questo membro è riservato per l'utilizzo del sistema; Non usare.</span><span class="sxs-lookup"><span data-stu-id="d1539-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d1539-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Pezzo**</span><span class="sxs-lookup"><span data-stu-id="d1539-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="d1539-168">Matrice di strutture **ChunkCount** **SRV \_ copychunk esegue** , una per ogni blocco da copiare.</span><span class="sxs-lookup"><span data-stu-id="d1539-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="d1539-169">La lunghezza, in byte, di questa matrice deve essere **ChunkCount** \* sizeof (**SRV \_ copychunk esegue**).</span><span class="sxs-lookup"><span data-stu-id="d1539-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="d1539-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span><span class="sxs-lookup"><span data-stu-id="d1539-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="d1539-171">Se l'operazione non è riuscita con un **parametro di errore \_ non valido \_**, questo valore indica il numero massimo di blocchi accettati dal server in una singola richiesta, ovvero 256.</span><span class="sxs-lookup"><span data-stu-id="d1539-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="d1539-172">In caso contrario, questo valore indica il numero di blocchi scritti correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1539-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="d1539-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="d1539-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="d1539-174">Se l'operazione non è riuscita con un **parametro di errore \_ non valido \_**, questo valore indica il numero massimo di byte che il server consentirà di scrivere in un singolo blocco, ovvero 1 MB.</span><span class="sxs-lookup"><span data-stu-id="d1539-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="d1539-175">In caso contrario, questo valore indica il numero di byte scritti correttamente nell'ultimo blocco non elaborato correttamente (se si è verificata una scrittura parziale).</span><span class="sxs-lookup"><span data-stu-id="d1539-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="d1539-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="d1539-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="d1539-177">Se l'operazione non è riuscita con un **parametro di errore \_ non valido \_**, questo valore indica il numero massimo di byte copiati dal server in una singola richiesta, ovvero 16 MB.</span><span class="sxs-lookup"><span data-stu-id="d1539-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="d1539-178">In caso contrario, questo valore indica il numero di byte scritti correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1539-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="d1539-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1539-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1539-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="d1539-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="d1539-181">**FSCTL \_ la \_ \_ chiave di ripresa della richiesta SRV \_**</span><span class="sxs-lookup"><span data-stu-id="d1539-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
