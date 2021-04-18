---
description: 'Altre informazioni su: funzione JetBackup'
title: Funzione JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319187"
---
# <a name="jetbackup-function"></a><span data-ttu-id="2a8ef-103">Funzione JetBackup</span><span class="sxs-lookup"><span data-stu-id="2a8ef-103">JetBackup Function</span></span>


<span data-ttu-id="2a8ef-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2a8ef-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="2a8ef-105">Funzione JetBackup</span><span class="sxs-lookup"><span data-stu-id="2a8ef-105">JetBackup Function</span></span>

<span data-ttu-id="2a8ef-106">La funzione **JetBackup** crea un backup del database mentre il database è online.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="2a8ef-107">Questa funzione è principalmente per la compatibilità con le versioni precedenti di Windows 2000 e dei motori di database precedenti, in cui è consentita una sola istanza di un database.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="2a8ef-108">In questo caso, l'istanza attiva è l'istanza di di cui viene eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="2a8ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a8ef-109">Parameters</span></span>

<span data-ttu-id="2a8ef-110">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="2a8ef-110">*szBackupPath*</span></span>

<span data-ttu-id="2a8ef-111">Directory in cui è archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-111">The directory where the backup is stored.</span></span> <span data-ttu-id="2a8ef-112">Se il percorso di backup è NULL, la funzione tronca i log, se possibile.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="2a8ef-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2a8ef-113">*grbit*</span></span>

<span data-ttu-id="2a8ef-114">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a8ef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2a8ef-115">Value</span></span></p></th>
<th><p><span data-ttu-id="2a8ef-116">Significato</span><span class="sxs-lookup"><span data-stu-id="2a8ef-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="2a8ef-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-118">Crea un backup completo del database.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-118">Creates a full backup of the database.</span></span> <span data-ttu-id="2a8ef-119">In questo modo è possibile mantenere un backup esistente nella stessa directory se il nuovo backup non riesce.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="2a8ef-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-121">Crea un backup incrementale anziché un backup completo.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="2a8ef-122">Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a8ef-123">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="2a8ef-123">*pfnStatus*</span></span>

<span data-ttu-id="2a8ef-124">Puntatore alla funzione di callback [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , che fornisce informazioni di notifica sullo stato di avanzamento dell'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="2a8ef-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a8ef-125">Return Value</span></span>

<span data-ttu-id="2a8ef-126">La funzione restituisce uno dei codici di errore [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="2a8ef-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="2a8ef-127">Di seguito sono riportati i più comunemente restituiti.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-127">The following are the most commonly returned.</span></span> <span data-ttu-id="2a8ef-128">Per un elenco completo degli errori per questa API, vedere [codici di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2a8ef-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a8ef-129">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2a8ef-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="2a8ef-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a8ef-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2a8ef-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-132">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="2a8ef-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-134">È già in corso un backup per la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="2a8ef-135">Non sono consentiti più backup contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="2a8ef-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-137">L'istanza non è ancora pronta per il backup mentre è in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2a8ef-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-139">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2a8ef-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-141">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="2a8ef-142"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="2a8ef-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-144">Un backup incrementale non è consentito se la registrazione circolare è attiva.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="2a8ef-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-146">Le opzioni specificate non sono valide.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2a8ef-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-148">Un parametro non valido è stato passato nell'API.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="2a8ef-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-150">Il percorso di destinazione non esiste.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="2a8ef-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-152">L'istanza è in esecuzione senza registrazione.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-152">The instance is running without logging.</span></span> <span data-ttu-id="2a8ef-153">Nessun backup consentito.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="2a8ef-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-155">Si è verificato un errore di verifica del checksum in un file di log.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="2a8ef-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-157">La registrazione per l'istanza è temporanea o è disabilitata definitivamente a causa di un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2a8ef-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-159">Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="2a8ef-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-161">Si è verificato un errore di verifica del checksum in una pagina del database.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2a8ef-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-163">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="2a8ef-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-165">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="2a8ef-166"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2a8ef-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a8ef-168">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a8ef-169">Se la funzione ha esito positivo, tutti i file necessari per un ripristino fino al momento del backup saranno contenuti nella directory di backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="2a8ef-170">Se si tratta di un backup completo, i file saranno i file di database e i file di log necessari per portare il database in uno stato coerente.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="2a8ef-171">Se si tratta di un backup incrementale, verranno aggiunti solo i file di log alle directory, ma i file già esistenti (database e file di log), insieme ai nuovi file di log, potranno essere ripristinati per riportare il database allo stato in cui si trovava nel momento in cui è iniziato il backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="2a8ef-172">Come effetto collaterale del backup, i file di log che non sono più necessari verranno troncati.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="2a8ef-173">Allo stesso tempo, le intestazioni del database verranno aggiornate con le informazioni relative al momento in cui è avvenuto l'ultimo backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="2a8ef-174">Se la funzione ha esito negativo, non saranno presenti file nella destinazione della directory di backup, quindi non sarà possibile eseguire alcun ripristino.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="2a8ef-175">Nello stesso tempo, i file di log correnti non verranno troncati.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2a8ef-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a8ef-176">Remarks</span></span>

<span data-ttu-id="2a8ef-177">Per i diversi passaggi del backup vengono generate voci del registro eventi, inclusi i nomi dei file, il troncamento del log e il risultato finale del backup.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="2a8ef-178">I backup incrementali sono possibili solo dopo che è stato eseguito un backup completo.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="2a8ef-179">Inoltre, i backup incrementali sono possibili solo se la registrazione circolare è disattivata.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="2a8ef-180">È consigliabile che la directory di backup non contenga alcun file diverso da quello usato nel backup o aggiunto da un backup precedente riuscito.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="2a8ef-181">La directory di backup deve esistere a meno che non sia impostato il parametro *JET_paramCreatePathIfNotExist* per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="2a8ef-182">Per informazioni, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2a8ef-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="2a8ef-183">Il backup eseguirà una verifica del checksum su tutte le pagine di database utilizzate e a partire da Windows Server 2003 anche nei file di log.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="2a8ef-184">Questo consente di stimare l'integrità del database, anche per le pagine che non vengono lette durante le normali operazioni.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="2a8ef-185">Se viene rilevato un danneggiamento di questo tipo, il backup avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="2a8ef-186">Durante il backup, il file di log corrente verrà completato e verrà generato un nuovo log.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="2a8ef-187">In questo modo, tutti i file di log necessari possono essere copie, perché il log corrente non verrà più usato.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="2a8ef-188">Si consiglia vivamente di non usare il backup per scopi diversi dal backup e dal ripristino a livello di motore.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="2a8ef-189">Questo consente di ridurre al minimo la possibilità di ottenere errori durante le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2a8ef-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a8ef-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-191"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2a8ef-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2a8ef-192">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2a8ef-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2a8ef-194">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-195"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2a8ef-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2a8ef-196">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-197"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2a8ef-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2a8ef-198">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8ef-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2a8ef-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2a8ef-200">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8ef-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2a8ef-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2a8ef-202">Implementato come <strong>JetBackupW</strong> (Unicode) e <strong>JetBackupA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2a8ef-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2a8ef-203">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2a8ef-203">See Also</span></span>

[<span data-ttu-id="2a8ef-204">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="2a8ef-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="2a8ef-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2a8ef-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2a8ef-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2a8ef-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2a8ef-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2a8ef-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2a8ef-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="2a8ef-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="2a8ef-209">JetRestore</span><span class="sxs-lookup"><span data-stu-id="2a8ef-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="2a8ef-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="2a8ef-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="2a8ef-211">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="2a8ef-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="2a8ef-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2a8ef-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="2a8ef-213">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="2a8ef-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
