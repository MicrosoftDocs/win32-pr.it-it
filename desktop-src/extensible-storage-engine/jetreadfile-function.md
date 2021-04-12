---
description: 'Altre informazioni su: funzione JetReadFile'
title: JetReadFile (funzione)
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232555"
---
# <a name="jetreadfile-function"></a><span data-ttu-id="f07f9-103">JetReadFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="f07f9-103">JetReadFile Function</span></span>


<span data-ttu-id="f07f9-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f07f9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="f07f9-105">JetReadFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="f07f9-105">JetReadFile Function</span></span>

<span data-ttu-id="f07f9-106">La funzione **JetReadFile** Recupera il contenuto di un file aperto con [JetOpenFile](./jetopenfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="f07f9-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="f07f9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f07f9-107">Parameters</span></span>

<span data-ttu-id="f07f9-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="f07f9-108">*hfFile*</span></span>

<span data-ttu-id="f07f9-109">Handle del file da leggere.</span><span class="sxs-lookup"><span data-stu-id="f07f9-109">The handle of the file to be read.</span></span>

<span data-ttu-id="f07f9-110">*PV*</span><span class="sxs-lookup"><span data-stu-id="f07f9-110">*pv*</span></span>

<span data-ttu-id="f07f9-111">Buffer di output che riceverà i dati del file.</span><span class="sxs-lookup"><span data-stu-id="f07f9-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="f07f9-112">*CB*</span><span class="sxs-lookup"><span data-stu-id="f07f9-112">*cb*</span></span>

<span data-ttu-id="f07f9-113">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="f07f9-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="f07f9-114">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="f07f9-114">*pcbActual*</span></span>

<span data-ttu-id="f07f9-115">Riceve la quantità effettiva di dati di file recuperati.</span><span class="sxs-lookup"><span data-stu-id="f07f9-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="f07f9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f07f9-116">Return Value</span></span>

<span data-ttu-id="f07f9-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f07f9-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f07f9-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f07f9-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f07f9-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f07f9-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="f07f9-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f07f9-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f07f9-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f07f9-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f07f9-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="f07f9-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="f07f9-124">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f07f9-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="f07f9-125">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f07f9-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f07f9-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f07f9-127">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f07f9-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f07f9-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f07f9-129">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="f07f9-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f07f9-130">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f07f9-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f07f9-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f07f9-132">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="f07f9-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="f07f9-133">Questo problema può verificarsi per <strong>JetReadFile</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="f07f9-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="f07f9-134">L'handle dell'istanza specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f07f9-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="f07f9-135">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f07f9-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="f07f9-136">La dimensione del buffer di output non è un multiplo delle dimensioni della pagina del database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="f07f9-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="f07f9-137">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f07f9-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="f07f9-138">Le dimensioni del buffer di output sono inferiori a tre pagine di database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ed è la prima chiamata a <strong>JetReadFile</strong> per l'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="f07f9-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="f07f9-139">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f07f9-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="f07f9-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="f07f9-141">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="f07f9-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f07f9-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f07f9-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="f07f9-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="f07f9-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="f07f9-145">Operazione non riuscita perché è stato rilevato un danneggiamento dei dati non ripristinabili durante la lettura di una pagina del database da un file di database o un file di patch del database.</span><span class="sxs-lookup"><span data-stu-id="f07f9-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="f07f9-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="f07f9-147">Operazione non riuscita perché è stato rilevato un danneggiamento dei dati non ripristinabili durante la lettura di un file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="f07f9-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="f07f9-148">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f07f9-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f07f9-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f07f9-150">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="f07f9-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f07f9-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f07f9-152">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="f07f9-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f07f9-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f07f9-154">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="f07f9-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f07f9-155">In seguito all'esito positivo, il blocco di dati successivo del file verrà letto nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="f07f9-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="f07f9-156">Verrà restituito anche il numero effettivo di byte recuperati.</span><span class="sxs-lookup"><span data-stu-id="f07f9-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="f07f9-157">L'offset del file in corrispondenza del quale verrà eseguita la lettura successiva verrà spostato in base a questa quantità.</span><span class="sxs-lookup"><span data-stu-id="f07f9-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="f07f9-158">In caso di errore, lo stato del buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="f07f9-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="f07f9-159">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="f07f9-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="f07f9-160">In Windows XP e versioni successive, il backup non verrà annullato se si è verificato un errore durante la lettura di un file di database.</span><span class="sxs-lookup"><span data-stu-id="f07f9-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="f07f9-161">Tuttavia, il backup del file di database verrà comunque annullato e l'handle corrispondente verrà chiuso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f07f9-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f07f9-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="f07f9-162">Remarks</span></span>

<span data-ttu-id="f07f9-163">Qualsiasi chiamata a **JetReadFile** utilizzando un handle che ha già restituito tutti i dati nel file sottostante, ad esempio una chiamata precedente restituita meno byte rispetto alla dimensione del buffer di output, avrà sempre esito positivo ma restituirà sempre zero byte di dati.</span><span class="sxs-lookup"><span data-stu-id="f07f9-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="f07f9-164">Per ottimizzare le prestazioni del backup, è necessario utilizzare un buffer di output di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f07f9-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="f07f9-165">Potrebbe essere necessaria una sperimentazione per individuare il compromesso giusto tra il consumo di risorse e la velocità effettiva per una determinata situazione.</span><span class="sxs-lookup"><span data-stu-id="f07f9-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="f07f9-166">Il buffer di output non deve essere minore di 64KB in qualsiasi caso.</span><span class="sxs-lookup"><span data-stu-id="f07f9-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="f07f9-167">Non sono supportate più chiamate simultanee a **JetReadFile** con lo stesso handle di file.</span><span class="sxs-lookup"><span data-stu-id="f07f9-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="f07f9-168">Ciò significa che non è possibile accodare diversi buffer per la lettura simultanea nello stesso file per ottenere una velocità effettiva elevata sequenziale.</span><span class="sxs-lookup"><span data-stu-id="f07f9-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="f07f9-169">In alternativa, è necessario usare un singolo buffer di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f07f9-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="f07f9-170">Se l'istanza è configurata in modo che lo scrubbing della pagina del database sia abilitato (vedere JET_paramZeroDatabaseDuringBackup nei parametri di sistema), i dati eliminati verranno rimossi dal database come effetto collaterale di una chiamata a **JetReadFile** rispetto al file di database.</span><span class="sxs-lookup"><span data-stu-id="f07f9-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="f07f9-171">È molto importante comprendere in che modo il backup e il danneggiamento dei dati interagiscono.</span><span class="sxs-lookup"><span data-stu-id="f07f9-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="f07f9-172">Se il motore di database rileva il danneggiamento dei dati durante un backup, il backup del database interessato o dell'intera istanza avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f07f9-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="f07f9-173">Si tratta di una decisione di progettazione consapevole per la protezione dalla perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="f07f9-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="f07f9-174">Se il motore di database ha consentito la riuscita di un backup in cui è presente il danneggiamento dei dati, è possibile che un backup precedente non danneggiato possa essere scartato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="f07f9-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="f07f9-175">Si tratta di un peccato perché sarebbe possibile correggere il danneggiamento dei dati nell'istanza di Live ripristinando tale backup e riproducendo tutti i file di log delle transazioni su tale database.</span><span class="sxs-lookup"><span data-stu-id="f07f9-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="f07f9-176">Questo scenario con zero perdite di dati presuppone che la registrazione circolare non sia abilitata (vedere [JET_paramCircularLog](./transaction-log-parameters.md) nei [parametri di sistema](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="f07f9-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="f07f9-177">È inoltre importante comprendere che, quando è presente il danneggiamento dei dati, il backup di flusso sarà il posto più probabile che verrà prima rilevato.</span><span class="sxs-lookup"><span data-stu-id="f07f9-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="f07f9-178">Questo avviene perché il backup di flusso è l'unico processo che esegue periodicamente l'analisi di ogni singola pagina del file di database.</span><span class="sxs-lookup"><span data-stu-id="f07f9-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="f07f9-179">È anche probabile che il backup di flusso sia il primo processo per rilevare i primi segni di errore hardware, come manifestato da errori di danneggiamento dei dati intermittenti.</span><span class="sxs-lookup"><span data-stu-id="f07f9-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="f07f9-180">Ciò è dovuto alla quantità di dati recuperati da backup e alla velocità con cui viene recuperato.</span><span class="sxs-lookup"><span data-stu-id="f07f9-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="f07f9-181">Il danneggiamento dei dati viene rilevato dal motore di database tramite l'utilizzo di checksum dei blocchi.</span><span class="sxs-lookup"><span data-stu-id="f07f9-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="f07f9-182">Questi checksum vengono impostati immediatamente prima della scrittura di una pagina del database e vengono verificati in una pagina di database letta.</span><span class="sxs-lookup"><span data-stu-id="f07f9-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="f07f9-183">Questo schema consente al motore di database di determinare che i dati sono stati danneggiati a un certo punto, ma non consente al motore di database di determinare l'origine di tale danneggiamento.</span><span class="sxs-lookup"><span data-stu-id="f07f9-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="f07f9-184">In passato, la ragione principale di tale danneggiamento è stata rilevata da origini diverse dal motore di database stesso.</span><span class="sxs-lookup"><span data-stu-id="f07f9-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f07f9-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f07f9-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f07f9-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f07f9-187">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f07f9-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f07f9-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f07f9-189">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f07f9-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-190"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f07f9-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f07f9-191">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f07f9-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07f9-192"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f07f9-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f07f9-193">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f07f9-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07f9-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f07f9-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f07f9-195">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f07f9-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f07f9-196">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f07f9-196">See Also</span></span>

[<span data-ttu-id="f07f9-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f07f9-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f07f9-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="f07f9-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="f07f9-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f07f9-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f07f9-200">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="f07f9-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f07f9-201">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f07f9-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="f07f9-202">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="f07f9-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
