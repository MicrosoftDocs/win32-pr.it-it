---
description: 'Altre informazioni su: funzione JetGetLock'
title: JetGetLock (funzione)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132434"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="cec04-103">JetGetLock (funzione)</span><span class="sxs-lookup"><span data-stu-id="cec04-103">JetGetLock Function</span></span>


<span data-ttu-id="cec04-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cec04-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="cec04-105">JetGetLock (funzione)</span><span class="sxs-lookup"><span data-stu-id="cec04-105">JetGetLock Function</span></span>

<span data-ttu-id="cec04-106">La funzione **JetGetLock** fornisce un mezzo per riservare in modo esplicito la possibilità di aggiornare una riga, un blocco di scrittura o di impedire in modo esplicito l'aggiornamento di una riga da qualsiasi altra sessione, ovvero il blocco di lettura.</span><span class="sxs-lookup"><span data-stu-id="cec04-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="cec04-107">In genere, i blocchi di scrittura di riga vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe.</span><span class="sxs-lookup"><span data-stu-id="cec04-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="cec04-108">I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record.</span><span class="sxs-lookup"><span data-stu-id="cec04-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="cec04-109">Tuttavia, in alcuni casi è possibile che una transazione desideri bloccare in modo esplicito una riga per applicare la serializzazione o per assicurarsi che un'operazione successiva abbia esito positivo in virtù del fatto che i blocchi necessari sono già stati eseguiti.</span><span class="sxs-lookup"><span data-stu-id="cec04-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="cec04-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cec04-110">Parameters</span></span>

<span data-ttu-id="cec04-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cec04-111">*sesid*</span></span>

<span data-ttu-id="cec04-112">Sessione che verrà utilizzata per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="cec04-112">The session that will be used for this call.</span></span>

<span data-ttu-id="cec04-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="cec04-113">*tableid*</span></span>

<span data-ttu-id="cec04-114">Cursore che verrà utilizzato per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="cec04-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="cec04-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cec04-115">*grbit*</span></span>

<span data-ttu-id="cec04-116">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cec04-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cec04-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cec04-117">Value</span></span></p></th>
<th><p><span data-ttu-id="cec04-118">Significato</span><span class="sxs-lookup"><span data-stu-id="cec04-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cec04-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="cec04-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="cec04-120">Questo flag causa l'acquisizione di un blocco di lettura nel record corrente.</span><span class="sxs-lookup"><span data-stu-id="cec04-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="cec04-121">I blocchi di lettura non sono compatibili con i blocchi di scrittura già conservati da altre sessioni, ma sono compatibili con i blocchi di lettura mantenuti da altre sessioni.</span><span class="sxs-lookup"><span data-stu-id="cec04-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="cec04-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="cec04-123">Questo flag determina l'acquisizione di un blocco di scrittura nel record corrente.</span><span class="sxs-lookup"><span data-stu-id="cec04-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="cec04-124">I blocchi di scrittura non sono compatibili con i blocchi Write o Read utilizzati da altre sessioni, ma sono compatibili con i blocchi di lettura contenuti nella stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="cec04-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cec04-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cec04-125">Return Value</span></span>

<span data-ttu-id="cec04-126">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="cec04-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cec04-127">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="cec04-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cec04-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cec04-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="cec04-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cec04-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cec04-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cec04-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cec04-131">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="cec04-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cec04-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cec04-133">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="cec04-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cec04-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cec04-135">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="cec04-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cec04-136">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cec04-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="cec04-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="cec04-138">Il <em>grbit</em> specificato non è JET_bitReadLock o JET_bitWriteLock.</span><span class="sxs-lookup"><span data-stu-id="cec04-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="cec04-139">Deve essere uno di questi due flag.</span><span class="sxs-lookup"><span data-stu-id="cec04-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="cec04-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="cec04-141">Per poter acquisire un blocco, il cursore deve trovarsi in un record.</span><span class="sxs-lookup"><span data-stu-id="cec04-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="cec04-142">I blocchi sono sempre presenti nei record.</span><span class="sxs-lookup"><span data-stu-id="cec04-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cec04-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cec04-144">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="cec04-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="cec04-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="cec04-146">I blocchi possono essere acquisiti solo da sessioni in una transazione.</span><span class="sxs-lookup"><span data-stu-id="cec04-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="cec04-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="cec04-148">Il cursore non può essere di sola lettura e acquisire un blocco di scrittura.</span><span class="sxs-lookup"><span data-stu-id="cec04-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cec04-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cec04-150">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="cec04-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cec04-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cec04-152">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="cec04-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="cec04-153">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cec04-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cec04-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cec04-155">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="cec04-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="cec04-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="cec04-157">La sessione deve disporre delle autorizzazioni di scrittura per acquisire il blocco di scrittura.</span><span class="sxs-lookup"><span data-stu-id="cec04-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="cec04-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="cec04-159">Errore restituito quando viene richiesto un blocco in conflitto.</span><span class="sxs-lookup"><span data-stu-id="cec04-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cec04-160">In seguito all'esito positivo, la sessione ha acquisito il blocco richiesto.</span><span class="sxs-lookup"><span data-stu-id="cec04-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="cec04-161">In caso di errore, la sessione non ha acquisito il blocco richiesto.</span><span class="sxs-lookup"><span data-stu-id="cec04-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cec04-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="cec04-162">Remarks</span></span>

<span data-ttu-id="cec04-163">Non è possibile acquisire blocchi di scrittura con sessioni o cursori che dispongono di autorizzazioni di sola lettura, anche se la sessione e il cursore non eseguono un'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="cec04-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="cec04-164">Sia la sessione che il cursore devono disporre dei privilegi di scrittura per acquisire un blocco di scrittura.</span><span class="sxs-lookup"><span data-stu-id="cec04-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="cec04-165">I blocchi di lettura e scrittura sono un metodo di blocco pessimistico.</span><span class="sxs-lookup"><span data-stu-id="cec04-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="cec04-166">Il blocco pessimistico prevede più sessioni simultanee per il conflitto e acquisisce i blocchi in anticipo per assicurarsi che le operazioni abbiano esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cec04-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="cec04-167">La maggior parte delle operazioni sarà serializzabile in base ai blocchi acquisiti in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="cec04-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="cec04-168">Tuttavia, alcune operazioni non lo sono.</span><span class="sxs-lookup"><span data-stu-id="cec04-168">However, some operations will not.</span></span> <span data-ttu-id="cec04-169">Per illustrare questo problema, prendere in considerazione le due transazioni,</span><span class="sxs-lookup"><span data-stu-id="cec04-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="cec04-170">T1: R (A), U (B)</span><span class="sxs-lookup"><span data-stu-id="cec04-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="cec04-171">T2: R (B), U (A)</span><span class="sxs-lookup"><span data-stu-id="cec04-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="cec04-172">Il controllo delle versioni A livello di record garantisce che ogni transazione eseguita contemporaneamente visualizzerà i valori originali per A e B. Non esiste un ordine seriale di esecuzione che può produrre gli stessi risultati per A e B, nel caso in cui i risultati dipendano dai dati letti.</span><span class="sxs-lookup"><span data-stu-id="cec04-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="cec04-173">Per rendere serializzabile questa transazione, l'applicazione deve acquisire un blocco di lettura esplicito su A e B in ogni transazione quando viene letto il valore.</span><span class="sxs-lookup"><span data-stu-id="cec04-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cec04-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cec04-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cec04-175"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cec04-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cec04-176">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cec04-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cec04-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cec04-178">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cec04-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-179"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="cec04-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cec04-180">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="cec04-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cec04-181"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="cec04-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cec04-182">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cec04-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cec04-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cec04-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cec04-184">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cec04-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cec04-185">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cec04-185">See Also</span></span>

[<span data-ttu-id="cec04-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cec04-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cec04-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cec04-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cec04-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cec04-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cec04-189">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="cec04-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="cec04-190">JetStopService</span><span class="sxs-lookup"><span data-stu-id="cec04-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="cec04-191">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="cec04-191">JetUpdate</span></span>](./jetupdate-function.md)
