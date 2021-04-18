---
description: 'Altre informazioni su: funzione JetGetAttachInfo'
title: Funzione JetGetAttachInfo
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317345"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="95b4c-103">Funzione JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="95b4c-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="95b4c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="95b4c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="95b4c-105">Funzione JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="95b4c-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="95b4c-106">La funzione **JetGetAttachInfo** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza di per i nomi dei file di database che devono diventare parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="95b4c-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="95b4c-107">Verranno considerati solo i database attualmente collegati all'istanza che usa [JetAttachDatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="95b4c-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="95b4c-108">Questi file possono essere successivamente aperti con [JetOpenFile](./jetopenfile-function.md) e letti usando [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="95b4c-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="95b4c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="95b4c-109">Parameters</span></span>

<span data-ttu-id="95b4c-110">*SZZ*</span><span class="sxs-lookup"><span data-stu-id="95b4c-110">*szz*</span></span>

<span data-ttu-id="95b4c-111">Buffer di output che riceve l'elenco di stringhe con terminazione null che descrivono il set di file di database che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="95b4c-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="95b4c-112">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="95b4c-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="95b4c-113">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="95b4c-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="95b4c-114">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="95b4c-114">*cbMax*</span></span>

<span data-ttu-id="95b4c-115">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="95b4c-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="95b4c-116">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="95b4c-116">*pcbActual*</span></span>

<span data-ttu-id="95b4c-117">Puntatore al buffer di output che ha ricevuto la quantità effettiva di dati stringa.</span><span class="sxs-lookup"><span data-stu-id="95b4c-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="95b4c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95b4c-118">Return Value</span></span>

<span data-ttu-id="95b4c-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="95b4c-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="95b4c-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="95b4c-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95b4c-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95b4c-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="95b4c-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95b4c-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="95b4c-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="95b4c-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="95b4c-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="95b4c-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="95b4c-126">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="95b4c-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="95b4c-127">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="95b4c-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="95b4c-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="95b4c-129">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="95b4c-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="95b4c-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="95b4c-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="95b4c-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="95b4c-132">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="95b4c-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="95b4c-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="95b4c-134">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="95b4c-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="95b4c-135"><strong>JetGetAttachInfo</strong> restituirà questo errore se il backup corrente non è un backup completo.</span><span class="sxs-lookup"><span data-stu-id="95b4c-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="95b4c-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="95b4c-137">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="95b4c-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="95b4c-138">Questo problema può verificarsi per <strong>JetGetAttachInfo</strong> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="95b4c-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="95b4c-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="95b4c-140">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="95b4c-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="95b4c-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="95b4c-142">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="95b4c-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="95b4c-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="95b4c-144">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="95b4c-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="95b4c-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="95b4c-146">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="95b4c-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="95b4c-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="95b4c-148">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="95b4c-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95b4c-149">In caso di esito positivo, le informazioni richieste sul set di file di database che devono far parte del set di file di backup verranno inserite nei buffer di output specificati.</span><span class="sxs-lookup"><span data-stu-id="95b4c-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="95b4c-150">In caso di errore, lo stato dei buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="95b4c-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="95b4c-151">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="95b4c-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="95b4c-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="95b4c-152">Remarks</span></span>

<span data-ttu-id="95b4c-153">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="95b4c-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="95b4c-154">L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive dell'elenco e utilizzare tali informazioni per determinare se l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="95b4c-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="95b4c-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95b4c-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-156"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="95b4c-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95b4c-157">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="95b4c-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="95b4c-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95b4c-159">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="95b4c-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-160"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="95b4c-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95b4c-161">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="95b4c-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-162"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="95b4c-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="95b4c-163">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="95b4c-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b4c-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="95b4c-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="95b4c-165">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="95b4c-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b4c-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="95b4c-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="95b4c-167">Implementato come <strong>JetGetAttachInfoW</strong> (Unicode) e <strong>JetGetAttachInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="95b4c-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="95b4c-168">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="95b4c-168">See Also</span></span>

[<span data-ttu-id="95b4c-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="95b4c-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="95b4c-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="95b4c-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="95b4c-171">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="95b4c-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="95b4c-172">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="95b4c-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="95b4c-173">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="95b4c-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="95b4c-174">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="95b4c-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="95b4c-175">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="95b4c-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="95b4c-176">JetStopService</span><span class="sxs-lookup"><span data-stu-id="95b4c-176">JetStopService</span></span>](./jetstopservice-function.md)
