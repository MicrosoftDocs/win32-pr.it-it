---
description: 'Altre informazioni su: funzione JetExternalRestore2'
title: Funzione JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967949"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="407f2-103">Funzione JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="407f2-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="407f2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="407f2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="407f2-105">Funzione JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="407f2-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="407f2-106">La funzione **JetExternalRestore2** ripristina un backup esterno che è stato usato con le API di backup esterne e fornisce checkpoint da usare per le operazioni di registrazione circolari.</span><span class="sxs-lookup"><span data-stu-id="407f2-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="407f2-107">Questa operazione è nota come ripristino a livello di hardware, che è simile ma differente rispetto al ripristino soft eseguito dalla funzione [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="407f2-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="407f2-108">**Windows XP: JetExternalRestore2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="407f2-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="407f2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="407f2-109">Parameters</span></span>

<span data-ttu-id="407f2-110">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="407f2-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="407f2-111">Percorso del file del checkpoint da utilizzare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o se il percorso dispone di un'istanza attiva o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="407f2-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="407f2-112">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="407f2-112">*szLogPath*</span></span>

<span data-ttu-id="407f2-113">Percorso o directory dei log per la fase finale (annullamento) del ripristino ed eventualmente per i log di rollforward.</span><span class="sxs-lookup"><span data-stu-id="407f2-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="407f2-114">Questo percorso può essere uguale a quello di *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="407f2-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="407f2-115">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="407f2-115">*rgrstmap*</span></span>

<span data-ttu-id="407f2-116">Si tratta di una matrice di strutture di [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="407f2-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="407f2-117">Si tratta di una mappa di percorsi di database vecchi e nuovi o di nomi file.</span><span class="sxs-lookup"><span data-stu-id="407f2-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="407f2-118">Questa operazione viene utilizzata perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="407f2-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="407f2-119">Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset dei database da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="407f2-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="407f2-120">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="407f2-120">*crstfilemap*</span></span>

<span data-ttu-id="407f2-121">Numero di voci nel parametro della matrice *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="407f2-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="407f2-122">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="407f2-122">*szBackupLogPath*</span></span>

<span data-ttu-id="407f2-123">Percorso della directory in cui vengono ripristinati i file di log.</span><span class="sxs-lookup"><span data-stu-id="407f2-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="407f2-124">Si tratta dei log che sono stati letti durante la sequenza di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="407f2-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="407f2-125">Questo percorso può essere uguale a quello di *szLogPath*.</span><span class="sxs-lookup"><span data-stu-id="407f2-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="407f2-126">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="407f2-126">*pLogInfo*</span></span>

<span data-ttu-id="407f2-127">*PLogInfo* descrive diversi aspetti dei log di backup da ripristinare. questo parametro consente a **JetExternalRestore2** di prendere i parametri *genLow* e *genHigh* espliciti che **JetExternalRestore2** possiede, nonché il nome del log di base, anziché un presunto nome di base del log "edb".</span><span class="sxs-lookup"><span data-stu-id="407f2-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="407f2-128">*szTargetInstanceName*</span><span class="sxs-lookup"><span data-stu-id="407f2-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="407f2-129">Questo parametro è deprecato e non può essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="407f2-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="407f2-130">*szTargetInstanceLogPath*</span><span class="sxs-lookup"><span data-stu-id="407f2-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="407f2-131">Percorso per i log di rollforward se il percorso dei log di cui si desidera eseguire il rollforward si trova in un set di registrazioni attivo o in un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="407f2-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="407f2-132">Questa operazione non deve essere specificata se l'istanza di destinazione usa la registrazione circolare.</span><span class="sxs-lookup"><span data-stu-id="407f2-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="407f2-133">*szTargetInstanceCheckpointPath*</span><span class="sxs-lookup"><span data-stu-id="407f2-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="407f2-134">Percorso del checkpoint durante il ripristino se non è presente alcuna istanza attiva in esecuzione in questa destinazione.</span><span class="sxs-lookup"><span data-stu-id="407f2-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="407f2-135">Questa operazione non deve essere specificata se l'istanza di destinazione usa la registrazione circolare.</span><span class="sxs-lookup"><span data-stu-id="407f2-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="407f2-136">*PFN*</span><span class="sxs-lookup"><span data-stu-id="407f2-136">*pfn*</span></span>

<span data-ttu-id="407f2-137">Callback di stato che segnala lo stato di avanzamento del ripristino.</span><span class="sxs-lookup"><span data-stu-id="407f2-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="407f2-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="407f2-138">Return Value</span></span>

<span data-ttu-id="407f2-139">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="407f2-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="407f2-140">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="407f2-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="407f2-141">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="407f2-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="407f2-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="407f2-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="407f2-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="407f2-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="407f2-144">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="407f2-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="407f2-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="407f2-146">Il <em>szTargetInstanceLogPath</em> specificato non appartiene a un'istanza inizializzata.</span><span class="sxs-lookup"><span data-stu-id="407f2-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="407f2-147">Questo errore verrà restituito solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="407f2-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="407f2-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="407f2-149">Indica che il database è danneggiato o un file non riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="407f2-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="407f2-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="407f2-151">Questo errore viene restituito se uno per i file di log in <em>szBackupLogPath</em>ha una generazione di log precedente a quella specificata in <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="407f2-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="407f2-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="407f2-153">L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="407f2-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="407f2-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="407f2-155">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="407f2-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="407f2-156">Questo problema può verificarsi per <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non sono entrambi specificati.</span><span class="sxs-lookup"><span data-stu-id="407f2-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="407f2-157">Ovvero devono corrispondere ed essere specificati o entrambi non specificati.</span><span class="sxs-lookup"><span data-stu-id="407f2-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="407f2-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="407f2-159">L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="407f2-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="407f2-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="407f2-161">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="407f2-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="407f2-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="407f2-163">Questo errore viene restituito se il file di database specificato durante l'operazione di ripristino non è un database di cui è stato eseguito il backup con backup esterno.</span><span class="sxs-lookup"><span data-stu-id="407f2-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="407f2-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="407f2-165">Il motore di database non è in grado di eseguire il ripristino esterno o il ripristino a freddo in modalità istanza singola.</span><span class="sxs-lookup"><span data-stu-id="407f2-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="407f2-166">Questo errore verrà restituito solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="407f2-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="407f2-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="407f2-168">Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="407f2-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="407f2-169">In seguito all'esito positivo, tutti i database del *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente.</span><span class="sxs-lookup"><span data-stu-id="407f2-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="407f2-170">A questo punto è possibile rimontare il database in un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="407f2-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="407f2-171">In caso di errore, il motore non è riuscito a recuperare il database.</span><span class="sxs-lookup"><span data-stu-id="407f2-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="407f2-172">Il database è in uno stato non valido e, per ritentare il ripristino, è necessario ripristinare nuovamente l'intero database.</span><span class="sxs-lookup"><span data-stu-id="407f2-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="407f2-173">In genere, l'origine di tale situazione è il danneggiamento del disco o del log, o un altro tipo di errore di gestione dei log oppure un set di log non continuo.</span><span class="sxs-lookup"><span data-stu-id="407f2-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="407f2-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="407f2-174">Remarks</span></span>

<span data-ttu-id="407f2-175">Vedere [JetExternalRestore](./jetexternalrestore-function.md).</span><span class="sxs-lookup"><span data-stu-id="407f2-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="407f2-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="407f2-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="407f2-177"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="407f2-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="407f2-178">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="407f2-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-179"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="407f2-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="407f2-180">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="407f2-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-181"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="407f2-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="407f2-182">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="407f2-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-183"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="407f2-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="407f2-184">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="407f2-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="407f2-185"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="407f2-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="407f2-186">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="407f2-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="407f2-187"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="407f2-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="407f2-188">Implementato come <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="407f2-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="407f2-189">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="407f2-189">See Also</span></span>

[<span data-ttu-id="407f2-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="407f2-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="407f2-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="407f2-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="407f2-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="407f2-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="407f2-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="407f2-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="407f2-194">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="407f2-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="407f2-195">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="407f2-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="407f2-196">JetInit</span><span class="sxs-lookup"><span data-stu-id="407f2-196">JetInit</span></span>](./jetinit-function.md)
