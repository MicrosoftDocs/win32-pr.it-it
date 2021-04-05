---
description: 'Altre informazioni su: funzione JetRestore'
title: Funzione JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ed164bb6775150f9745cb0e6d9b158a5f03f146
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969541"
---
# <a name="jetrestore-function"></a><span data-ttu-id="068fc-103">Funzione JetRestore</span><span class="sxs-lookup"><span data-stu-id="068fc-103">JetRestore Function</span></span>


<span data-ttu-id="068fc-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="068fc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore-function"></a><span data-ttu-id="068fc-105">Funzione JetRestore</span><span class="sxs-lookup"><span data-stu-id="068fc-105">JetRestore Function</span></span>

<span data-ttu-id="068fc-106">La funzione **JetRestore** Ripristina e recupera un backup di flusso di un'istanza, inclusi tutti i database collegati.</span><span class="sxs-lookup"><span data-stu-id="068fc-106">The **JetRestore** function restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="068fc-107">Questa funzione è principalmente per la compatibilità con le versioni precedenti di Windows 2000 e dei motori di database precedenti, in cui è consentita una sola istanza di un database.</span><span class="sxs-lookup"><span data-stu-id="068fc-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="068fc-108">In questo caso, l'istanza attiva è l'istanza di ripristinata.</span><span class="sxs-lookup"><span data-stu-id="068fc-108">In this case, the active instance is the instance that is restored.</span></span> <span data-ttu-id="068fc-109">Con **JetRestore**, non è possibile specificare il percorso per i database ripristinati.</span><span class="sxs-lookup"><span data-stu-id="068fc-109">With **JetRestore**, the location for the restored databases cannot be specified.</span></span>

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="068fc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="068fc-110">Parameters</span></span>

<span data-ttu-id="068fc-111">*SZ*</span><span class="sxs-lookup"><span data-stu-id="068fc-111">*sz*</span></span>

<span data-ttu-id="068fc-112">Cartella in cui si trova il backup.</span><span class="sxs-lookup"><span data-stu-id="068fc-112">The folder where the backup is located.</span></span> <span data-ttu-id="068fc-113">Il backup dovrebbe essere stato generato tramite la funzione [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="068fc-113">The backup should have been generated using the [JetBackup](./jetbackup-function.md) function.</span></span>

<span data-ttu-id="068fc-114">*PFN*</span><span class="sxs-lookup"><span data-stu-id="068fc-114">*pfn*</span></span>

<span data-ttu-id="068fc-115">Puntatore facoltativo alla funzione che verrà chiamato come informazioni di notifica sullo stato di avanzamento dell'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="068fc-115">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="068fc-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="068fc-116">Return Value</span></span>

<span data-ttu-id="068fc-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="068fc-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="068fc-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="068fc-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="068fc-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="068fc-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="068fc-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="068fc-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="068fc-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="068fc-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="068fc-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="068fc-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fc-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="068fc-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="068fc-124">L'operazione non è riuscita perché il motore è già inizializzato per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="068fc-124">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fc-125">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="068fc-125">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="068fc-126">Il set di file di log dal set di backup e dal percorso del log corrente non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="068fc-126">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fc-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="068fc-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="068fc-128">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="068fc-128">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fc-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="068fc-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="068fc-130">L'operazione non è riuscita perché alcuni percorsi specificati non sono validi (percorso di backup, percorso di destinazione, log o percorso di sistema per l'istanza).</span><span class="sxs-lookup"><span data-stu-id="068fc-130">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fc-131">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="068fc-131">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="068fc-132">L'operazione non è riuscita perché il motore è configurato per l'utilizzo di una dimensione di pagina del database (utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> per <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) che non corrisponde alle dimensioni della pagina del database utilizzate per creare i file di log delle transazioni o i database associati ai file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-132">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fc-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="068fc-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="068fc-134">L'operazione non è riuscita perché i parametri implicavano la modalità a istanza singola (modalità di compatibilità di Windows 2000) e il motore è già in modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="068fc-134">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="068fc-135">In seguito all'esito positivo, i file di database del set di backup verranno ripristinati nel percorso e verrà eseguito il ripristino in modo che i database si trovino in uno stato di coerenza transazionale pulito.</span><span class="sxs-lookup"><span data-stu-id="068fc-135">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="068fc-136">Il ripristino rieseguirà i file di log dal set di backup e i file di log del percorso del log se tali file esistono.</span><span class="sxs-lookup"><span data-stu-id="068fc-136">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="068fc-137">Con questo ripristino verranno apportate modifiche al file del checkpoint, ai file di log delle transazioni e a tutti i database a cui fanno riferimento tali file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-137">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="068fc-138">In caso di errore, l'istanza rimane in uno stato non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="068fc-138">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="068fc-139">È probabile che lo stato dei file di log delle transazioni e di eventuali database a cui fanno riferimento tali file di log delle transazioni sia stato modificato nel tentativo di inizializzare il ripristino e ripristinare i database.</span><span class="sxs-lookup"><span data-stu-id="068fc-139">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="068fc-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="068fc-140">Remarks</span></span>

<span data-ttu-id="068fc-141">Il processo di ripristino ricostruirà i database collegati all'istanza durante il backup e salverà le modifiche nei file di database.</span><span class="sxs-lookup"><span data-stu-id="068fc-141">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="068fc-142">Il risultato sarà costituito da database coerenti con le transazioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-142">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="068fc-143">Se possibile, verrà salvata anche nel database le modifiche apportate dal momento in cui è stato eseguito il backup fino a quando non viene rilevata la modifica più recente nei log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-143">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="068fc-144">Questo potrebbe essere possibile se i log delle transazioni generati dopo l'esecuzione del backup sono ancora presenti nella directory dei log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-144">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="068fc-145">Si noti che se per l'istanza è stata abilitata la registrazione circolare, i log delle transazioni generati vengono riutilizzati in modo tale che il ripristino possa salvare le modifiche apportate fino al momento del backup.</span><span class="sxs-lookup"><span data-stu-id="068fc-145">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="068fc-146">In ogni caso, il processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre sui database è di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-146">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="068fc-147">È necessario chiamare le funzioni **JetRestore** su un'istanza prima di chiamare [JetInit](./jetinit-function.md) per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="068fc-147">**JetRestore** functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="068fc-148">Poiché durante il ripristino viene utilizzato un numero significativo di pagine di database e di log delle transazioni, è presente un'intera serie di errori che potrebbero essere restituiti da queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-148">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="068fc-149">Questi errori possono essere causati da errori di allocazione delle risorse temporanei come Jet_errOutOfMemory a errori che rappresentano danneggiamenti fisici come JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="068fc-149">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="068fc-150">Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati.</span><span class="sxs-lookup"><span data-stu-id="068fc-150">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="068fc-151">La gestione non automatica dei file si manifesterà più spesso come JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="068fc-151">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="068fc-152">Questi errori possono essere evitati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="068fc-152">These errors are preventable by the application.</span></span> <span data-ttu-id="068fc-153">L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="068fc-153">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="068fc-154">Se l'applicazione desidera eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="068fc-154">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="068fc-155">Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="068fc-155">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="068fc-156">Per i diversi passaggi del ripristino vengono generate voci del registro eventi, tra cui lo stato di riproduzione del log delle transazioni e il risultato finale del ripristino.</span><span class="sxs-lookup"><span data-stu-id="068fc-156">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="068fc-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="068fc-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="068fc-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="068fc-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="068fc-159">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="068fc-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fc-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="068fc-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="068fc-161">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="068fc-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fc-162"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="068fc-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="068fc-163">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="068fc-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fc-164"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="068fc-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="068fc-165">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="068fc-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fc-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="068fc-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="068fc-167">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="068fc-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fc-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="068fc-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="068fc-169">Implementato come <strong>JetRestoreW</strong> (Unicode) e <strong>JetRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="068fc-169">Implemented as <strong>JetRestoreW</strong> (Unicode) and <strong>JetRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="068fc-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="068fc-170">See Also</span></span>

[<span data-ttu-id="068fc-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="068fc-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="068fc-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="068fc-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="068fc-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="068fc-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="068fc-174">JetBackup</span><span class="sxs-lookup"><span data-stu-id="068fc-174">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="068fc-175">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="068fc-175">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="068fc-176">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="068fc-176">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="068fc-177">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="068fc-177">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
