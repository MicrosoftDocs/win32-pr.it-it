---
description: 'Altre informazioni su: funzione JetExternalRestore'
title: JetExternalRestore (funzione)
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323807"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="15174-103">JetExternalRestore (funzione)</span><span class="sxs-lookup"><span data-stu-id="15174-103">JetExternalRestore Function</span></span>


<span data-ttu-id="15174-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="15174-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="15174-105">JetExternalRestore (funzione)</span><span class="sxs-lookup"><span data-stu-id="15174-105">JetExternalRestore Function</span></span>

<span data-ttu-id="15174-106">La funzione **JetExternalRestore** ripristina un backup esterno che è stato eseguito con le API di backup esterne e specifica un intervallo di numeri di file di log da riprodurre durante il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="15174-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="15174-107">Questa operazione è nota come ripristino a livello di hardware, che è simile a, ma diverso dal ripristino soft come eseguito dalla funzione [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="15174-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="15174-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15174-108">Parameters</span></span>

<span data-ttu-id="15174-109">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="15174-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="15174-110">Percorso del file del checkpoint da utilizzare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o è già presente un'istanza attiva o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="15174-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="15174-111">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="15174-111">*szLogPath*</span></span>

<span data-ttu-id="15174-112">Percorso o directory dei log per la fase finale (annullamento) del ripristino ed eventualmente per i log di rollforward.</span><span class="sxs-lookup"><span data-stu-id="15174-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="15174-113">Questo percorso può essere uguale a quello di *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="15174-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="15174-114">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="15174-114">*rgrstmap*</span></span>

<span data-ttu-id="15174-115">Si tratta di una matrice di strutture di [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="15174-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="15174-116">Si tratta di una mappa di percorsi di database vecchi e nuovi o di nomi file.</span><span class="sxs-lookup"><span data-stu-id="15174-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="15174-117">Questa operazione viene utilizzata perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="15174-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="15174-118">Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset di database da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="15174-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="15174-119">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="15174-119">*crstfilemap*</span></span>

<span data-ttu-id="15174-120">Numero di voci nel parametro della matrice *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="15174-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="15174-121">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="15174-121">*szBackupLogPath*</span></span>

<span data-ttu-id="15174-122">Percorso della directory in cui vengono ripristinati i file di log.</span><span class="sxs-lookup"><span data-stu-id="15174-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="15174-123">Si tratta dei log che sono stati letti durante la sequenza di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="15174-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="15174-124">Questo percorso può essere uguale a quello di szLogPath.</span><span class="sxs-lookup"><span data-stu-id="15174-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="15174-125">*genLow*</span><span class="sxs-lookup"><span data-stu-id="15174-125">*genLow*</span></span>

<span data-ttu-id="15174-126">Numero di file di log più basso che deve essere riprodotto da *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="15174-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="15174-127">È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="15174-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="15174-128">Questo può cambiare nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="15174-128">This may change in future versions.</span></span>

<span data-ttu-id="15174-129">*genHigh*</span><span class="sxs-lookup"><span data-stu-id="15174-129">*genHigh*</span></span>

<span data-ttu-id="15174-130">Numero massimo di file di log che deve essere riprodotto da *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="15174-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="15174-131">È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="15174-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="15174-132">Questo può cambiare nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="15174-132">This may change in future versions.</span></span>

<span data-ttu-id="15174-133">*PFN*</span><span class="sxs-lookup"><span data-stu-id="15174-133">*pfn*</span></span>

<span data-ttu-id="15174-134">Callback di stato per segnalare lo stato di avanzamento del ripristino.</span><span class="sxs-lookup"><span data-stu-id="15174-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="15174-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15174-135">Return Value</span></span>

<span data-ttu-id="15174-136">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="15174-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="15174-137">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="15174-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15174-138">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="15174-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="15174-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15174-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15174-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="15174-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="15174-141">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="15174-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="15174-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="15174-143">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="15174-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="15174-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="15174-145">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="15174-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="15174-146">Questo problema può verificarsi per <strong>JetExternalRestore</strong>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non sono entrambi specificati.</span><span class="sxs-lookup"><span data-stu-id="15174-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="15174-147">Ovvero devono corrispondere ed essere specificati o entrambi non specificati.</span><span class="sxs-lookup"><span data-stu-id="15174-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="15174-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="15174-149">Indica che il database è danneggiato o un file non riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="15174-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="15174-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="15174-151">L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="15174-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="15174-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="15174-153">L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="15174-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="15174-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="15174-155">Questo errore viene restituito se il file di database specificato durante l'operazione di ripristino non è un database di cui è stato eseguito il backup con backup esterno.</span><span class="sxs-lookup"><span data-stu-id="15174-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="15174-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="15174-157">Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="15174-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="15174-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="15174-159">Questo errore viene restituito se uno per i file di log in <em>szBackupLogPath</em>ha una generazione di log precedente a quella specificata in <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="15174-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="15174-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="15174-161">Il <em>szTargetInstanceLogPath</em> specificato non appartiene a un'istanza inizializzata.</span><span class="sxs-lookup"><span data-stu-id="15174-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="15174-162">Questo errore verrà restituito solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="15174-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="15174-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="15174-164">Il motore di database non è in grado di eseguire il ripristino esterno o il ripristino a freddo in modalità istanza singola.</span><span class="sxs-lookup"><span data-stu-id="15174-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="15174-165">Questo errore verrà restituito solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="15174-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="15174-166">In seguito all'esito positivo, tutti i database del *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente.</span><span class="sxs-lookup"><span data-stu-id="15174-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="15174-167">A questo punto è possibile rimontare il database in un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="15174-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="15174-168">In caso di errore, il motore non è riuscito a recuperare il database.</span><span class="sxs-lookup"><span data-stu-id="15174-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="15174-169">Il database è in uno stato non valido e, per ritentare il ripristino, è necessario ripristinare nuovamente l'intero database.</span><span class="sxs-lookup"><span data-stu-id="15174-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="15174-170">In genere, l'origine di tale situazione è il danneggiamento del disco o del log, o un altro tipo di errore di gestione dei log oppure un set di log non continuo.</span><span class="sxs-lookup"><span data-stu-id="15174-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="15174-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="15174-171">Remarks</span></span>

<span data-ttu-id="15174-172">Per comprendere il funzionamento di un ripristino "complesso", è necessario comprendere che esistono tre fasi di ripristino e la seconda fase può avere due parti.</span><span class="sxs-lookup"><span data-stu-id="15174-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="15174-173">Nella fase I, I log sono obbligatori a garantire la coerenza di un database di cui è stato eseguito il backup (oppure è possibile usare un set iniziale di log incrementali).</span><span class="sxs-lookup"><span data-stu-id="15174-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="15174-174">Nella fase II vengono utilizzati tutti i log di rollforward aggiuntivi disponibili per rendere il database coerente.</span><span class="sxs-lookup"><span data-stu-id="15174-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="15174-175">È inoltre disponibile una riproduzione dei log di rollforward aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="15174-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="15174-176">La fase III è la fase di rollback del ripristino.</span><span class="sxs-lookup"><span data-stu-id="15174-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="15174-177">Fase I: viene eseguita la riproduzione del set di log che deve essere ripristinato per portare il database a uno stato coerente (o a un set di file di log iniziale).</span><span class="sxs-lookup"><span data-stu-id="15174-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="15174-178">In sostanza, si tratta della riproduzione del set di file di log non facoltativi per i database da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="15174-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="15174-179">Se sono presenti log mancanti da questo intervallo di log, il ripristino avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="15174-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="15174-180">Questi log devono essere inseriti nella directory specificata nel parametro *szBackupLogPath* .</span><span class="sxs-lookup"><span data-stu-id="15174-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="15174-181">Fase II: facoltativamente, possono essere presenti alcuni set di file di log che eseguono il rollforward dei file di log che provengono da backup incrementali o differenziali e dai file di log di un'istanza attiva.</span><span class="sxs-lookup"><span data-stu-id="15174-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="15174-182">Nel caso di file di log di backup incrementali o differenziali, i file di log possono essere inseriti nelle directory specificate nei parametri *szBackupLogPath* o *szTargetInstanceLogPath* , con il primo che è la directory consigliata.</span><span class="sxs-lookup"><span data-stu-id="15174-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="15174-183">I log usati per la fase di rollforward (fase II) dovrebbero provenire dalla stessa serie di log rilasciati durante la fase I e devono avere incrementato continuamente I numeri di log senza gap dalla fase I log.</span><span class="sxs-lookup"><span data-stu-id="15174-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="15174-184">Per riprodurre un database in modo che sia completamente aggiornato con i file di log attualmente utilizzati da un'istanza attiva, è necessario specificare i parametri *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath* .</span><span class="sxs-lookup"><span data-stu-id="15174-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="15174-185">Questa operazione può essere eseguita anche mentre altri database sono collegati a tale set di log.</span><span class="sxs-lookup"><span data-stu-id="15174-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="15174-186">Fase III: nella fase finale del ripristino, viene eseguito il rollback di tutte le transazioni di cui non è stato eseguito il commit, che richiedono la generazione di nuovi file di log e l'aggiornamento del file del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="15174-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="15174-187">Questa fase viene a volte definita "annullamento".</span><span class="sxs-lookup"><span data-stu-id="15174-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="15174-188">Il percorso del file del checkpoint da usare durante questa fase è il percorso analogo al percorso del log della fase III, ovvero se *szLogPath* viene usato per la fase III, viene usato *szCheckpointFilePath* se viene usato *szTargetInstanceLogPath* per la fase III del ripristino *szTargetInstanceCheckpointPath* .</span><span class="sxs-lookup"><span data-stu-id="15174-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="15174-189">Per comprendere il funzionamento dei percorsi, usare questo diagramma di flusso:</span><span class="sxs-lookup"><span data-stu-id="15174-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="15174-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="15174-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="15174-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15174-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15174-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="15174-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="15174-193">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="15174-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="15174-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="15174-195">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="15174-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-196"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="15174-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="15174-197">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="15174-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-198"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="15174-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="15174-199">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="15174-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15174-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="15174-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="15174-201">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="15174-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15174-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="15174-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="15174-203">Implementato come <strong>JetExternalRestoreW</strong> (Unicode) e <strong>JetExternalRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="15174-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="15174-204">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="15174-204">See Also</span></span>

[<span data-ttu-id="15174-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="15174-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="15174-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="15174-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="15174-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="15174-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="15174-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="15174-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="15174-209">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="15174-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="15174-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="15174-210">JetInit</span></span>](./jetinit-function.md)
