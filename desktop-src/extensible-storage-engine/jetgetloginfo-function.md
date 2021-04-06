---
description: 'Altre informazioni su: funzione JetGetLogInfo'
title: JetGetLogInfo (funzione)
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c96827be0ac62502e7545a9acb1fe157f3b28fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758486"
---
# <a name="jetgetloginfo-function"></a><span data-ttu-id="b9667-103">JetGetLogInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="b9667-103">JetGetLogInfo Function</span></span>


<span data-ttu-id="b9667-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b9667-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfo-function"></a><span data-ttu-id="b9667-105">JetGetLogInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="b9667-105">JetGetLogInfo Function</span></span>

<span data-ttu-id="b9667-106">La funzione **JetGetLogInfo** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza di per i nomi dei file di patch del database e i file di log delle transazioni che devono diventare parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="b9667-106">The **JetGetLogInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="b9667-107">Questi file possono essere successivamente aperti con [JetOpenFile](./jetopenfile-function.md) e letti usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9667-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="b9667-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9667-108">Parameters</span></span>

<span data-ttu-id="b9667-109">*SZZ*</span><span class="sxs-lookup"><span data-stu-id="b9667-109">*szz*</span></span>

<span data-ttu-id="b9667-110">Il buffer di output che riceverà l'elenco di stringhe con terminazione null che descrivono il set di file di patch del database e i file di log delle transazioni che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="b9667-110">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="b9667-111">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9667-111">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="b9667-112">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="b9667-112">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="b9667-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="b9667-113">*cbMax*</span></span>

<span data-ttu-id="b9667-114">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="b9667-114">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="b9667-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="b9667-115">*pcbActual*</span></span>

<span data-ttu-id="b9667-116">Riceve la quantità effettiva di dati stringa ricevuti nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="b9667-116">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="b9667-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9667-117">Return Value</span></span>

<span data-ttu-id="b9667-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b9667-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b9667-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b9667-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9667-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b9667-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="b9667-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9667-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9667-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b9667-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b9667-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b9667-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-124">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="b9667-124">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="b9667-125">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="b9667-125">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="b9667-126">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b9667-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b9667-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b9667-128">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b9667-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b9667-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b9667-130">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="b9667-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="b9667-131">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b9667-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-132">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="b9667-132">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="b9667-133">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="b9667-133">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="b9667-134"><strong>JetGetLogInfo</strong> restituirà questo errore se sono presenti handle di file in attesa creati utilizzando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="b9667-134"><strong>JetGetLogInfo</strong> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b9667-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b9667-136">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="b9667-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="b9667-137">Questo problema può verificarsi per <strong>JetGetLogInfo</strong> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="b9667-137">This can happen for <strong>JetGetLogInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-138">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="b9667-138">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="b9667-139">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="b9667-139">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-140">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b9667-140">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b9667-141">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="b9667-141">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b9667-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b9667-143">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="b9667-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-144">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="b9667-144">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="b9667-145">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="b9667-145">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b9667-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b9667-147">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="b9667-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9667-148">In caso di esito positivo, le informazioni richieste sul set di file di patch del database e i file di log delle transazioni che devono far parte del set di file di backup verranno inseriti nei buffer di output specificati.</span><span class="sxs-lookup"><span data-stu-id="b9667-148">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="b9667-149">La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="b9667-149">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="b9667-150">Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.</span><span class="sxs-lookup"><span data-stu-id="b9667-150">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="b9667-151">In caso di errore, lo stato dei buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="b9667-151">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="b9667-152">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="b9667-152">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b9667-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9667-153">Remarks</span></span>

<span data-ttu-id="b9667-154">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="b9667-154">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="b9667-155">L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive dell'elenco e utilizzare tali informazioni per determinare se l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="b9667-155">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b9667-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9667-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9667-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b9667-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b9667-158">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b9667-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b9667-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b9667-160">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b9667-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-161"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b9667-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b9667-162">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b9667-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-163"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b9667-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b9667-164">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b9667-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9667-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b9667-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b9667-166">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b9667-166">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9667-167"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b9667-167"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b9667-168">Implementato come <strong>JetGetLogInfoW</strong> (Unicode) e <strong>JetGetLogInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b9667-168">Implemented as <strong>JetGetLogInfoW</strong> (Unicode) and <strong>JetGetLogInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b9667-169">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b9667-169">See Also</span></span>

[<span data-ttu-id="b9667-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b9667-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b9667-171">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b9667-171">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b9667-172">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="b9667-172">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="b9667-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="b9667-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="b9667-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="b9667-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="b9667-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="b9667-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="b9667-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="b9667-176">JetStopBackup</span></span>](./jetstopbackup-function.md)
