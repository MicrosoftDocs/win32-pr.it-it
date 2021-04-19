---
description: 'Altre informazioni su: funzione JetRestore2'
title: Funzione JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318085"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="803b0-103">Funzione JetRestore2</span><span class="sxs-lookup"><span data-stu-id="803b0-103">JetRestore2 Function</span></span>


<span data-ttu-id="803b0-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="803b0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="803b0-105">Funzione JetRestore2</span><span class="sxs-lookup"><span data-stu-id="803b0-105">JetRestore2 Function</span></span>

<span data-ttu-id="803b0-106">Il **JetRestore2** Ripristina e recupera un backup di flusso di un'istanza, inclusi tutti i database collegati.</span><span class="sxs-lookup"><span data-stu-id="803b0-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="803b0-107">Questa funzione è principalmente per la compatibilità con le versioni precedenti di Windows 2000 e dei motori di database precedenti, in cui è consentita una sola istanza di un database.</span><span class="sxs-lookup"><span data-stu-id="803b0-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="803b0-108">In questo caso, l'istanza attiva è l'istanza di ripristinata.</span><span class="sxs-lookup"><span data-stu-id="803b0-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="803b0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="803b0-109">Parameters</span></span>

<span data-ttu-id="803b0-110">*SZ*</span><span class="sxs-lookup"><span data-stu-id="803b0-110">*sz*</span></span>

<span data-ttu-id="803b0-111">Cartella in cui si trova il backup.</span><span class="sxs-lookup"><span data-stu-id="803b0-111">The folder where the backup is located.</span></span> <span data-ttu-id="803b0-112">Il backup dovrebbe essere stato generato usando le API [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="803b0-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="803b0-113">*szDest*</span><span class="sxs-lookup"><span data-stu-id="803b0-113">*szDest*</span></span>

<span data-ttu-id="803b0-114">Nome della cartella in cui verranno copiati e ripristinati i file di database del set di backup.</span><span class="sxs-lookup"><span data-stu-id="803b0-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="803b0-115">Se questo valore è impostato su NULL (come nel caso della [JetRestore](./jetrestore-function.md)legacy), i file di database verranno copiati e ripristinati nel percorso originale.</span><span class="sxs-lookup"><span data-stu-id="803b0-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="803b0-116">*PFN*</span><span class="sxs-lookup"><span data-stu-id="803b0-116">*pfn*</span></span>

<span data-ttu-id="803b0-117">Puntatore facoltativo alla funzione che verrà chiamato come informazioni di notifica sullo stato di avanzamento dell'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="803b0-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="803b0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="803b0-118">Return Value</span></span>

<span data-ttu-id="803b0-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="803b0-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="803b0-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="803b0-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="803b0-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="803b0-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="803b0-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="803b0-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="803b0-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="803b0-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="803b0-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="803b0-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803b0-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="803b0-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="803b0-126">L'operazione non è riuscita perché il motore è già inizializzato per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="803b0-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803b0-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="803b0-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="803b0-128">Il set di file di log dal set di backup e dal percorso del log corrente non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="803b0-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803b0-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="803b0-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="803b0-130">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="803b0-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="803b0-131">Questo errore viene restituito da <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> quando il motore è in modalità a istanze diverse e pinstance si riferisce a un'istanza non valida di Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="803b0-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803b0-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="803b0-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="803b0-133">L'operazione non è riuscita perché alcuni percorsi specificati non sono validi (percorso di backup, percorso di destinazione, log o percorso di sistema per l'istanza).</span><span class="sxs-lookup"><span data-stu-id="803b0-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803b0-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="803b0-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="803b0-135">L'operazione non è riuscita perché il motore è configurato per l'utilizzo di una dimensione di pagina del database (utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> per <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) che non corrisponde alle dimensioni della pagina del database utilizzate per creare i file di log delle transazioni o i database associati ai file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803b0-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="803b0-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="803b0-137">L'operazione non è riuscita perché i parametri implicavano la modalità a istanza singola (modalità di compatibilità di Windows 2000) e il motore è già in modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="803b0-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="803b0-138">In seguito all'esito positivo, i file di database del set di backup verranno ripristinati nel percorso e verrà eseguito il ripristino in modo che i database si trovino in uno stato di coerenza transazionale pulito.</span><span class="sxs-lookup"><span data-stu-id="803b0-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="803b0-139">Il ripristino rieseguirà i file di log dal set di backup e i file di log del percorso del log se tali file esistono.</span><span class="sxs-lookup"><span data-stu-id="803b0-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="803b0-140">Con questo ripristino verranno apportate modifiche al file del checkpoint, ai file di log delle transazioni e a tutti i database a cui fanno riferimento tali file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="803b0-141">In caso di errore, l'istanza rimane in uno stato non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="803b0-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="803b0-142">È probabile che lo stato dei file di log delle transazioni e di eventuali database a cui fanno riferimento tali file di log delle transazioni sia stato modificato nel tentativo di inizializzare il ripristino e ripristinare i database.</span><span class="sxs-lookup"><span data-stu-id="803b0-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="803b0-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="803b0-143">Remarks</span></span>

<span data-ttu-id="803b0-144">Il processo di ripristino ricostruirà i database collegati all'istanza durante il backup e salverà le modifiche nei file di database.</span><span class="sxs-lookup"><span data-stu-id="803b0-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="803b0-145">Il risultato sarà costituito da database coerenti con le transazioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="803b0-146">Se possibile, verrà salvata anche nel database le modifiche apportate dal momento in cui è stato eseguito il backup fino a quando non viene rilevata la modifica più recente nei log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="803b0-147">Questo potrebbe essere possibile se i log delle transazioni generati dopo l'esecuzione del backup sono ancora presenti nella directory dei log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="803b0-148">Si noti che se per l'istanza è stata abilitata la registrazione circolare, i log delle transazioni generati vengono riutilizzati in modo tale che il ripristino possa salvare le modifiche apportate fino al momento del backup.</span><span class="sxs-lookup"><span data-stu-id="803b0-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="803b0-149">In ogni caso, il processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre sui database è di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="803b0-150">È necessario chiamare le funzioni [JetRestore](./jetrestore-function.md) su un'istanza prima di chiamare [JetInit](./jetinit-function.md) per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="803b0-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="803b0-151">Poiché durante il ripristino viene utilizzato un numero significativo di pagine di database e di log delle transazioni, è presente un'intera serie di errori che potrebbero essere restituiti da queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="803b0-152">Questi errori possono essere causati da errori di allocazione delle risorse temporanei come Jet_errOutOfMemory a errori che rappresentano danneggiamenti fisici come JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="803b0-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="803b0-153">Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati.</span><span class="sxs-lookup"><span data-stu-id="803b0-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="803b0-154">La gestione non automatica dei file si manifesterà più spesso come JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="803b0-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="803b0-155">Questi errori possono essere evitati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="803b0-155">These errors are preventable by the application.</span></span> <span data-ttu-id="803b0-156">L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="803b0-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="803b0-157">Se l'applicazione desidera eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="803b0-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="803b0-158">Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="803b0-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="803b0-159">Per i diversi passaggi del ripristino vengono generate voci del registro eventi, tra cui lo stato di riproduzione del log delle transazioni e il risultato finale del ripristino.</span><span class="sxs-lookup"><span data-stu-id="803b0-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="803b0-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="803b0-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="803b0-161"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="803b0-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="803b0-162">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="803b0-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803b0-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="803b0-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="803b0-164">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="803b0-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803b0-165"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="803b0-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="803b0-166">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="803b0-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803b0-167"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="803b0-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="803b0-168">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="803b0-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="803b0-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="803b0-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="803b0-170">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="803b0-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="803b0-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="803b0-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="803b0-172">Implementato come <strong>JetRestore2W</strong> (Unicode) e <strong>JetRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="803b0-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="803b0-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="803b0-173">See Also</span></span>

[<span data-ttu-id="803b0-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="803b0-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="803b0-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="803b0-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="803b0-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="803b0-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="803b0-177">JetBackup</span><span class="sxs-lookup"><span data-stu-id="803b0-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="803b0-178">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="803b0-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="803b0-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="803b0-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="803b0-180">JetInit</span><span class="sxs-lookup"><span data-stu-id="803b0-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="803b0-181">JetRestore</span><span class="sxs-lookup"><span data-stu-id="803b0-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="803b0-182">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="803b0-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="803b0-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="803b0-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
