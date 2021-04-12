---
description: 'Altre informazioni su: funzione JetRestoreInstance'
title: Funzione JetRestoreInstance
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233634"
---
# <a name="jetrestoreinstance-function"></a><span data-ttu-id="32901-103">Funzione JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="32901-103">JetRestoreInstance Function</span></span>


<span data-ttu-id="32901-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="32901-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestoreinstance-function"></a><span data-ttu-id="32901-105">Funzione JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="32901-105">JetRestoreInstance Function</span></span>

<span data-ttu-id="32901-106">La funzione **JetRestoreInstance** Ripristina e recupera un backup di flusso di un'istanza di, inclusi tutti i database collegati.</span><span class="sxs-lookup"><span data-stu-id="32901-106">The **JetRestoreInstance** function restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="32901-107">È progettato per funzionare con un backup creato con la funzione [JetBackupInstance](./jetbackupinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="32901-107">It is designed to work with a backup created with the [JetBackupInstance](./jetbackupinstance-function.md) function.</span></span> <span data-ttu-id="32901-108">Si tratta della funzione di ripristino più semplice e incapsulata.</span><span class="sxs-lookup"><span data-stu-id="32901-108">This is the simplest and most encapsulated one restore function.</span></span>

<span data-ttu-id="32901-109">**Windows XP:**  **JetRestoreInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32901-109">**Windows XP:**  **JetRestoreInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="32901-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="32901-110">Parameters</span></span>

<span data-ttu-id="32901-111">*istanza*</span><span class="sxs-lookup"><span data-stu-id="32901-111">*instance*</span></span>

<span data-ttu-id="32901-112">Specifica l'istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="32901-112">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="32901-113">Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore.</span><span class="sxs-lookup"><span data-stu-id="32901-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="32901-114">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL o può essere impostato su un buffer di output valido contenente NULL o JET_instanceNil che restituirà l'handle dell'istanza globale creato come effetto collaterale dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="32901-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="32901-115">Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="32901-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="32901-116">Se il motore funziona in modalità a istanze diverse, questo parametro deve essere impostato su un buffer di input valido che contiene l'handle dell'istanza restituito da [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="32901-116">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="32901-117">*SZ*</span><span class="sxs-lookup"><span data-stu-id="32901-117">*sz*</span></span>

<span data-ttu-id="32901-118">Cartella in cui si trova il backup.</span><span class="sxs-lookup"><span data-stu-id="32901-118">The folder where the backup is located.</span></span> <span data-ttu-id="32901-119">Il backup dovrebbe essere stato generato usando le API [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="32901-119">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="32901-120">*szDest*</span><span class="sxs-lookup"><span data-stu-id="32901-120">*szDest*</span></span>

<span data-ttu-id="32901-121">Nome della cartella in cui verranno copiati e ripristinati i file di database del set di backup.</span><span class="sxs-lookup"><span data-stu-id="32901-121">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="32901-122">Se questo valore è impostato su NULL (come nel caso della [JetRestore](./jetrestore-function.md)legacy), i file di database verranno copiati e ripristinati nel percorso originale.</span><span class="sxs-lookup"><span data-stu-id="32901-122">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="32901-123">*PFN*</span><span class="sxs-lookup"><span data-stu-id="32901-123">*pfn*</span></span>

<span data-ttu-id="32901-124">Puntatore facoltativo alla funzione che verrà chiamato come informazioni di notifica sullo stato di avanzamento dell'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="32901-124">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="32901-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32901-125">Return Value</span></span>

<span data-ttu-id="32901-126">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="32901-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="32901-127">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="32901-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32901-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="32901-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="32901-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32901-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32901-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="32901-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="32901-131">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="32901-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32901-132">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="32901-132">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="32901-133">L'operazione non è riuscita perché il motore è già inizializzato per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="32901-133">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32901-134">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="32901-134">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="32901-135">Il set di file di log dal set di backup e dal percorso del log corrente non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="32901-135">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32901-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="32901-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="32901-137">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="32901-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="32901-138">Questo errore viene restituito da <strong>JetRestoreInstance</strong> quando il motore è in modalità a istanze diverse e pinstance si riferisce a un'istanza non valida di Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="32901-138">This error will be returned by <strong>JetRestoreInstance</strong> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32901-139">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="32901-139">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="32901-140">L'operazione non è riuscita perché alcuni percorsi specificati non sono validi (percorso di backup, percorso di destinazione, log o percorso di sistema per l'istanza).</span><span class="sxs-lookup"><span data-stu-id="32901-140">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32901-141">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="32901-141">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="32901-142">L'operazione non è riuscita perché il motore è configurato per l'utilizzo di una dimensione di pagina del database (utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> per <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) che non corrisponde alle dimensioni della pagina del database utilizzate per creare i file di log delle transazioni o i database associati ai file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="32901-142">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32901-143">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="32901-143">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="32901-144">L'operazione non è riuscita perché i parametri implicavano la modalità a istanza singola (modalità di compatibilità di Windows 2000) e il motore è già in modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="32901-144">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32901-145">In seguito all'esito positivo, i file di database del set di backup verranno ripristinati nel percorso e verrà eseguito il ripristino in modo che i database si trovino in uno stato di coerenza transazionale pulito.</span><span class="sxs-lookup"><span data-stu-id="32901-145">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="32901-146">Il ripristino rieseguirà i file di log dal set di backup e i file di log del percorso del log se tali file esistono.</span><span class="sxs-lookup"><span data-stu-id="32901-146">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="32901-147">Con questo ripristino verranno apportate modifiche al file del checkpoint, ai file di log delle transazioni e a tutti i database a cui fanno riferimento tali file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="32901-147">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="32901-148">In caso di errore, l'istanza rimane in uno stato non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="32901-148">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="32901-149">È probabile che lo stato dei file di log delle transazioni e di eventuali database a cui fanno riferimento tali file di log delle transazioni sia stato modificato nel tentativo di inizializzare il ripristino e ripristinare i database.</span><span class="sxs-lookup"><span data-stu-id="32901-149">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="32901-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="32901-150">Remarks</span></span>

<span data-ttu-id="32901-151">Il processo di ripristino ricostruirà i database collegati all'istanza durante il backup e salverà le modifiche nei file di database.</span><span class="sxs-lookup"><span data-stu-id="32901-151">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="32901-152">Il risultato sarà costituito da database coerenti con le transazioni.</span><span class="sxs-lookup"><span data-stu-id="32901-152">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="32901-153">Se possibile, verrà salvata anche nel database le modifiche apportate dal momento in cui è stato eseguito il backup fino a quando non viene rilevata la modifica più recente nei log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="32901-153">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="32901-154">Questo potrebbe essere possibile se i log delle transazioni generati dopo l'esecuzione del backup sono ancora presenti nella directory dei log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="32901-154">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="32901-155">Si noti che se per l'istanza è stata abilitata la registrazione circolare, i log delle transazioni generati vengono riutilizzati in modo tale che il ripristino possa salvare le modifiche apportate fino al momento del backup.</span><span class="sxs-lookup"><span data-stu-id="32901-155">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="32901-156">In ogni caso, il processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre sui database è di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="32901-156">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="32901-157">**JetRestoreInstance** deve essere chiamato su un'istanza che è già stata creata utilizzando [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="32901-157">**JetRestoreInstance** must be called on an instance which was already created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="32901-158">Poiché durante il ripristino viene utilizzato un numero significativo di pagine di database e di log delle transazioni, è presente un'intera serie di errori che potrebbero essere restituiti da queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="32901-158">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="32901-159">Questi errori possono essere causati da errori di allocazione delle risorse temporanei come Jet_errOutOfMemory a errori che rappresentano danneggiamenti fisici come JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="32901-159">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="32901-160">Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati.</span><span class="sxs-lookup"><span data-stu-id="32901-160">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="32901-161">La gestione non automatica dei file si manifesterà più spesso come JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="32901-161">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="32901-162">Questi errori possono essere evitati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32901-162">These errors are preventable by the application.</span></span> <span data-ttu-id="32901-163">L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="32901-163">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="32901-164">Se l'applicazione desidera eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="32901-164">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="32901-165">Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="32901-165">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="32901-166">Per i diversi passaggi del ripristino vengono generate voci del registro eventi, tra cui lo stato di riproduzione del log delle transazioni e il risultato finale del ripristino.</span><span class="sxs-lookup"><span data-stu-id="32901-166">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="32901-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32901-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32901-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="32901-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="32901-169">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32901-169">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32901-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="32901-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="32901-171">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="32901-171">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32901-172"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="32901-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="32901-173">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="32901-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32901-174"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="32901-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="32901-175">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="32901-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32901-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="32901-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="32901-177">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="32901-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32901-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="32901-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="32901-179">Implementato come <strong>JetRestoreInstanceW</strong> (Unicode) e <strong>JetRestoreInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="32901-179">Implemented as <strong>JetRestoreInstanceW</strong> (Unicode) and <strong>JetRestoreInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="32901-180">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="32901-180">See Also</span></span>

[<span data-ttu-id="32901-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="32901-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="32901-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="32901-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="32901-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="32901-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="32901-184">JetBackup</span><span class="sxs-lookup"><span data-stu-id="32901-184">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="32901-185">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="32901-185">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="32901-186">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="32901-186">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="32901-187">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="32901-187">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
