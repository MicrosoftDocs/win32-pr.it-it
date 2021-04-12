---
description: Il \_ \_ \_ codice di controllo degli attributi da ottenere NFS esegue una query su informazioni aggiuntive su una condivisione NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Codice di controllo DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523370"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="de6fb-103">DA \_ ottenere \_ il \_ codice di controllo degli attributi NFS</span><span class="sxs-lookup"><span data-stu-id="de6fb-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="de6fb-104">Il codice di controllo degli **\_ \_ \_ attributi da ottenere NFS** esegue una query su informazioni aggiuntive su una condivisione NFS.</span><span class="sxs-lookup"><span data-stu-id="de6fb-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="de6fb-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="de6fb-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="de6fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de6fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de6fb-107">*hDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-108">Handle per un file nella condivisione NFS.</span><span class="sxs-lookup"><span data-stu-id="de6fb-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="de6fb-109">Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="de6fb-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-110">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-111">The control code for the operation.</span></span> <span data-ttu-id="de6fb-112">Usare **\_ \_ \_ gli attributi da Get NFS** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="de6fb-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="de6fb-114">Non utilizzato con questa operazione. impostare su **null**.</span><span class="sxs-lookup"><span data-stu-id="de6fb-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-115">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-116">Non utilizzato con questa operazione. impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="de6fb-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-117">*lpOutBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-118">Puntatore al buffer di output, che contiene una struttura **di \_ \_ attributi di file NFS** .</span><span class="sxs-lookup"><span data-stu-id="de6fb-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="de6fb-119">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="de6fb-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-120">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-121">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="de6fb-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-122">*lpBytesReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-123">Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="de6fb-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="de6fb-124">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore di \_ \_ buffer insufficiente** e *lpBytesReturned* è zero.</span><span class="sxs-lookup"><span data-stu-id="de6fb-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="de6fb-125">Se *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="de6fb-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="de6fb-126">Anche quando un'operazione non restituisce dati di output e *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="de6fb-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="de6fb-127">Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.</span><span class="sxs-lookup"><span data-stu-id="de6fb-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="de6fb-128">Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="de6fb-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="de6fb-129">Se questo parametro non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="de6fb-130">Per recuperare il numero di byte restituiti, chiamare [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="de6fb-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="de6fb-131">Se il parametro *hDevice* è associato a una porta di completamento di I/O, è possibile recuperare il numero di byte restituiti chiamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="de6fb-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-132">*lpOverlapped* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de6fb-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-133">Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="de6fb-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="de6fb-134">Se *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="de6fb-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="de6fb-135">Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="de6fb-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="de6fb-136">In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="de6fb-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="de6fb-137">In caso contrario, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="de6fb-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="de6fb-138">Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="de6fb-139">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="de6fb-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de6fb-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de6fb-140">Return value</span></span>

<span data-ttu-id="de6fb-141">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="de6fb-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="de6fb-142">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="de6fb-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="de6fb-143">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="de6fb-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="de6fb-144">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="de6fb-144">Remarks</span></span>

<span data-ttu-id="de6fb-145">A questo codice di controllo non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-145">This control code has no associated header file.</span></span> <span data-ttu-id="de6fb-146">È necessario definire il codice di controllo e le strutture di dati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="de6fb-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="de6fb-147">I membri della struttura possono essere descritti come segue.</span><span class="sxs-lookup"><span data-stu-id="de6fb-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="de6fb-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="de6fb-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-149">Valore opaco utilizzato per i tipi di file speciali, ad esempio file di blocco, speciali e FIFO.</span><span class="sxs-lookup"><span data-stu-id="de6fb-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="de6fb-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-151">Valore opaco utilizzato per i tipi di file speciali, ad esempio file di blocco, speciali e FIFO.</span><span class="sxs-lookup"><span data-stu-id="de6fb-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Secondi**</span><span class="sxs-lookup"><span data-stu-id="de6fb-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-153">Valore a 64 bit che rappresenta i secondi a partire dal 1 ° gennaio 1970 (UTC).</span><span class="sxs-lookup"><span data-stu-id="de6fb-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span><span class="sxs-lookup"><span data-stu-id="de6fb-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-155">Numero di nanosecondi da aggiungere al membro dei **secondi** .</span><span class="sxs-lookup"><span data-stu-id="de6fb-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span><span class="sxs-lookup"><span data-stu-id="de6fb-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-157">Tipo di file NFS della condivisione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="de6fb-158">Tipo di file NFS</span><span class="sxs-lookup"><span data-stu-id="de6fb-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="de6fb-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de6fb-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="de6fb-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>tipo di NFS \_ \_ reg</span><span class="sxs-lookup"><span data-stu-id="de6fb-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="de6fb-161">Un file normale.</span><span class="sxs-lookup"><span data-stu-id="de6fb-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="de6fb-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>\_dir tipo \_ NFS</span><span class="sxs-lookup"><span data-stu-id="de6fb-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="de6fb-163">Una directory.</span><span class="sxs-lookup"><span data-stu-id="de6fb-163">A directory.</span></span><br/>              |
| <span data-ttu-id="de6fb-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>tipo di NFS \_ \_ BLK</span><span class="sxs-lookup"><span data-stu-id="de6fb-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="de6fb-165">File speciale di blocco.</span><span class="sxs-lookup"><span data-stu-id="de6fb-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="de6fb-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>tipo di NFS \_ \_ Chr</span><span class="sxs-lookup"><span data-stu-id="de6fb-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="de6fb-167">File speciale di caratteri.</span><span class="sxs-lookup"><span data-stu-id="de6fb-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="de6fb-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>tipo di NFS \_ \_ lnk</span><span class="sxs-lookup"><span data-stu-id="de6fb-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="de6fb-169">Collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="de6fb-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="de6fb-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>tipo di NFS \_ \_ Sock</span><span class="sxs-lookup"><span data-stu-id="de6fb-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="de6fb-171">Un socket di Windows.</span><span class="sxs-lookup"><span data-stu-id="de6fb-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="de6fb-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>tipo di NFS \_ \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="de6fb-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="de6fb-173">Un file FIFO.</span><span class="sxs-lookup"><span data-stu-id="de6fb-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="de6fb-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modalità**</span><span class="sxs-lookup"><span data-stu-id="de6fb-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-175">Modalità file.</span><span class="sxs-lookup"><span data-stu-id="de6fb-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span><span class="sxs-lookup"><span data-stu-id="de6fb-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-177">Numero di collegamenti alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="de6fb-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**</span><span class="sxs-lookup"><span data-stu-id="de6fb-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-179">Identificatore utente (UID) UNIX.</span><span class="sxs-lookup"><span data-stu-id="de6fb-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**GID**</span><span class="sxs-lookup"><span data-stu-id="de6fb-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-181">Identificatore del gruppo UNIX (GID).</span><span class="sxs-lookup"><span data-stu-id="de6fb-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="de6fb-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-183">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="de6fb-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Utilizzato**</span><span class="sxs-lookup"><span data-stu-id="de6fb-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-185">Dimensioni del file utilizzate, in byte.</span><span class="sxs-lookup"><span data-stu-id="de6fb-185">The file size used, in bytes.</span></span> <span data-ttu-id="de6fb-186">Corrisponde alla dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="de6fb-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span><span class="sxs-lookup"><span data-stu-id="de6fb-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-188">Identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de6fb-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span><span class="sxs-lookup"><span data-stu-id="de6fb-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-190">Identificatore file system.</span><span class="sxs-lookup"><span data-stu-id="de6fb-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span><span class="sxs-lookup"><span data-stu-id="de6fb-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-192">Identificatore di file.</span><span class="sxs-lookup"><span data-stu-id="de6fb-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span><span class="sxs-lookup"><span data-stu-id="de6fb-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-194">Ora dell'ultimo accesso.</span><span class="sxs-lookup"><span data-stu-id="de6fb-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span><span class="sxs-lookup"><span data-stu-id="de6fb-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-196">Ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="de6fb-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span><span class="sxs-lookup"><span data-stu-id="de6fb-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-198">Ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="de6fb-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="de6fb-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="de6fb-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-200">Struttura **di \_ \_ attributi di file NFS** .</span><span class="sxs-lookup"><span data-stu-id="de6fb-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="de6fb-201">Per descrizioni più dettagliate dei membri di questa struttura, vedere la struttura **fattr3** nella specifica del protocollo NFS versione 3 (come definito nella [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span><span class="sxs-lookup"><span data-stu-id="de6fb-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="de6fb-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione**</span><span class="sxs-lookup"><span data-stu-id="de6fb-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="de6fb-203">Specifica se la connessione in cui è stato creato l'handle per la condivisione NFS è tramite il protocollo NFS versione 2 o NFS versione 3.</span><span class="sxs-lookup"><span data-stu-id="de6fb-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="de6fb-204">Valore</span><span class="sxs-lookup"><span data-stu-id="de6fb-204">Value</span></span>                            | <span data-ttu-id="de6fb-205">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de6fb-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="de6fb-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="de6fb-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="de6fb-207">NFS versione 2</span><span class="sxs-lookup"><span data-stu-id="de6fb-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="de6fb-208"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="de6fb-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="de6fb-209">NFS versione 3</span><span class="sxs-lookup"><span data-stu-id="de6fb-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de6fb-210">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de6fb-210">Requirements</span></span>



| <span data-ttu-id="de6fb-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="de6fb-211">Requirement</span></span> | <span data-ttu-id="de6fb-212">Valore</span><span class="sxs-lookup"><span data-stu-id="de6fb-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="de6fb-213">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de6fb-213">Minimum supported client</span></span><br/> | <span data-ttu-id="de6fb-214">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="de6fb-214">None supported</span></span><br/>         |
| <span data-ttu-id="de6fb-215">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de6fb-215">Minimum supported server</span></span><br/> | <span data-ttu-id="de6fb-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de6fb-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="de6fb-217">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="de6fb-217">End of client support</span></span><br/>    | <span data-ttu-id="de6fb-218">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="de6fb-218">None supported</span></span><br/>         |
| <span data-ttu-id="de6fb-219">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="de6fb-219">End of server support</span></span><br/>    | <span data-ttu-id="de6fb-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de6fb-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de6fb-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de6fb-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6fb-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="de6fb-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
