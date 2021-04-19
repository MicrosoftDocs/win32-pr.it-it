---
description: 'Altre informazioni su: funzione JetGetTruncateLogInfoInstance'
title: JetGetTruncateLogInfoInstance (funzione)
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318091"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="16266-103">JetGetTruncateLogInfoInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="16266-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="16266-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="16266-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="16266-105">JetGetTruncateLogInfoInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="16266-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="16266-106">La funzione **JetGetTruncateLogInfoInstance** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza di per i nomi dei file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup.</span><span class="sxs-lookup"><span data-stu-id="16266-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="16266-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16266-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="16266-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="16266-108">Parameters</span></span>

<span data-ttu-id="16266-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="16266-109">*instance*</span></span>

<span data-ttu-id="16266-110">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="16266-110">The instance to use for this call.</span></span>

<span data-ttu-id="16266-111">*SZZ*</span><span class="sxs-lookup"><span data-stu-id="16266-111">*szz*</span></span>

<span data-ttu-id="16266-112">Buffer di output che riceve l'elenco di stringhe con terminazione null che descrivono il set di file di log delle transazioni che possono essere eliminati in modo sicuro dopo che il backup è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="16266-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="16266-113">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringa utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="16266-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="16266-114">Ogni stringa con terminazione null viene restituita in sequenza e seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="16266-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="16266-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="16266-115">*cbMax*</span></span>

<span data-ttu-id="16266-116">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="16266-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="16266-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="16266-117">*pcbActual*</span></span>

<span data-ttu-id="16266-118">Puntatore al buffer di output che riceve la quantità effettiva di dati stringa.</span><span class="sxs-lookup"><span data-stu-id="16266-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="16266-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16266-119">Return Value</span></span>

<span data-ttu-id="16266-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="16266-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="16266-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="16266-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16266-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="16266-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="16266-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16266-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16266-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="16266-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="16266-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="16266-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="16266-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="16266-127">Uno dei parametri specificati contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="16266-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="16266-128"><strong>Windows XP e versioni successive:</strong>  Questo problema può verificarsi per <strong>JetGetTruncateLogInfoInstance</strong> quando l'handle di istanza specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="16266-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="16266-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="16266-130">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="16266-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="16266-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="16266-132">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="16266-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="16266-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="16266-134">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="16266-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="16266-135"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16266-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="16266-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="16266-137">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="16266-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="16266-138"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16266-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="16266-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="16266-140">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="16266-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="16266-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="16266-142">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="16266-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="16266-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="16266-144">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="16266-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="16266-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="16266-146">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="16266-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-147"><strong>JetGetTruncateLogInfoInstance</strong></span><span class="sxs-lookup"><span data-stu-id="16266-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-148">Sono presenti handle di file in attesa creati utilizzando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="16266-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16266-149">Se questa funzione ha esito positivo, le informazioni richieste sul set di file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup verranno inserite nei buffer di output in cui vengono fornite.</span><span class="sxs-lookup"><span data-stu-id="16266-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="16266-150">La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito.</span><span class="sxs-lookup"><span data-stu-id="16266-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="16266-151">Oltre questo punto, è possibile aprire solo file di patch del database e file di log delle transazioni per il backup.</span><span class="sxs-lookup"><span data-stu-id="16266-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="16266-152">Se questa funzione ha esito negativo, lo stato dei buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="16266-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="16266-153">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="16266-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="16266-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="16266-154">Remarks</span></span>

<span data-ttu-id="16266-155">Questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="16266-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="16266-156">L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive dell'elenco e utilizzare tali informazioni per determinare se l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="16266-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="16266-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16266-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16266-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="16266-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-159">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16266-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="16266-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-161">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="16266-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-162"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="16266-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-163">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="16266-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-164"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="16266-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-165">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="16266-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16266-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="16266-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-167">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="16266-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16266-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="16266-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="16266-169">Implementato come <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) e <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="16266-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="16266-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="16266-170">See Also</span></span>

[<span data-ttu-id="16266-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="16266-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="16266-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="16266-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="16266-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="16266-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="16266-174">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="16266-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="16266-175">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="16266-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="16266-176">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="16266-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="16266-177">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="16266-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="16266-178">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="16266-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="16266-179">JetRollback</span><span class="sxs-lookup"><span data-stu-id="16266-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="16266-180">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="16266-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="16266-181">JetStopService</span><span class="sxs-lookup"><span data-stu-id="16266-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="16266-182">JetTerm</span><span class="sxs-lookup"><span data-stu-id="16266-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="16266-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="16266-183">JetTerm2</span></span>](./jetterm2-function.md)
