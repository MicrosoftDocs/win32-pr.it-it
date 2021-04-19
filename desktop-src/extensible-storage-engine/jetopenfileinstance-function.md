---
description: 'Altre informazioni su: funzione JetOpenFileInstance'
title: Funzione JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319630"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="563e8-103">Funzione JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="563e8-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="563e8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="563e8-105">Funzione JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="563e8-106">La funzione **JetOpenFileInstance** apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di streaming.</span><span class="sxs-lookup"><span data-stu-id="563e8-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="563e8-107">I dati di questi file possono essere successivamente letti tramite l'handle restituito mediante [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="563e8-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="563e8-108">L'handle restituito deve essere chiuso utilizzando [JetCloseFileInstance](./jetclosefileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="563e8-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="563e8-109">È necessario che un backup esterno dell'istanza sia stato avviato in precedenza utilizzando [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="563e8-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="563e8-110">**Windows XP:**  **JetOpenFileInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="563e8-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="563e8-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="563e8-111">Parameters</span></span>

<span data-ttu-id="563e8-112">*istanza*</span><span class="sxs-lookup"><span data-stu-id="563e8-112">*instance*</span></span>

<span data-ttu-id="563e8-113">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="563e8-113">The instance to use for this call.</span></span>

<span data-ttu-id="563e8-114">Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="563e8-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="563e8-115">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="563e8-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="563e8-116">Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="563e8-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="563e8-117">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="563e8-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="563e8-118">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="563e8-118">*szFileName*</span></span>

<span data-ttu-id="563e8-119">Percorso relativo o assoluto di un database collegato, di un file di patch del database o di un file di log delle transazioni gestito dall'istanza di letta per il backup.</span><span class="sxs-lookup"><span data-stu-id="563e8-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="563e8-120">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="563e8-120">*phfFile*</span></span>

<span data-ttu-id="563e8-121">Puntatore al buffer di output che riceve un handle per il file da leggere.</span><span class="sxs-lookup"><span data-stu-id="563e8-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="563e8-122">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="563e8-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="563e8-123">Puntatore al buffer di output che riceve i 32 bit meno significativi della dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="563e8-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="563e8-124">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="563e8-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="563e8-125">Puntatore al buffer di output che riceve i 32 bit più significativi della dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="563e8-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="563e8-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="563e8-126">Return Value</span></span>

<span data-ttu-id="563e8-127">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="563e8-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="563e8-128">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="563e8-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="563e8-129">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="563e8-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="563e8-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="563e8-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="563e8-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="563e8-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="563e8-132">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="563e8-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="563e8-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="563e8-134">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="563e8-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="563e8-135">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="563e8-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="563e8-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="563e8-137">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="563e8-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="563e8-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="563e8-139">L'operazione non è riuscita perché non è stato possibile aprire il file richiesto a causa di una violazione di condivisione o di privilegi insufficienti.</span><span class="sxs-lookup"><span data-stu-id="563e8-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="563e8-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="563e8-141">L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="563e8-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="563e8-142">Questo errore verrà restituito solo da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="563e8-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="563e8-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="563e8-144">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="563e8-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="563e8-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="563e8-146">L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="563e8-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="563e8-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="563e8-148">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="563e8-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="563e8-149">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="563e8-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="563e8-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="563e8-151">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="563e8-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="563e8-152">Questo problema può verificarsi per <strong>JetOpenFileInstance</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="563e8-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="563e8-153">L'handle dell'istanza specificato non è valido (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="563e8-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="563e8-154">Il parametro filename specificato è NULL o una stringa di lunghezza zero (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="563e8-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="563e8-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="563e8-156">Non è stato possibile aprire il file richiesto per il backup perché non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="563e8-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="563e8-157">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="563e8-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="563e8-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="563e8-159">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="563e8-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="563e8-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="563e8-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="563e8-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="563e8-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="563e8-163">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="563e8-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="563e8-164"><strong>JetOpenFileInstance</strong> restituirà JET_errOutOfMemory se viene effettuato un tentativo di aprire un altro file prima che il file precedente aperto utilizzando <strong>JetOpenFileInstance</strong> sia stato chiuso da <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="563e8-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="563e8-165">Attualmente è supportato un solo handle di file in attesa.</span><span class="sxs-lookup"><span data-stu-id="563e8-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="563e8-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="563e8-167">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="563e8-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="563e8-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="563e8-169">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="563e8-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="563e8-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="563e8-171">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="563e8-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="563e8-172">In seguito all'esito positivo, viene restituito un handle per il file richiesto.</span><span class="sxs-lookup"><span data-stu-id="563e8-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="563e8-173">Se l'handle è per un file di database, il file di database verrà preparato per un backup di flusso, che può comportare la creazione di un file di patch del database nello stesso percorso del file di database.</span><span class="sxs-lookup"><span data-stu-id="563e8-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="563e8-174">Il file di patch del database ha esattamente lo stesso percorso e il nome del file di database, ma con. Estensione PAT.</span><span class="sxs-lookup"><span data-stu-id="563e8-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="563e8-175">Verranno restituite anche le dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="563e8-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="563e8-176">In caso di errore, lo stato dei buffer di output sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="563e8-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="563e8-177">Un file di patch del database può essere temporaneamente creato sul disco ed è possibile che qualsiasi file esistente nel percorso del file di patch venga eliminato.</span><span class="sxs-lookup"><span data-stu-id="563e8-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="563e8-178">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="563e8-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="563e8-179">In Windows XP e versioni successive, il backup non verrà annullato se è stato effettuato un tentativo di eseguire il backup di un database non collegato all'istanza al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="563e8-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="563e8-180">**Avviso**  di  Per motivi di sicurezza, è importante tenere presente che **JetOpenFileInstance** non verifica che il percorso del file richiesto sia associato al set di file di cui viene eseguito il backup per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="563e8-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="563e8-181">Di conseguenza, è possibile usare questa funzione per accedere a qualsiasi file che può essere aperto dal contesto di sicurezza corrente del thread.</span><span class="sxs-lookup"><span data-stu-id="563e8-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="563e8-182">È fondamentale che l'applicazione limiti i percorsi passati a questa funzione a un set noto di percorsi di file validi oppure che sia possibile che si verifichi una divulgazione di attacchi informativi.</span><span class="sxs-lookup"><span data-stu-id="563e8-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="563e8-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="563e8-183">Remarks</span></span>

<span data-ttu-id="563e8-184">È necessario che siano presenti i buffer di output delle dimensioni del file e dell'handle.</span><span class="sxs-lookup"><span data-stu-id="563e8-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="563e8-185">Se non sono presenti, il motore si arresterà in modo anomalo perché i parametri del buffer di output non vengono convalidati.</span><span class="sxs-lookup"><span data-stu-id="563e8-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="563e8-186">A questo punto, è possibile aprire un solo file per il backup in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="563e8-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="563e8-187">**JetOpenFileInstance** non dichiara il privilegio di backup prima di aprire il file richiesto.</span><span class="sxs-lookup"><span data-stu-id="563e8-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="563e8-188">La dimensione del file da leggere come indicato da questa funzione potrebbe non corrispondere a quella del file su disco.</span><span class="sxs-lookup"><span data-stu-id="563e8-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="563e8-189">In Windows XP e versioni successive, le informazioni aggiuntive possono essere aggiunte a un file di database utilizzato dal motore di database durante un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="563e8-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="563e8-190">Di conseguenza, l'applicazione deve basarsi solo sulle dimensioni del file restituite da **JetOpenFileInstance** o sul numero effettivo di byte di dati restituiti da [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="563e8-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="563e8-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="563e8-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="563e8-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="563e8-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="563e8-193">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="563e8-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="563e8-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="563e8-195">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="563e8-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-196"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="563e8-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="563e8-197">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="563e8-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-198"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="563e8-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="563e8-199">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="563e8-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="563e8-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="563e8-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="563e8-201">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="563e8-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="563e8-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="563e8-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="563e8-203">Implementato come <strong>JetOpenFileInstanceW</strong> (Unicode) e <strong>JetOpenFileInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="563e8-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="563e8-204">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="563e8-204">See Also</span></span>

[<span data-ttu-id="563e8-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="563e8-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="563e8-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="563e8-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="563e8-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="563e8-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="563e8-208">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="563e8-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="563e8-209">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="563e8-210">JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="563e8-211">JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="563e8-212">JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="563e8-213">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="563e8-214">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="563e8-215">JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="563e8-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
