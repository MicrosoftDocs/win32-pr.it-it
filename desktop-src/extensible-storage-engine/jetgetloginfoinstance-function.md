---
description: 'Altre informazioni su: funzione JetGetLogInfoInstance'
title: JetGetLogInfoInstance (funzione)
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2056859bdce13dfdc28d4cbbf8716925d5bc1cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318093"
---
# <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="8eee2-103">JetGetLogInfoInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="8eee2-103">JetGetLogInfoInstance Function</span></span>


<span data-ttu-id="8eee2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8eee2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="8eee2-105">JetGetLogInfoInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="8eee2-105">JetGetLogInfoInstance Function</span></span>

<span data-ttu-id="8eee2-106">La funzione **JetGetLogInfoInstance** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza di per i nomi dei file di patch del database e i file di log delle transazioni che devono diventare parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="8eee2-106">The **JetGetLogInfoInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="8eee2-107">Questi file possono essere successivamente aperti con [JetOpenFile](./jetopenfile-function.md) e letti usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="8eee2-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="8eee2-108">**Windows XP: JetGetLogInfoInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8eee2-108">**Windows XP:  JetGetLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="8eee2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8eee2-109">Parameters</span></span>

<span data-ttu-id="8eee2-110">*istanza*</span><span class="sxs-lookup"><span data-stu-id="8eee2-110">*instance*</span></span>

<span data-ttu-id="8eee2-111">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="8eee2-111">The instance to use for this call.</span></span>

<span data-ttu-id="8eee2-112">Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="8eee2-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="8eee2-113">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="8eee2-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="8eee2-114">Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="8eee2-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="8eee2-115">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="8eee2-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="8eee2-116">*SZZ*</span><span class="sxs-lookup"><span data-stu-id="8eee2-116">*szz*</span></span>

<span data-ttu-id="8eee2-117">Il buffer di output che riceverà l'elenco di stringhe con terminazione null che descrivono il set di file di patch del database e i file di log delle transazioni che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="8eee2-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="8eee2-118">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8eee2-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="8eee2-119">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="8eee2-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="8eee2-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="8eee2-120">*cbMax*</span></span>

<span data-ttu-id="8eee2-121">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="8eee2-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="8eee2-122">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="8eee2-122">*pcbActual*</span></span>

<span data-ttu-id="8eee2-123">Riceve la quantità effettiva di dati stringa ricevuti nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="8eee2-123">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="8eee2-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8eee2-124">Return Value</span></span>

<span data-ttu-id="8eee2-125">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="8eee2-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8eee2-126">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="8eee2-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8eee2-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8eee2-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="8eee2-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8eee2-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8eee2-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8eee2-130">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8eee2-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-131">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="8eee2-131">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="8eee2-132">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="8eee2-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="8eee2-133">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8eee2-133">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-134">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8eee2-134">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8eee2-135">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8eee2-135">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8eee2-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8eee2-137">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="8eee2-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8eee2-138">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8eee2-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="8eee2-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="8eee2-140">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="8eee2-140">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="8eee2-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> restituirà questo errore se sono presenti handle di file in attesa creati utilizzando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="8eee2-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8eee2-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8eee2-143">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="8eee2-143">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="8eee2-144">Questo problema può verificarsi per <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="8eee2-144">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-145">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="8eee2-145">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="8eee2-146">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="8eee2-146">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8eee2-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8eee2-148">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="8eee2-148">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8eee2-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8eee2-150">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="8eee2-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="8eee2-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="8eee2-152">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="8eee2-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8eee2-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8eee2-154">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="8eee2-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8eee2-155">In caso di esito positivo, le informazioni richieste sul set di file di patch del database e i file di log delle transazioni che devono far parte del set di file di backup verranno inseriti nei buffer di output specificati.</span><span class="sxs-lookup"><span data-stu-id="8eee2-155">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="8eee2-156">La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="8eee2-156">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="8eee2-157">Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.</span><span class="sxs-lookup"><span data-stu-id="8eee2-157">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="8eee2-158">In caso di errore, lo stato dei buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="8eee2-158">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="8eee2-159">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8eee2-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8eee2-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eee2-160">Remarks</span></span>

<span data-ttu-id="8eee2-161">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="8eee2-161">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="8eee2-162">L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive dell'elenco e utilizzare tali informazioni per determinare se l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="8eee2-162">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8eee2-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eee2-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8eee2-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8eee2-165">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8eee2-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8eee2-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8eee2-167">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8eee2-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-168"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="8eee2-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8eee2-169">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="8eee2-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-170"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="8eee2-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8eee2-171">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8eee2-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8eee2-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8eee2-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8eee2-173">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8eee2-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8eee2-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8eee2-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8eee2-175">Implementato come <strong>JetGetLogInfoInstanceW</strong> (Unicode) e <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8eee2-175">Implemented as <strong>JetGetLogInfoInstanceW</strong> (Unicode) and <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8eee2-176">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8eee2-176">See Also</span></span>

[<span data-ttu-id="8eee2-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8eee2-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8eee2-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8eee2-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8eee2-179">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="8eee2-179">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="8eee2-180">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="8eee2-180">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="8eee2-181">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="8eee2-181">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="8eee2-182">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="8eee2-182">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="8eee2-183">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="8eee2-183">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="8eee2-184">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8eee2-184">JetStopService</span></span>](./jetstopservice-function.md)
