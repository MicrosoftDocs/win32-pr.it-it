---
description: 'Altre informazioni su: funzione JetGetAttachInfoInstance'
title: JetGetAttachInfoInstance (funzione)
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882270"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="aa391-103">JetGetAttachInfoInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="aa391-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="aa391-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aa391-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="aa391-105">JetGetAttachInfoInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="aa391-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="aa391-106">La funzione **JetGetAttachInfoInstance** viene utilizzata durante un backup avviato da [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) per eseguire una query su un'istanza di per i nomi dei file di database che devono diventare parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="aa391-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="aa391-107">Verranno considerati solo i database attualmente collegati all'istanza di utilizzando [JetAttachDatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="aa391-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="aa391-108">Questi file possono essere successivamente aperti con [JetOpenFileInstance](./jetopenfileinstance-function.md) e letti usando [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="aa391-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="aa391-109">**Windows XP: JetGetAttachInfoInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aa391-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="aa391-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa391-110">Parameters</span></span>

<span data-ttu-id="aa391-111">*istanza*</span><span class="sxs-lookup"><span data-stu-id="aa391-111">*instance*</span></span>

<span data-ttu-id="aa391-112">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="aa391-112">The instance to use for this call.</span></span>

<span data-ttu-id="aa391-113">Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="aa391-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="aa391-114">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="aa391-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="aa391-115">Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="aa391-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="aa391-116">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="aa391-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="aa391-117">*SZZ*</span><span class="sxs-lookup"><span data-stu-id="aa391-117">*szz*</span></span>

<span data-ttu-id="aa391-118">Buffer di output che riceve l'elenco di stringhe con terminazione null che descrivono il set di file di database che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="aa391-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="aa391-119">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="aa391-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="aa391-120">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="aa391-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="aa391-121">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="aa391-121">*cbMax*</span></span>

<span data-ttu-id="aa391-122">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="aa391-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="aa391-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="aa391-123">*pcbActual*</span></span>

<span data-ttu-id="aa391-124">Puntatore al buffer di output che riceve la quantità effettiva di dati stringa.</span><span class="sxs-lookup"><span data-stu-id="aa391-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="aa391-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa391-125">Return Value</span></span>

<span data-ttu-id="aa391-126">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="aa391-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aa391-127">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="aa391-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa391-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="aa391-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="aa391-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa391-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa391-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aa391-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aa391-131">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="aa391-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="aa391-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="aa391-133">L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="aa391-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="aa391-134">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="aa391-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="aa391-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="aa391-136">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="aa391-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="aa391-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="aa391-138">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="aa391-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="aa391-139">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="aa391-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="aa391-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="aa391-141">L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="aa391-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="aa391-142"><strong>JetGetAttachInfoInstance</strong> restituirà questo errore se il backup corrente non è un backup completo.</span><span class="sxs-lookup"><span data-stu-id="aa391-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="aa391-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="aa391-144">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="aa391-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="aa391-145">Questo problema può verificarsi per <strong>JetGetAttachInfoInstance</strong> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="aa391-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="aa391-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="aa391-147">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="aa391-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="aa391-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="aa391-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="aa391-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="aa391-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="aa391-151">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="aa391-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="aa391-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="aa391-153">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="aa391-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="aa391-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="aa391-155">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="aa391-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa391-156">In caso di esito positivo, le informazioni richieste sul set di file di database che devono far parte del set di file di backup verranno inserite nei buffer di output specificati.</span><span class="sxs-lookup"><span data-stu-id="aa391-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="aa391-157">In caso di errore, lo stato dei buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="aa391-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="aa391-158">L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="aa391-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="aa391-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa391-159">Remarks</span></span>

<span data-ttu-id="aa391-160">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="aa391-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="aa391-161">L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive dell'elenco e utilizzare tali informazioni per determinare se l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="aa391-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="aa391-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa391-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa391-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="aa391-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aa391-164">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aa391-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="aa391-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aa391-166">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aa391-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-167"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="aa391-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aa391-168">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="aa391-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-169"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="aa391-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aa391-170">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="aa391-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa391-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="aa391-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aa391-172">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="aa391-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa391-173"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="aa391-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="aa391-174">Implementato come <strong>JetGetAttachInfoInstanceW</strong> (Unicode) e <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="aa391-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aa391-175">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aa391-175">See Also</span></span>

[<span data-ttu-id="aa391-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aa391-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aa391-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="aa391-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="aa391-178">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="aa391-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="aa391-179">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="aa391-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="aa391-180">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="aa391-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="aa391-181">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="aa391-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="aa391-182">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="aa391-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="aa391-183">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="aa391-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
