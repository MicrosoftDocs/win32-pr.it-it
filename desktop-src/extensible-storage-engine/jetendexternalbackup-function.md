---
description: 'Altre informazioni su: funzione JetEndExternalBackup'
title: Funzione JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319634"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="18330-103">Funzione JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="18330-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="18330-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18330-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="18330-105">Funzione JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="18330-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="18330-106">La funzione **JetEndExternalBackup** termina una sessione di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="18330-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="18330-107">Questa funzione è l'ultimo elemento API in una serie di elementi API che devono essere chiamati per eseguire un backup online (non basato su VSS) riuscito.</span><span class="sxs-lookup"><span data-stu-id="18330-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="18330-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="18330-108">Parameters</span></span>

<span data-ttu-id="18330-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="18330-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="18330-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18330-110">Return Value</span></span>

<span data-ttu-id="18330-111">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="18330-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="18330-112">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="18330-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18330-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="18330-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="18330-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18330-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18330-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="18330-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="18330-116">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="18330-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="18330-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="18330-118">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="18330-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18330-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="18330-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="18330-120">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="18330-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="18330-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="18330-122"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP</span><span class="sxs-lookup"><span data-stu-id="18330-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="18330-123">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede l'accesso a tutti i dati da revocare per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="18330-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18330-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="18330-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="18330-125">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="18330-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="18330-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="18330-127">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="18330-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18330-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="18330-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="18330-129">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="18330-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="18330-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="18330-131"><strong>Windows Server 2003:  </strong> Questo valore restituito è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18330-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="18330-132">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="18330-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18330-133">errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="18330-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="18330-134"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18330-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="18330-135">Il chiamante ha terminato un backup al centro della sequenza di backup senza segnalare l'intenzione con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="18330-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="18330-136">Questo errore è il risultato di un bug nel client di backup in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="18330-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="18330-137">In Windows XP viene restituito questo errore per una chiusura intenzionale della sequenza di backup esterna.</span><span class="sxs-lookup"><span data-stu-id="18330-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="18330-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="18330-139">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="18330-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18330-140">Se questa funzione ha esito positivo, il backup esterno ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="18330-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="18330-141">Success indica che tutti i file, ad esempio i database e i log, appropriati per il tipo di backup (specificato in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) sono stati recuperati dal motore di backup.</span><span class="sxs-lookup"><span data-stu-id="18330-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="18330-142">I file di cui è stato eseguito il backup possono essere ripristinati con ripristino hardware ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="18330-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="18330-143">Se questa funzione ha esito negativo, il backup esterno termina in genere.</span><span class="sxs-lookup"><span data-stu-id="18330-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="18330-144">Errore indica che il backup non è valido a causa di un errore di utilizzo del client o dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18330-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="18330-145">È importante controllare il codice restituito per questa API per verificare che la sequenza di backup sia stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="18330-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="18330-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="18330-146">Remarks</span></span>

<span data-ttu-id="18330-147">Se il motore è configurato per registrare gli eventi, viene registrato un evento per indicare la risoluzione del backup esterno.</span><span class="sxs-lookup"><span data-stu-id="18330-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="18330-148">Se la sequenza di backup non viene completata in ordine e con una chiamata riuscita a **JetEndExternalBackup**, i successivi backup incrementali potrebbero contenere un numero di dati superiore a quello previsto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18330-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="18330-149">Per ulteriori informazioni sulla sequenza di API di backup esterno, vedere [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="18330-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="18330-150">Prima di Windows Vista, se il troncamento del log non è stato eseguito, il motore ha considerato che il backup era un backup di copia.</span><span class="sxs-lookup"><span data-stu-id="18330-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="18330-151">Tuttavia, il backup potrebbe essere un backup normale per il quale non è stato eseguito il troncamento (ad esempio, se sono presenti database scollegati).</span><span class="sxs-lookup"><span data-stu-id="18330-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="18330-152">È possibile utilizzare l'opzione JET_bitBackupTruncateDone per informare il motore e consentire le modifiche appropriate dell'intestazione del database.</span><span class="sxs-lookup"><span data-stu-id="18330-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="18330-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18330-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18330-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18330-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18330-155">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="18330-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18330-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18330-157">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="18330-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18330-158"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="18330-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18330-159">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="18330-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18330-160"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="18330-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="18330-161">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="18330-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18330-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="18330-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="18330-163">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="18330-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="18330-164">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="18330-164">See Also</span></span>

[<span data-ttu-id="18330-165">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="18330-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="18330-166">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="18330-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="18330-167">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="18330-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="18330-168">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="18330-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="18330-169">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="18330-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="18330-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="18330-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="18330-171">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="18330-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="18330-172">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="18330-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="18330-173">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="18330-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="18330-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="18330-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="18330-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="18330-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="18330-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="18330-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="18330-177">JetStopService</span><span class="sxs-lookup"><span data-stu-id="18330-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="18330-178">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="18330-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)
