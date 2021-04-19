---
description: 'Altre informazioni su: funzione JetDupCursor'
title: Funzione JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317346"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="b5791-103">Funzione JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b5791-103">JetDupCursor Function</span></span>


<span data-ttu-id="b5791-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b5791-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="b5791-105">Funzione JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b5791-105">JetDupCursor Function</span></span>

<span data-ttu-id="b5791-106">La funzione **JetDupCursor** duplica un cursore aperto e restituisce un handle al cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="b5791-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="b5791-107">Se il cursore duplicato era un cursore di sola lettura, il cursore duplicato è anche un cursore di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b5791-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="b5791-108">Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="b5791-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="b5791-109">Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="b5791-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="b5791-110">Il cursore duplicato viene sempre aperto nell'indice cluster e il relativo percorso è sempre nella prima riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="b5791-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b5791-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5791-111">Parameters</span></span>

<span data-ttu-id="b5791-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b5791-112">*sesid*</span></span>

<span data-ttu-id="b5791-113">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b5791-113">The session to use for this call.</span></span>

<span data-ttu-id="b5791-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b5791-114">*tableid*</span></span>

<span data-ttu-id="b5791-115">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b5791-115">The cursor to use for this call.</span></span>

<span data-ttu-id="b5791-116">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="b5791-116">*ptableid*</span></span>

<span data-ttu-id="b5791-117">Puntatore a *TableID*.</span><span class="sxs-lookup"><span data-stu-id="b5791-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="b5791-118">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b5791-118">*grbit*</span></span>

<span data-ttu-id="b5791-119">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="b5791-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="b5791-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5791-120">Return Value</span></span>

<span data-ttu-id="b5791-121">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b5791-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b5791-122">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b5791-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5791-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b5791-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="b5791-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5791-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5791-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b5791-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b5791-126">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b5791-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5791-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b5791-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b5791-128">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b5791-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5791-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b5791-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b5791-130">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="b5791-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="b5791-131">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b5791-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5791-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b5791-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b5791-133">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="b5791-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5791-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="b5791-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="b5791-135">Non esistono risorse di cursore disponibili.</span><span class="sxs-lookup"><span data-stu-id="b5791-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5791-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b5791-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b5791-137">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="b5791-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5791-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b5791-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b5791-139">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="b5791-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="b5791-140">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b5791-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5791-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b5791-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b5791-142">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="b5791-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5791-143">In seguito all'esito positivo, *pTableID* è impostato su un cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="b5791-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="b5791-144">In caso di errore, non viene apportata alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="b5791-144">On failure, no changes are made.</span></span> <span data-ttu-id="b5791-145">Lo stato di *TableID* è invariato.</span><span class="sxs-lookup"><span data-stu-id="b5791-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b5791-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5791-146">Remarks</span></span>

<span data-ttu-id="b5791-147">Per il cursore duplicato non è stato copiato l'intero stato del cursore.</span><span class="sxs-lookup"><span data-stu-id="b5791-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="b5791-148">La posizione del cursore duplicato, incluso l'indice corrente, è in genere diversa dal cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="b5791-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="b5791-149">Il cursore duplicato viene sempre restituito nell'indice cluster e nella prima riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="b5791-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="b5791-150">Se la tabella è vuota, il cursore duplicato non si trova in nessuna riga.</span><span class="sxs-lookup"><span data-stu-id="b5791-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="b5791-151">Le tabelle aperte con **JetDupCursor** devono essere in genere chiuse con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5791-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="b5791-152">L'eccezione a questa regola si verifica quando **JetDupCursor** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="b5791-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="b5791-153">Quando si esegue il rollback di una transazione, il cursore viene chiuso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b5791-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="b5791-154">In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5791-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="b5791-155">Il numero di tabelle che è possibile aprire contemporaneamente è interessato direttamente da [JET_paramMaxOpenTables](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b5791-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="b5791-156">Per informazioni dettagliate, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="b5791-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b5791-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5791-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5791-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b5791-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5791-159">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b5791-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5791-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b5791-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5791-161">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b5791-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5791-162"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b5791-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5791-163">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b5791-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5791-164"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b5791-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b5791-165">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b5791-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5791-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b5791-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b5791-167">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b5791-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b5791-168">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b5791-168">See Also</span></span>

[<span data-ttu-id="b5791-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b5791-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b5791-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b5791-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b5791-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5791-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b5791-172">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b5791-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b5791-173">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b5791-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b5791-174">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b5791-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="b5791-175">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="b5791-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
