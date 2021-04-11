---
description: 'Altre informazioni su: funzione JetBackupInstance'
title: Funzione JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128175"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="1d2b8-103">Funzione JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="1d2b8-103">JetBackupInstance Function</span></span>


<span data-ttu-id="1d2b8-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d2b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="1d2b8-105">Funzione JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="1d2b8-105">JetBackupInstance Function</span></span>

<span data-ttu-id="1d2b8-106">La funzione **JetBackupInstance** esegue un backup di flusso di un'istanza, inclusi tutti i database collegati, in una directory.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="1d2b8-107">Con più metodi di backup supportati dal motore di, questa è la funzione più semplice e incapsulata.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="1d2b8-108">**Windows XP: JetBackupInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="1d2b8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d2b8-109">Parameters</span></span>

<span data-ttu-id="1d2b8-110">*istanza*</span><span class="sxs-lookup"><span data-stu-id="1d2b8-110">*instance*</span></span>

<span data-ttu-id="1d2b8-111">Istanza del database di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-111">The instance of the database to backup.</span></span>

<span data-ttu-id="1d2b8-112">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="1d2b8-112">*szBackupPath*</span></span>

<span data-ttu-id="1d2b8-113">Directory in cui è archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-113">The directory where the backup is stored.</span></span> <span data-ttu-id="1d2b8-114">Se il percorso di backup è NULL per usare la funzione, i log vengono troncati, se possibile.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="1d2b8-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1d2b8-115">*grbit*</span></span>

<span data-ttu-id="1d2b8-116">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d2b8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1d2b8-117">Value</span></span></p></th>
<th><p><span data-ttu-id="1d2b8-118">Significato</span><span class="sxs-lookup"><span data-stu-id="1d2b8-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="1d2b8-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-120">Crea un backup completo del database.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-120">Creates a full backup of the database.</span></span> <span data-ttu-id="1d2b8-121">In questo modo è possibile mantenere un backup esistente nella stessa directory se il nuovo backup non riesce.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="1d2b8-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-123">Crea un backup incrementale anziché un backup completo.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="1d2b8-124">Ciò significa che verrà eseguito il backup solo dei file di log creati dopo l'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="1d2b8-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-126">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d2b8-127">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="1d2b8-127">*pfnStatus*</span></span>

<span data-ttu-id="1d2b8-128">Puntatore alla funzione di callback [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , che fornisce informazioni di notifica sullo stato di avanzamento dell'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="1d2b8-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d2b8-129">Return Value</span></span>

<span data-ttu-id="1d2b8-130">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1d2b8-131">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1d2b8-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d2b8-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1d2b8-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="1d2b8-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d2b8-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1d2b8-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-135">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="1d2b8-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-137">È già in corso un backup per la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="1d2b8-138">Non sono consentiti più backup contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="1d2b8-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-140">L'istanza non è ancora pronta per il backup mentre è in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1d2b8-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-142">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1d2b8-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-144">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1d2b8-145"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="1d2b8-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-147">Un backup incrementale non è consentito se la registrazione circolare è attiva.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="1d2b8-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-149">Le opzioni specificate non sono valide.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1d2b8-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-151">Un parametro non valido è stato passato nell'API.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1d2b8-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-153">Il percorso di destinazione non esiste.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="1d2b8-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-155">L'istanza è in esecuzione senza registrazione.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-155">The instance is running without logging.</span></span> <span data-ttu-id="1d2b8-156">Nessun backup consentito.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1d2b8-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-158">Si è verificato un errore di verifica del checksum in un file di log.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="1d2b8-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-160">La registrazione per l'istanza è temporanea o è disabilitata definitivamente a causa di un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1d2b8-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-162">Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1d2b8-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-164">Si è verificato un errore di verifica del checksum in una pagina del database.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1d2b8-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-166">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1d2b8-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-168">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1d2b8-169"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1d2b8-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1d2b8-171">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d2b8-172">Dopo che la funzione ha restituito esito positivo, nella directory di backup saranno presenti tutti i file necessari per un ripristino fino al momento del backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="1d2b8-173">Se si tratta di un backup completo, i file saranno i file di database e i file di log necessari per portare il database in uno stato coerente.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="1d2b8-174">Se si tratta di un backup incrementale, verranno aggiunti solo i file di log alle directory, ma i file già esistenti (database e file di log) insieme ai nuovi file di registro saranno in grado di ripristinare e ripristinare lo stato del database al momento del backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="1d2b8-175">Come effetto collaterale del backup, i file di log che non sono più necessari verranno troncati.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="1d2b8-176">Allo stesso tempo, le intestazioni del database verranno aggiornate con le informazioni relative al momento in cui è avvenuto l'ultimo backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="1d2b8-177">In caso di errore, non saranno presenti file nella destinazione della directory di backup, quindi non sarà possibile eseguire alcun ripristino.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="1d2b8-178">Nello stesso tempo, i file di log correnti non verranno troncati.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1d2b8-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d2b8-179">Remarks</span></span>

<span data-ttu-id="1d2b8-180">Nei diversi passaggi del backup vengono generate voci del registro eventi, inclusi i nomi dei file, il troncamento del log e il risultato finale del backup.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="1d2b8-181">Il backup incrementale è possibile solo dopo che è stato eseguito un backup completo.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="1d2b8-182">Inoltre, i backup incrementali sono possibili solo se la registrazione circolare è disattivata.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="1d2b8-183">È consigliabile che la directory di backup non contenga altri file, quindi quello incluso nel backup o aggiunto da un backup precedente riuscito.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="1d2b8-184">La directory di backup deve esistere a meno che non sia impostato il parametro *JET_paramCreatePathIfNotExist* per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="1d2b8-185">Per informazioni, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d2b8-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="1d2b8-186">Il backup eseguirà la verifica del checksum su tutte le pagine di database utilizzate e a partire da Windows Server 2003 anche nei file di log.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="1d2b8-187">Questo consente di stimare l'integrità del database anche per le pagine che non vengono lette durante le normali operazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="1d2b8-188">Se viene rilevato un danneggiamento di questo tipo, il backup avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="1d2b8-189">Durante il backup, il file di log corrente verrà completato e verrà avviata una nuova generazione del log.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="1d2b8-190">In questo modo sarà possibile copiare i file di log necessari, perché l'ultimo necessario non sarà più in uso.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="1d2b8-191">Si consiglia vivamente di non usare il backup per altri scopi, quindi il backup e il ripristino a livello di motore.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="1d2b8-192">Questa operazione consente di ridurre al minimo le modifiche apportate agli errori durante le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1d2b8-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d2b8-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1d2b8-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d2b8-195">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1d2b8-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d2b8-197">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-198"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1d2b8-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d2b8-199">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-200"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1d2b8-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1d2b8-201">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2b8-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1d2b8-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1d2b8-203">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1d2b8-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2b8-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1d2b8-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1d2b8-205">Implementato come <strong>JetBackupInstanceW</strong> (Unicode) e <strong>JetBackupInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1d2b8-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1d2b8-206">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1d2b8-206">See Also</span></span>

[<span data-ttu-id="1d2b8-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1d2b8-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1d2b8-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1d2b8-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1d2b8-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1d2b8-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1d2b8-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="1d2b8-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="1d2b8-211">JetRestore</span><span class="sxs-lookup"><span data-stu-id="1d2b8-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="1d2b8-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="1d2b8-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="1d2b8-213">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="1d2b8-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="1d2b8-214">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="1d2b8-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="1d2b8-215">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="1d2b8-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
