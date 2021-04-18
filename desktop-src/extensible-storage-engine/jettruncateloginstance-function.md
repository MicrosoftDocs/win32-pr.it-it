---
description: 'Altre informazioni su: funzione JetTruncateLogInstance'
title: JetTruncateLogInstance (funzione)
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307803"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="a5ce7-103">JetTruncateLogInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="a5ce7-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="a5ce7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a5ce7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="a5ce7-105">JetTruncateLogInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="a5ce7-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="a5ce7-106">La funzione **JetTruncateLogInstance** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eliminare tutti i file di log delle transazioni che non saranno più necessari dopo il completamento corretto del backup corrente.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="a5ce7-107">**Windows XP:**  **JetTruncateLogInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="a5ce7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5ce7-108">Parameters</span></span>

<span data-ttu-id="a5ce7-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="a5ce7-109">*instance*</span></span>

<span data-ttu-id="a5ce7-110">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-110">The instance to use for this call.</span></span>

<span data-ttu-id="a5ce7-111">Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="a5ce7-112">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="a5ce7-113">Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="a5ce7-114">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="a5ce7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5ce7-115">Return Value</span></span>

<span data-ttu-id="a5ce7-116">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a5ce7-117">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ce7-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5ce7-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a5ce7-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="a5ce7-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5ce7-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a5ce7-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-121">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="a5ce7-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-123"><strong>Windows Server 2003:</strong>  Questo valore restituito è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="a5ce7-124">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a5ce7-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-126">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a5ce7-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-128">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a5ce7-129">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="a5ce7-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-131">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="a5ce7-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> restituirà questo errore se sono presenti handle di file in attesa creati utilizzando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a5ce7-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-134">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="a5ce7-135">Questo problema può verificarsi per <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> quando l'handle di istanza specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a5ce7-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-137">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a5ce7-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-139">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a5ce7-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-141">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a5ce7-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-143">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a5ce7-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a5ce7-145">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5ce7-146">Se questa funzione ha esito positivo, il set di file di log delle transazioni che non sarà più necessario una volta completato correttamente il backup corrente viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="a5ce7-147">La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="a5ce7-148">Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="a5ce7-149">Se questa funzione ha esito negativo, la macchina a stati di backup può essere avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="a5ce7-150">È possibile che venga eliminato un numero di file di log delle transazioni inferiore al numero desiderato, ma che verranno sempre eliminati dal più vecchio al più recente.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a5ce7-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5ce7-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a5ce7-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a5ce7-153">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a5ce7-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a5ce7-155">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-156"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a5ce7-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a5ce7-157">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ce7-158"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a5ce7-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a5ce7-159">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ce7-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a5ce7-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a5ce7-161">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a5ce7-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a5ce7-162">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a5ce7-162">See Also</span></span>

[<span data-ttu-id="a5ce7-163">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="a5ce7-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="a5ce7-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a5ce7-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a5ce7-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a5ce7-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a5ce7-166">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="a5ce7-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="a5ce7-167">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="a5ce7-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="a5ce7-168">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="a5ce7-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="a5ce7-169">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a5ce7-169">JetStopService</span></span>](./jetstopservice-function.md)
