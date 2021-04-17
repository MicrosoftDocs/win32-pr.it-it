---
description: Legge i dati da un file aperto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Funzione NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523177"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="4ed0b-103">NtReadFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ed0b-103">NtReadFile function</span></span>

<span data-ttu-id="4ed0b-104">Legge i dati da un file aperto.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-104">Reads data from an open file.</span></span>

<span data-ttu-id="4ed0b-105">Questa funzione è l'equivalente della modalità utente per la funzione [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentata in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="4ed0b-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed0b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ed0b-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="4ed0b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ed0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ed0b-108">*Filehandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-109">Handle per l'oggetto file.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-109">Handle to the file object.</span></span> <span data-ttu-id="4ed0b-110">Questo handle viene creato da una chiamata riuscita a [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) o [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span><span class="sxs-lookup"><span data-stu-id="4ed0b-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-111">*Evento* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-112">Facoltativamente, un handle a un oggetto evento da impostare sullo stato segnalato dopo il completamento dell'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="4ed0b-113">Il dispositivo e i driver intermedi devono impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-114">*ApcRoutine* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-115">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-115">This parameter is reserved.</span></span> <span data-ttu-id="4ed0b-116">Il puntatore del dispositivo e i driver intermedi devono essere impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-117">*ApcContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-118">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-118">This parameter is reserved.</span></span> <span data-ttu-id="4ed0b-119">Il puntatore del dispositivo e i driver intermedi devono essere impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-120">*IoStatusBlock* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-121">Puntatore a una struttura di [**\_ \_ blocco di stato io**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) che riceve lo stato di completamento finale e le informazioni sull'operazione di lettura richiesta.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="4ed0b-122">Il membro **Information** riceve il numero di byte effettivamente letti dal file.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-123">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-124">Puntatore a un buffer allocato dal chiamante che riceve i dati letti dal file.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-125">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-126">Dimensione, in byte, del buffer a cui punta il *buffer*.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-127">*ByteOffset* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-128">Puntatore a una variabile che specifica l'offset di byte iniziale nel file in cui inizierà l'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="4ed0b-129">Se viene effettuato un tentativo di lettura oltre la fine del file, **NtReadFile** restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="4ed0b-130">Se la chiamata a [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) imposta uno dei flag *createOptions* file di avviso i/o sincrono file \_ O file di i \_ \_ \_ \_ /o sincrono \_ , gestione i/O mantiene la posizione del file corrente.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="4ed0b-131">In tal caso, il chiamante di **NtReadFile** può specificare che venga utilizzato l'offset della posizione corrente del file anziché un valore *ByteOffset* esplicito.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="4ed0b-132">Questa specifica può essere eseguita utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ed0b-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="4ed0b-133">Specificare un puntatore a un **valore \_ Integer grande** con il membro **HighPart** impostato su-1 e il membro **LowPart** impostato sul file di valori definito dal sistema \_ utilizzare la posizione del puntatore del \_ file \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed0b-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="4ed0b-134">Passare un puntatore **null** per *ByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="4ed0b-135">**NtReadFile** aggiorna la posizione corrente del file aggiungendo il numero di byte letti quando viene completata l'operazione di lettura, se usa la posizione del file corrente gestita dal gestore di i/O.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="4ed0b-136">Anche quando gestione i/O gestisce la posizione corrente del file, il chiamante può reimpostare questa posizione passando un valore *ByteOffset* esplicito a **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="4ed0b-137">In questo modo viene automaticamente modificata la posizione del file corrente in quel valore di *ByteOffset* , viene eseguita l'operazione di lettura e quindi la posizione viene aggiornata in base al numero di byte effettivamente letti.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="4ed0b-138">Questa tecnica fornisce al chiamante il servizio di ricerca e lettura atomiche.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="4ed0b-139">*Chiave* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed0b-140">Il puntatore del dispositivo e i driver intermedi devono essere impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ed0b-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ed0b-141">Return value</span></span>

<span data-ttu-id="4ed0b-142">**NtReadFile** restituisce \_ l'esito positivo dello stato o il codice di errore NTSTATUS appropriato.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed0b-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ed0b-143">Remarks</span></span>

<span data-ttu-id="4ed0b-144">I chiamanti di **NtReadFile** devono avere già chiamato [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) con i dati di lettura del file \_ o il \_ \_ valore di lettura generico impostato nel parametro *desiredAccess* .</span><span class="sxs-lookup"><span data-stu-id="4ed0b-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="4ed0b-145">Se la chiamata precedente a [**NTCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) impostano \_ il \_ \_ flag di buffering intermedio nel parametro *createOptions* su **NTCreateFile**, i parametri *length* e *ByteOffset* per **NtReadFile** devono essere multipli delle dimensioni del settore.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="4ed0b-146">Per ulteriori informazioni, vedere **NTCreateFile**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="4ed0b-147">**NtReadFile** inizia la lettura dal *ByteOffset* specificato o dalla posizione corrente del file nel *buffer* specificato.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="4ed0b-148">Termina l'operazione di lettura in una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ed0b-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="4ed0b-149">Il buffer è pieno perché il numero di byte specificato dal parametro *length* è stato letto.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="4ed0b-150">Pertanto, non è possibile inserire più dati nel buffer senza un overflow.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="4ed0b-151">Viene raggiunta la fine del file durante l'operazione di lettura, pertanto non sono presenti altri dati nel file da trasferire nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="4ed0b-152">Se il chiamante ha aperto il file con il flag SYNCHRONIZE impostato in *desiredAccess*, il thread chiamante può eseguire la sincronizzazione fino al completamento dell'operazione di lettura in attesa dell'handle di file, *filehandle*.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="4ed0b-153">L'handle viene segnalato ogni volta che viene completata un'operazione di I/O eseguita nell'handle.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="4ed0b-154">Tuttavia, il chiamante non deve attendere un handle che è stato aperto per l'accesso sincrono al file, ovvero un avviso di i/o sincrono di file \_ \_ o file di i \_ /o \_ sincrono \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4ed0b-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="4ed0b-155">In questo caso, **NtReadFile** attende per conto del chiamante e non restituisce alcun risultato fino a quando l'operazione di lettura non viene completata.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="4ed0b-156">Il chiamante può attendere in modo sicuro l'handle di file solo se vengono soddisfatte tutte e tre le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ed0b-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="4ed0b-157">L'handle è stato aperto per l'accesso asincrono, ovvero non \_ \_ \_  è stato specificato alcun flag i/o sincrono dei file.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="4ed0b-158">L'handle viene utilizzato solo per un'operazione di I/O alla volta.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="4ed0b-159">**NtReadFile** ha restituito lo stato \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="4ed0b-160">Un driver deve chiamare **NtReadFile** nel contesto del processo di sistema se sussistono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ed0b-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="4ed0b-161">Il driver ha creato l'handle di file che passa a **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="4ed0b-162">**NtReadFile** invierà una notifica al driver del completamento i/O per mezzo di un evento creato dal driver.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="4ed0b-163">**NtReadFile** invierà una notifica al driver del completamento i/O per mezzo di una routine di callback APC che il driver passa a **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="4ed0b-164">Gli handle di file e di evento sono validi solo nel contesto di processo in cui vengono creati gli handle.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="4ed0b-165">Pertanto, per evitare problemi di sicurezza, il driver deve creare qualsiasi handle di file o evento che passa a **NtReadFile** nel contesto del processo di sistema piuttosto che del contesto del processo in cui si trova il driver.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="4ed0b-166">Analogamente, **NtReadFile** deve essere chiamato nel contesto del processo di sistema se notifica al driver il completamento i/o per mezzo di un APC, perché APC vengono sempre attivati nel contesto del thread che rilascia la richiesta di i/o.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="4ed0b-167">Se il driver chiama **NtReadFile** nel contesto di un processo diverso da quello del sistema, l'APC potrebbe essere ritardato per un periodo illimitato o potrebbe non essere attivato.</span><span class="sxs-lookup"><span data-stu-id="4ed0b-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="4ed0b-168">Per ulteriori informazioni sull'utilizzo dei file, vedere [utilizzo di file in un driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span><span class="sxs-lookup"><span data-stu-id="4ed0b-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="4ed0b-169">I chiamanti di **NtReadFile** devono essere in esecuzione al livello livello IRQL = passive \_ e [con APC kernel speciale abilitato](/windows-hardware/drivers/kernel/disabling-apcs).</span><span class="sxs-lookup"><span data-stu-id="4ed0b-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed0b-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ed0b-170">Requirements</span></span>



| <span data-ttu-id="4ed0b-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed0b-171">Requirement</span></span> | <span data-ttu-id="4ed0b-172">Valore</span><span class="sxs-lookup"><span data-stu-id="4ed0b-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed0b-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ed0b-173">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed0b-174">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="4ed0b-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ed0b-175">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed0b-176">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ed0b-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="4ed0b-177">Piattaforma di destinazione</span><span class="sxs-lookup"><span data-stu-id="4ed0b-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="4ed0b-178"><dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed0b-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="4ed0b-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ed0b-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed0b-180"><dt>WDM. h (include WDM. h, ntddk. h o Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed0b-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="4ed0b-181">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ed0b-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ed0b-182"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ed0b-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ed0b-183">DLL</span><span class="sxs-lookup"><span data-stu-id="4ed0b-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ed0b-184"><dt>Ntdll.dll (modalità utente)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed0b-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="4ed0b-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ed0b-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed0b-186">**KeInitializeEvent**</span><span class="sxs-lookup"><span data-stu-id="4ed0b-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="4ed0b-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="4ed0b-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="4ed0b-188">**NtQueryInformationFile**</span><span class="sxs-lookup"><span data-stu-id="4ed0b-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="4ed0b-189">**NtSetInformationFile**</span><span class="sxs-lookup"><span data-stu-id="4ed0b-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="4ed0b-190">**NtWriteFile**</span><span class="sxs-lookup"><span data-stu-id="4ed0b-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
