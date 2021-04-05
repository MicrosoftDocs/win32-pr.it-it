---
description: 'Altre informazioni su: funzione JetTruncateLog'
title: JetTruncateLog (funzione)
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750479"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="bdc45-103">JetTruncateLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="bdc45-103">JetTruncateLog Function</span></span>


<span data-ttu-id="bdc45-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bdc45-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="bdc45-105">JetTruncateLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="bdc45-105">JetTruncateLog Function</span></span>

<span data-ttu-id="bdc45-106">La funzione **JetTruncateLog** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eliminare tutti i file di log delle transazioni che non saranno più necessari dopo il completamento corretto del backup corrente.</span><span class="sxs-lookup"><span data-stu-id="bdc45-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="bdc45-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdc45-107">Parameters</span></span>

<span data-ttu-id="bdc45-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="bdc45-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="bdc45-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdc45-109">Return Value</span></span>

<span data-ttu-id="bdc45-110">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="bdc45-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bdc45-111">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc45-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdc45-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bdc45-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="bdc45-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdc45-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bdc45-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bdc45-115">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="bdc45-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="bdc45-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="bdc45-117">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="bdc45-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="bdc45-118"><strong>Windows Server 2003:</strong>  Questo valore restituito è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bdc45-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bdc45-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bdc45-120">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bdc45-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bdc45-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bdc45-122">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="bdc45-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bdc45-123"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bdc45-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="bdc45-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="bdc45-125">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="bdc45-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="bdc45-126"><strong>JetTruncateLog</strong> restituirà questo errore se sono presenti handle di file in attesa creati utilizzando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="bdc45-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bdc45-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bdc45-128">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bdc45-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="bdc45-129">Questo problema può verificarsi per <strong>JetTruncateLog</strong> quando l'handle di istanza specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="bdc45-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="bdc45-130"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bdc45-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="bdc45-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="bdc45-132">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="bdc45-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bdc45-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bdc45-134">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="bdc45-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bdc45-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bdc45-136">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="bdc45-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="bdc45-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="bdc45-138">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="bdc45-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bdc45-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bdc45-140">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="bdc45-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bdc45-141">Se questa funzione ha esito positivo, il set di file di log delle transazioni che non sarà più necessario una volta completato correttamente il backup corrente viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="bdc45-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="bdc45-142">La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="bdc45-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="bdc45-143">Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.</span><span class="sxs-lookup"><span data-stu-id="bdc45-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="bdc45-144">Se questa funzione ha esito negativo, la macchina a stati di backup può essere avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="bdc45-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="bdc45-145">È possibile che venga eliminato un numero di file di log delle transazioni inferiore al numero desiderato, ma che verranno sempre eliminati dal più vecchio al più recente.</span><span class="sxs-lookup"><span data-stu-id="bdc45-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bdc45-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdc45-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bdc45-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bdc45-148">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bdc45-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bdc45-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bdc45-150">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bdc45-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-151"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="bdc45-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bdc45-152">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="bdc45-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdc45-153"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="bdc45-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bdc45-154">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bdc45-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdc45-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bdc45-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bdc45-156">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bdc45-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bdc45-157">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bdc45-157">See Also</span></span>

[<span data-ttu-id="bdc45-158">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="bdc45-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="bdc45-159">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="bdc45-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="bdc45-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bdc45-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bdc45-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bdc45-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="bdc45-162">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="bdc45-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="bdc45-163">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="bdc45-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="bdc45-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="bdc45-164">JetStopService</span></span>](./jetstopservice-function.md)
