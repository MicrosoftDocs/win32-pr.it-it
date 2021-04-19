---
description: 'Altre informazioni su: funzione JetOpenFile'
title: Funzione JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305732"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="888c7-103">Funzione JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="888c7-103">JetOpenFile Function</span></span>


<span data-ttu-id="888c7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="888c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="888c7-105">Funzione JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="888c7-105">JetOpenFile Function</span></span>

<span data-ttu-id="888c7-106">La funzione **JetOpenFile** apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di streaming.</span><span class="sxs-lookup"><span data-stu-id="888c7-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="888c7-107">I dati di questi file possono essere successivamente letti tramite l'handle restituito mediante [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="888c7-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="888c7-108">L'handle restituito deve essere chiuso utilizzando [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="888c7-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="888c7-109">È necessario che un backup esterno dell'istanza sia stato avviato in precedenza utilizzando [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="888c7-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="888c7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="888c7-110">Parameters</span></span>

<span data-ttu-id="888c7-111">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="888c7-111">*szFileName*</span></span>

<span data-ttu-id="888c7-112">Percorso relativo o assoluto di un database collegato, di un file di patch del database o di un file di log delle transazioni gestito dall'istanza di che verrà letta per il backup.</span><span class="sxs-lookup"><span data-stu-id="888c7-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="888c7-113">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="888c7-113">*phfFile*</span></span>

<span data-ttu-id="888c7-114">Buffer di output che riceve un handle per il file da leggere.</span><span class="sxs-lookup"><span data-stu-id="888c7-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="888c7-115">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="888c7-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="888c7-116">Il buffer di output che riceve i bit 32 meno significativi della dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="888c7-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="888c7-117">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="888c7-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="888c7-118">Il buffer di output che riceve i 32 bit più significativi della dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="888c7-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="888c7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="888c7-119">Return Value</span></span>

<span data-ttu-id="888c7-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="888c7-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="888c7-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="888c7-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="888c7-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="888c7-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="888c7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="888c7-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="888c7-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="888c7-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="888c7-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="888c7-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="888c7-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="888c7-127">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="888c7-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="888c7-128">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="888c7-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="888c7-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="888c7-130">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="888c7-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="888c7-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="888c7-132">L'operazione non è riuscita perché non è stato possibile aprire il file richiesto a causa di una violazione di condivisione o di privilegi insufficienti.</span><span class="sxs-lookup"><span data-stu-id="888c7-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="888c7-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="888c7-134">L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="888c7-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="888c7-135">Questo errore verrà restituito solo da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="888c7-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="888c7-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="888c7-137">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="888c7-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="888c7-138">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="888c7-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="888c7-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="888c7-140">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="888c7-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="888c7-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="888c7-142">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="888c7-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="888c7-143">Questo problema può verificarsi per <strong>JetOpenFile</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="888c7-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="888c7-144">L'handle dell'istanza specificato non è valido (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="888c7-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="888c7-145">Il parametro filename specificato è NULL o una stringa di lunghezza zero (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="888c7-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="888c7-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="888c7-147">L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="888c7-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="888c7-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="888c7-149">Non è stato possibile aprire il file richiesto per il backup perché non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="888c7-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="888c7-150">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="888c7-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="888c7-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="888c7-152">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="888c7-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="888c7-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="888c7-154">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="888c7-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="888c7-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="888c7-156">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="888c7-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="888c7-157"><strong>JetOpenFile</strong> restituirà JET_errOutOfMemory se viene effettuato un tentativo di aprire un altro file prima che il file precedente aperto utilizzando <strong>JetOpenFile</strong> sia stato chiuso da <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span><span class="sxs-lookup"><span data-stu-id="888c7-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="888c7-158">Attualmente è supportato un solo handle di file in attesa.</span><span class="sxs-lookup"><span data-stu-id="888c7-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="888c7-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="888c7-160">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="888c7-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="888c7-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="888c7-162">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="888c7-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="888c7-163">JET_errRestoreInProgress non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="888c7-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="888c7-164">In seguito all'esito positivo, verrà restituito un handle per il file richiesto.</span><span class="sxs-lookup"><span data-stu-id="888c7-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="888c7-165">Se l'handle è per un file di database, il file di database verrà preparato per il backup di flusso, che può comportare la creazione di un file di patch del database nello stesso percorso del file di database.</span><span class="sxs-lookup"><span data-stu-id="888c7-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="888c7-166">Il file di patch del database ha esattamente lo stesso percorso e il nome file del file di database, ma dispone di un. Estensione PAT.</span><span class="sxs-lookup"><span data-stu-id="888c7-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="888c7-167">Verranno restituite anche le dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="888c7-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="888c7-168">In caso di errore, lo stato dei buffer di output sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="888c7-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="888c7-169">Un file di patch del database può essere temporaneamente creato sul disco ed è possibile che qualsiasi file esistente nel percorso del file di patch venga eliminato.</span><span class="sxs-lookup"><span data-stu-id="888c7-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="888c7-170">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="888c7-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="888c7-171">In Windows XP e versioni successive, il backup non verrà annullato se è stato effettuato un tentativo di eseguire il backup di un database non collegato all'istanza al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="888c7-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="888c7-172">**Avviso**  di  Per motivi di sicurezza, è importante tenere presente che **JetOpenFile** non verifica che il percorso del file richiesto sia associato al set di file di cui eseguire il backup per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="888c7-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="888c7-173">Di conseguenza, è possibile usare questa funzione per accedere a qualsiasi file che può essere aperto dal contesto di sicurezza corrente del thread.</span><span class="sxs-lookup"><span data-stu-id="888c7-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="888c7-174">È fondamentale che l'applicazione limiti i percorsi passati a questa funzione a un set noto di percorsi di file validi oppure che sia possibile che si verifichi una divulgazione di attacchi informativi.</span><span class="sxs-lookup"><span data-stu-id="888c7-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="888c7-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="888c7-175">Remarks</span></span>

<span data-ttu-id="888c7-176">È necessario che siano presenti i buffer di output delle dimensioni del file e dell'handle.</span><span class="sxs-lookup"><span data-stu-id="888c7-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="888c7-177">Se non sono presenti, il motore si arresterà in modo anomalo perché i parametri del buffer di output non vengono convalidati.</span><span class="sxs-lookup"><span data-stu-id="888c7-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="888c7-178">A questo punto, è possibile aprire un solo file per il backup in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="888c7-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="888c7-179">**JetOpenFile** non dichiara il privilegio di backup prima di aprire il file richiesto.</span><span class="sxs-lookup"><span data-stu-id="888c7-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="888c7-180">La dimensione del file da leggere come indicato da questa funzione potrebbe non corrispondere a quella del file su disco.</span><span class="sxs-lookup"><span data-stu-id="888c7-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="888c7-181">In Windows XP e versioni successive, le informazioni aggiuntive possono essere aggiunte a un file di database utilizzato dal motore di database durante un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="888c7-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="888c7-182">Di conseguenza, l'applicazione deve basarsi solo sulle dimensioni del file restituite da **JetOpenFile** o sul numero effettivo di byte di dati restituiti da [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="888c7-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="888c7-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="888c7-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="888c7-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="888c7-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="888c7-185">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="888c7-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="888c7-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="888c7-187">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="888c7-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-188"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="888c7-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="888c7-189">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="888c7-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-190"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="888c7-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="888c7-191">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="888c7-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888c7-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="888c7-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="888c7-193">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="888c7-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888c7-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="888c7-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="888c7-195">Implementato come <strong>JetOpenFileW</strong> (Unicode) e <strong>JetOpenFileA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="888c7-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="888c7-196">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="888c7-196">See Also</span></span>

[<span data-ttu-id="888c7-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="888c7-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="888c7-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="888c7-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="888c7-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="888c7-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="888c7-200">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="888c7-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="888c7-201">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="888c7-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="888c7-202">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="888c7-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="888c7-203">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="888c7-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="888c7-204">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="888c7-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="888c7-205">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="888c7-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="888c7-206">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="888c7-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="888c7-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="888c7-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="888c7-208">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="888c7-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
