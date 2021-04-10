---
description: 'Altre informazioni su: funzione JetEndExternalBackupInstance'
title: JetEndExternalBackupInstance (funzione)
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057926"
---
# <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="5c3ac-103">JetEndExternalBackupInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-103">JetEndExternalBackupInstance Function</span></span>


<span data-ttu-id="5c3ac-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5c3ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="5c3ac-105">JetEndExternalBackupInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-105">JetEndExternalBackupInstance Function</span></span>

<span data-ttu-id="5c3ac-106">La funzione **JetEndExternalBackupInstance** termina una sessione di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-106">The **JetEndExternalBackupInstance** function ends an external backup session.</span></span> <span data-ttu-id="5c3ac-107">Questa API è l'ultima API in una serie di API che devono essere chiamate per eseguire un backup online (non basato su VSS) riuscito.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="5c3ac-108">**Windows XP: JetEndExternalBackupInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-108">**Windows XP:  JetEndExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="5c3ac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c3ac-109">Parameters</span></span>

<span data-ttu-id="5c3ac-110">*istanza*</span><span class="sxs-lookup"><span data-stu-id="5c3ac-110">*instance*</span></span>

<span data-ttu-id="5c3ac-111">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-111">The instance to use for this call.</span></span>

<span data-ttu-id="5c3ac-112">**Windows 2000:** Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="5c3ac-113">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="5c3ac-114">**Windows XP:** Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="5c3ac-115">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="5c3ac-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c3ac-116">Return Value</span></span>

<span data-ttu-id="5c3ac-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5c3ac-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5c3ac-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c3ac-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c3ac-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="5c3ac-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c3ac-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-123">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="5c3ac-123">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-124"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-124"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="5c3ac-125">Il chiamante ha terminato un backup al centro della sequenza di backup senza segnalare l'intenzione con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-125">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="5c3ac-126">Questo errore è il risultato di un bug nel client di backup in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-126">This error is the result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="5c3ac-127">In Windows XP viene restituito questo errore per una chiusura intenzionale della sequenza di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-127">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-128">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="5c3ac-128">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-129"><strong>Windows Server 2003:  </strong> Questo valore restituito è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-129"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="5c3ac-130">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-130">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-132">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-134"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="5c3ac-135">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-135">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-137">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5c3ac-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-139">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5c3ac-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-141">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="5c3ac-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-143">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5c3ac-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5c3ac-145">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c3ac-146">Se la funzione ha esito positivo, il backup esterno ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-146">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="5c3ac-147">Success indica che tutti i file, ad esempio i database e i log, appropriati per il tipo di backup (specificato in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) sono stati recuperati dal motore di backup.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-147">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="5c3ac-148">I file di cui è stato eseguito il backup possono essere ripristinati con ripristino hardware ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-148">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="5c3ac-149">Se questa funzione ha esito negativo, il backup esterno termina in genere.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-149">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="5c3ac-150">Errore indica che il backup non è valido a causa di un errore di utilizzo del client o dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-150">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="5c3ac-151">È importante controllare il codice restituito per questa API per verificare che la sequenza di backup sia stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-151">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5c3ac-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c3ac-152">Remarks</span></span>

<span data-ttu-id="5c3ac-153">Se il motore è configurato per registrare gli eventi, viene registrato un evento per indicare la risoluzione del backup esterno.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-153">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="5c3ac-154">Se la sequenza di backup non viene completata in ordine e con una chiamata riuscita a [JetEndExternalBackup](./jetendexternalbackup-function.md), i successivi backup incrementali potrebbero contenere un numero di dati superiore a quello previsto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-154">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="5c3ac-155">Per ulteriori informazioni sulla sequenza di API di backup esterno, vedere [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-155">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="5c3ac-156">Prima di Windows Vista, se il troncamento del log non è stato eseguito, il motore ha considerato che il backup era un backup di copia.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-156">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="5c3ac-157">Tuttavia, il backup potrebbe essere un backup normale per il quale non è stato eseguito il troncamento (ad esempio, se sono presenti database scollegati).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-157">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="5c3ac-158">È possibile utilizzare l'opzione JET_bitBackupTruncateDone per informare il motore e consentire le modifiche appropriate dell'intestazione del database.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-158">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow proper database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5c3ac-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c3ac-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-160"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5c3ac-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3ac-161">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-161">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5c3ac-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3ac-163">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-163">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-164"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5c3ac-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3ac-165">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3ac-166"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5c3ac-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3ac-167">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3ac-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5c3ac-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3ac-169">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5c3ac-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5c3ac-170">See Also</span></span>

[<span data-ttu-id="5c3ac-171">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="5c3ac-171">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="5c3ac-172">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-172">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="5c3ac-173">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="5c3ac-173">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="5c3ac-174">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-174">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="5c3ac-175">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-175">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="5c3ac-176">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-176">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="5c3ac-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5c3ac-178">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-178">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="5c3ac-179">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-179">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="5c3ac-180">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-180">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="5c3ac-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5c3ac-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5c3ac-182">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-182">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="5c3ac-183">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-183">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="5c3ac-184">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-184">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="5c3ac-185">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-185">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="5c3ac-186">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="5c3ac-186">JetTruncateLog</span></span>](./jettruncatelog-function.md)
