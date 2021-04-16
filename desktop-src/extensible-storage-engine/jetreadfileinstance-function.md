---
description: 'Altre informazioni su: funzione JetReadFileInstance'
title: Funzione JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524960"
---
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="3586f-103">Funzione JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="3586f-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="3586f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3586f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="3586f-105">Funzione JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="3586f-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="3586f-106">La funzione **JetReadFileInstance** Recupera il contenuto di un file aperto con la funzione [JetOpenFileInstance](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3586f-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="3586f-107">**Windows XP**:   **JetReadFileInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3586f-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="3586f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3586f-108">Parameters</span></span>

<span data-ttu-id="3586f-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="3586f-109">*instance*</span></span>

<span data-ttu-id="3586f-110">Istanza di da utilizzare per una particolare chiamata API.</span><span class="sxs-lookup"><span data-stu-id="3586f-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="3586f-111">Si noti che per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="3586f-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="3586f-112">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="3586f-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="3586f-113">Per Windows XP e versioni successive, è possibile chiamare la variante API che non accetta questo parametro solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) nei casi in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="3586f-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="3586f-114">In caso contrario, l'operazione avrà esito negativo e restituirà l'errore JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="3586f-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="3586f-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="3586f-115">*hfFile*</span></span>

<span data-ttu-id="3586f-116">Handle del file da leggere.</span><span class="sxs-lookup"><span data-stu-id="3586f-116">The handle of the file to be read.</span></span>

<span data-ttu-id="3586f-117">*PV*</span><span class="sxs-lookup"><span data-stu-id="3586f-117">*pv*</span></span>

<span data-ttu-id="3586f-118">Buffer di output che riceverà i dati del file.</span><span class="sxs-lookup"><span data-stu-id="3586f-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="3586f-119">*CB*</span><span class="sxs-lookup"><span data-stu-id="3586f-119">*cb*</span></span>

<span data-ttu-id="3586f-120">Dimensione massima, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="3586f-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="3586f-121">*PCB*</span><span class="sxs-lookup"><span data-stu-id="3586f-121">*pcb*</span></span>

<span data-ttu-id="3586f-122">Quantità effettiva di dati recuperati dal file.</span><span class="sxs-lookup"><span data-stu-id="3586f-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="3586f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3586f-123">Return Value</span></span>

<span data-ttu-id="3586f-124">Questa funzione semplifica la restituzione di qualsiasi tipo di dati [JET_ERR](./jet-err.md) definiti nell'API ESE (Extensible Storage Engine).</span><span class="sxs-lookup"><span data-stu-id="3586f-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="3586f-125">Per altre informazioni sugli errori di JET, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.</span><span class="sxs-lookup"><span data-stu-id="3586f-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3586f-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3586f-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="3586f-127">Significato</span><span class="sxs-lookup"><span data-stu-id="3586f-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3586f-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3586f-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3586f-129">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3586f-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="3586f-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="3586f-131">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="3586f-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="3586f-132">Questo errore viene restituito solo da Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3586f-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3586f-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3586f-134">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="3586f-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3586f-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3586f-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="3586f-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="3586f-137">Questo errore viene restituito solo da Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3586f-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3586f-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3586f-139">Uno dei parametri specificati contiene un valore imprevisto o un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="3586f-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="3586f-140">Questa situazione può verificarsi per la funzione <strong>JetReadFileInstance</strong> quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3586f-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="3586f-141">L'handle dell'istanza specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3586f-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="3586f-142">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3586f-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="3586f-143">La dimensione del buffer di output non è un multiplo delle dimensioni della pagina del database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="3586f-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="3586f-144">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3586f-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="3586f-145">Le dimensioni del buffer di output sono inferiori a tre pagine di database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ed è la prima chiamata alla funzione <strong>JetReadFileInstance</strong> per l'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="3586f-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="3586f-146">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3586f-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="3586f-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="3586f-148">Operazione non riuscita perché è stato rilevato un danneggiamento dei dati irreversibile durante la lettura di un file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="3586f-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="3586f-149">Questo errore viene restituito solo da Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="3586f-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="3586f-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="3586f-151">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="3586f-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3586f-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3586f-153">Non è possibile completare l'operazione perché l'istanza associata a questa sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="3586f-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="3586f-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="3586f-155">Operazione non riuscita perché è stato rilevato un danneggiamento dei dati irreversibile durante la lettura di una pagina del database da un file di database o da un file di patch del database.</span><span class="sxs-lookup"><span data-stu-id="3586f-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3586f-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3586f-157">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata a questa sessione.</span><span class="sxs-lookup"><span data-stu-id="3586f-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="3586f-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="3586f-159">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) nel caso in cui sia supportata una sola istanza, ma esistono già più istanze.</span><span class="sxs-lookup"><span data-stu-id="3586f-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3586f-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3586f-161">Non è possibile completare l'operazione perché l'istanza associata a questa sessione è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="3586f-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3586f-162">In seguito all'esito positivo, il blocco di dati successivo del file verrà letto nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="3586f-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="3586f-163">Verrà restituito anche il numero effettivo di byte recuperati.</span><span class="sxs-lookup"><span data-stu-id="3586f-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="3586f-164">L'offset del file in corrispondenza del quale verrà eseguita la lettura successiva verrà spostato in base a questa quantità.</span><span class="sxs-lookup"><span data-stu-id="3586f-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="3586f-165">In caso di errore, lo stato del buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="3586f-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="3586f-166">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="3586f-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="3586f-167">In Windows XP e versioni successive di Windows, il backup non verrà annullato se si è verificato un errore durante la lettura di un file di database.</span><span class="sxs-lookup"><span data-stu-id="3586f-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="3586f-168">Tuttavia, il backup del file di database verrà comunque annullato e l'handle corrispondente verrà chiuso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3586f-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3586f-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="3586f-169">Remarks</span></span>

<span data-ttu-id="3586f-170">Qualsiasi chiamata alla funzione **JetReadFileInstance** eseguita usando un handle che ha già restituito tutti i dati nel file sottostante (ad esempio se una chiamata precedente ha restituito un minor numero di byte rispetto alla dimensione del buffer di output) avrà sempre esito positivo ma restituirà zero byte di dati.</span><span class="sxs-lookup"><span data-stu-id="3586f-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="3586f-171">Per ottimizzare le prestazioni del backup, è necessario utilizzare un buffer di output di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3586f-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="3586f-172">Potrebbe essere necessario sperimentare per individuare il compromesso ottimale tra l'utilizzo delle risorse e la velocità effettiva per una particolare situazione.</span><span class="sxs-lookup"><span data-stu-id="3586f-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="3586f-173">In ogni caso, il buffer di output non deve essere inferiore a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="3586f-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="3586f-174">Il puntatore passato a **JetReadFileInstance** deve essere allineato con un limite della pagina di memoria (4 KB o 8 KB).</span><span class="sxs-lookup"><span data-stu-id="3586f-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="3586f-175">Questa operazione può essere eseguita chiamando la funzione **VirtualAlloc** .</span><span class="sxs-lookup"><span data-stu-id="3586f-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="3586f-176">Non sono supportate più chiamate simultanee a **JetReadFileInstance** effettuate usando lo stesso handle di file.</span><span class="sxs-lookup"><span data-stu-id="3586f-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="3586f-177">Ciò significa che non è possibile accodare diversi buffer per la lettura simultanea sullo stesso file per ottenere una velocità effettiva elevata sequenziale.</span><span class="sxs-lookup"><span data-stu-id="3586f-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="3586f-178">Usare invece un solo buffer di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3586f-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="3586f-179">Se è stata configurata una particolare istanza in modo che lo scrubbing della pagina del database sia abilitato (vedere il [JET_paramCircularLog](./transaction-log-parameters.md) parametro nei [parametri di sistema](./extensible-storage-engine-system-parameters.md)), i dati eliminati verranno rimossi dal database come effetto collaterale di una chiamata a **JetReadFileInstance** sul file di database.</span><span class="sxs-lookup"><span data-stu-id="3586f-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="3586f-180">È molto importante comprendere in che modo il backup e il danneggiamento dei dati interagiscono.</span><span class="sxs-lookup"><span data-stu-id="3586f-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="3586f-181">Se il motore di database rileva il danneggiamento dei dati durante un backup, il backup del database interessato o dell'intera istanza avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3586f-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="3586f-182">Si tratta di una decisione di progettazione consapevole per la protezione dalla perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="3586f-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="3586f-183">Se il motore di database ha consentito la riuscita di un backup in cui è presente il danneggiamento dei dati, è possibile che un backup precedente non danneggiato possa essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="3586f-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="3586f-184">Si tratta di un peccato perché sarebbe possibile correggere il danneggiamento dei dati nell'istanza di Live ripristinando tale backup e riproducendo tutti i file di log delle transazioni su tale database.</span><span class="sxs-lookup"><span data-stu-id="3586f-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="3586f-185">Questo scenario di perdita di dati zero presuppone che la registrazione circolare non sia abilitata (vedere [JET_paramCircularLog](./transaction-log-parameters.md) nei [parametri di sistema](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="3586f-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="3586f-186">È inoltre importante comprendere che in genere i casi di danneggiamento dei dati vengono rilevati per la prima volta durante il backup di flusso.</span><span class="sxs-lookup"><span data-stu-id="3586f-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="3586f-187">Questo perché il backup di flusso è l'unico processo che esegue periodicamente l'analisi di ogni singola pagina del file di database.</span><span class="sxs-lookup"><span data-stu-id="3586f-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="3586f-188">È anche probabile che il backup di flusso sia il primo processo per rilevare i primi segni di errore hardware, come manifestato da errori di danneggiamento dei dati intermittenti, a causa della quantità di dati recuperati dal backup e della velocità di recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="3586f-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="3586f-189">Il danneggiamento dei dati viene rilevato dal motore di database tramite l'utilizzo di checksum dei blocchi.</span><span class="sxs-lookup"><span data-stu-id="3586f-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="3586f-190">Questi checksum vengono impostati immediatamente prima della scrittura di una pagina del database e vengono verificati in una pagina di database letta.</span><span class="sxs-lookup"><span data-stu-id="3586f-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="3586f-191">Questo schema consente al motore di database di determinare che i dati sono stati danneggiati a un certo punto, ma non consente al motore di database di determinare l'origine di tale danneggiamento.</span><span class="sxs-lookup"><span data-stu-id="3586f-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="3586f-192">Storicamente, le istanze di tali dati danneggiate sono state originate da origini diverse dal motore di database stesso.</span><span class="sxs-lookup"><span data-stu-id="3586f-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3586f-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3586f-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3586f-194">Client</span><span class="sxs-lookup"><span data-stu-id="3586f-194">Client</span></span></p></td>
<td><p><span data-ttu-id="3586f-195">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3586f-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-196">Server</span><span class="sxs-lookup"><span data-stu-id="3586f-196">Server</span></span></p></td>
<td><p><span data-ttu-id="3586f-197">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3586f-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-198">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3586f-198">Header</span></span></p></td>
<td><p><span data-ttu-id="3586f-199">Viene dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3586f-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3586f-200">Libreria</span><span class="sxs-lookup"><span data-stu-id="3586f-200">Library</span></span></p></td>
<td><p><span data-ttu-id="3586f-201">USA ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3586f-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3586f-202">DLL</span><span class="sxs-lookup"><span data-stu-id="3586f-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="3586f-203">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3586f-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3586f-204">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3586f-204">See Also</span></span>

[<span data-ttu-id="3586f-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3586f-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3586f-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="3586f-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="3586f-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3586f-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="3586f-208">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="3586f-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="3586f-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="3586f-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="3586f-210">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="3586f-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
