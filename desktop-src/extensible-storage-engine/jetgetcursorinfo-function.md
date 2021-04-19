---
description: 'Altre informazioni su: funzione JetGetCursorInfo'
title: JetGetCursorInfo (funzione)
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319633"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="09fad-103">JetGetCursorInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="09fad-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="09fad-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="09fad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="09fad-105">JetGetCursorInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="09fad-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="09fad-106">La funzione **JetGetCursorInfo** viene utilizzata per determinare se un aggiornamento del record corrente di un cursore provocherà un conflitto di scrittura, in base allo stato corrente dell'aggiornamento del record.</span><span class="sxs-lookup"><span data-stu-id="09fad-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="09fad-107">È possibile che venga restituito un conflitto di scrittura anche se **JetGetCursorInfo** restituisce JET_errSuccess, perché un'altra sessione può aggiornare il record prima che la sessione corrente sia in grado di aggiornare lo stesso record.</span><span class="sxs-lookup"><span data-stu-id="09fad-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="09fad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09fad-108">Parameters</span></span>

<span data-ttu-id="09fad-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="09fad-109">*sesid*</span></span>

<span data-ttu-id="09fad-110">Sessione che verrà utilizzata per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="09fad-110">The session that will be used for this call.</span></span>

<span data-ttu-id="09fad-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="09fad-111">*tableid*</span></span>

<span data-ttu-id="09fad-112">Cursore che verrà utilizzato per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="09fad-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="09fad-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="09fad-113">*pvResult*</span></span>

<span data-ttu-id="09fad-114">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="09fad-114">Reserved for future use.</span></span>

<span data-ttu-id="09fad-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="09fad-115">*cbMax*</span></span>

<span data-ttu-id="09fad-116">Deve essere impostato su 0 (zero); in caso contrario, non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="09fad-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="09fad-117">È presente per le funzionalità future.</span><span class="sxs-lookup"><span data-stu-id="09fad-117">It is present for future functionality.</span></span>

<span data-ttu-id="09fad-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="09fad-118">*InfoLevel*</span></span>

<span data-ttu-id="09fad-119">Deve essere impostato su 0 (zero); in caso contrario, non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="09fad-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="09fad-120">È presente per le funzionalità future.</span><span class="sxs-lookup"><span data-stu-id="09fad-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="09fad-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09fad-121">Return Value</span></span>

<span data-ttu-id="09fad-122">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="09fad-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="09fad-123">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="09fad-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09fad-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="09fad-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="09fad-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09fad-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09fad-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="09fad-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="09fad-127">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="09fad-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="09fad-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="09fad-129">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="09fad-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fad-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="09fad-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="09fad-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="09fad-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="09fad-132">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09fad-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="09fad-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="09fad-134"><em>CbMax</em> è diverso da 0 (zero) o <em>InfoLevel</em> non è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="09fad-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fad-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="09fad-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="09fad-136">Il cursore non si trova attualmente in un record e le informazioni su un record logico non possono essere restituite come risultato.</span><span class="sxs-lookup"><span data-stu-id="09fad-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="09fad-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="09fad-138">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="09fad-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fad-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="09fad-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="09fad-140">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="09fad-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="09fad-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="09fad-142">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="09fad-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="09fad-143">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="09fad-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fad-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="09fad-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="09fad-145">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="09fad-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="09fad-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="09fad-147">Il record corrente del cursore è stato aggiornato da un'altra sessione e un aggiornamento del record da questa sessione provocherà un conflitto di scrittura.</span><span class="sxs-lookup"><span data-stu-id="09fad-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09fad-148">In seguito all'esito positivo, questa operazione non ha alcun effetto sulla posizione del cursore, ma indica che non è attualmente stato aggiornato da nessun'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="09fad-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="09fad-149">In caso di errore, se viene restituito un codice di errore negativo non sono presenti effetti sul cursore o sul database.</span><span class="sxs-lookup"><span data-stu-id="09fad-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="09fad-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="09fad-150">Remarks</span></span>

<span data-ttu-id="09fad-151">Questa operazione non influisce sullo stato del cursore o dei dati.</span><span class="sxs-lookup"><span data-stu-id="09fad-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="09fad-152">Restituisce solo un codice di errore che indica se un aggiornamento del record corrente da parte della sessione chiamante è noto come risultato di un JET_errWriteConflict o è sconosciuto per restituire JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="09fad-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="09fad-153">Se il record è già stato aggiornato da un'altra sessione per utilizzarlo, è certo che un aggiornamento del record da questa sessione provocherà un conflitto di scrittura.</span><span class="sxs-lookup"><span data-stu-id="09fad-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="09fad-154">Questa operazione sarà valida fino a quando questa sessione non eseguirà il commit o il rollback delle transazioni a livello di transazione 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="09fad-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="09fad-155">Tuttavia, se **JetGetCursorInfo** restituisce JET_errSuccess, è ancora possibile che un'altra sessione aggiorni questo record prima della sessione corrente e quindi è comunque possibile che un aggiornamento del record corrente da questa sessione nella transazione corrente provochi un conflitto di scrittura.</span><span class="sxs-lookup"><span data-stu-id="09fad-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="09fad-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09fad-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09fad-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="09fad-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="09fad-158">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="09fad-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="09fad-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="09fad-160">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="09fad-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fad-161"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="09fad-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="09fad-162">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="09fad-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09fad-163"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="09fad-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="09fad-164">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="09fad-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09fad-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="09fad-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="09fad-166">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="09fad-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="09fad-167">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="09fad-167">See Also</span></span>

[<span data-ttu-id="09fad-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="09fad-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="09fad-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="09fad-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="09fad-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="09fad-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="09fad-171">JetGetLock</span><span class="sxs-lookup"><span data-stu-id="09fad-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="09fad-172">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="09fad-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="09fad-173">JetStopService</span><span class="sxs-lookup"><span data-stu-id="09fad-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="09fad-174">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="09fad-174">JetUpdate</span></span>](./jetupdate-function.md)
