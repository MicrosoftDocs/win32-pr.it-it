---
description: 'Altre informazioni su: funzione JetEscrowUpdate'
title: Funzione JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316453"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="770ac-103">Funzione JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="770ac-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="770ac-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="770ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="770ac-105">Funzione JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="770ac-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="770ac-106">La funzione **JetEscrowUpdate** esegue un'operazione di addizione atomica su una colonna.</span><span class="sxs-lookup"><span data-stu-id="770ac-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="770ac-107">Questa funzione consente a più sessioni di aggiornare simultaneamente lo stesso record senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="770ac-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="770ac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="770ac-108">Parameters</span></span>

<span data-ttu-id="770ac-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="770ac-109">*sesid*</span></span>

<span data-ttu-id="770ac-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="770ac-110">The session to use for this call.</span></span>

<span data-ttu-id="770ac-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="770ac-111">*tableid*</span></span>

<span data-ttu-id="770ac-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="770ac-112">The cursor to use for this call.</span></span>

<span data-ttu-id="770ac-113">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="770ac-113">*columnid*</span></span>

<span data-ttu-id="770ac-114">*ColumnID* della colonna da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="770ac-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="770ac-115">*PV*</span><span class="sxs-lookup"><span data-stu-id="770ac-115">*pv*</span></span>

<span data-ttu-id="770ac-116">Puntatore a un buffer contenente Addend per la colonna.</span><span class="sxs-lookup"><span data-stu-id="770ac-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="770ac-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="770ac-117">*cbMax*</span></span>

<span data-ttu-id="770ac-118">Dimensioni del buffer che contiene Addend.</span><span class="sxs-lookup"><span data-stu-id="770ac-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="770ac-119">*pvOld*</span><span class="sxs-lookup"><span data-stu-id="770ac-119">*pvOld*</span></span>

<span data-ttu-id="770ac-120">Il buffer di output che riceverà il valore corrente della colonna archiviato nel database (il controllo delle versioni viene ignorato).</span><span class="sxs-lookup"><span data-stu-id="770ac-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="770ac-121">*cbOldMax*</span><span class="sxs-lookup"><span data-stu-id="770ac-121">*cbOldMax*</span></span>

<span data-ttu-id="770ac-122">Dimensione massima del buffer di output che riceverà il valore corrente della colonna.</span><span class="sxs-lookup"><span data-stu-id="770ac-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="770ac-123">Attualmente è supportata solo JET_coltypLong, quindi il buffer deve avere una lunghezza di 4 byte o di 0 byte.</span><span class="sxs-lookup"><span data-stu-id="770ac-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="770ac-124">Se *pvOld* è null, *cbOldMax* deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="770ac-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="770ac-125">*pcbOldActual*</span><span class="sxs-lookup"><span data-stu-id="770ac-125">*pcbOldActual*</span></span>

<span data-ttu-id="770ac-126">Riceve la quantità effettiva di dati del valore non elaborato ricevuti nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="770ac-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="770ac-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="770ac-127">*grbit*</span></span>

<span data-ttu-id="770ac-128">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="770ac-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="770ac-129">Valore</span><span class="sxs-lookup"><span data-stu-id="770ac-129">Value</span></span></p></th>
<th><p><span data-ttu-id="770ac-130">Significato</span><span class="sxs-lookup"><span data-stu-id="770ac-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="770ac-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="770ac-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="770ac-132">Anche se la sessione che esegue l'aggiornamento del deposito a garanzia ha il rollback della transazione, questo aggiornamento non verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="770ac-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="770ac-133">Si noti che, poiché è possibile che i record del log non vengano scaricati su disco, gli aggiornamenti del deposito recenti eseguiti con questo flag potrebbero andare persi in caso di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="770ac-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="770ac-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="770ac-134">Return Value</span></span>

<span data-ttu-id="770ac-135">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="770ac-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="770ac-136">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="770ac-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="770ac-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="770ac-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="770ac-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="770ac-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="770ac-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="770ac-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="770ac-140">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="770ac-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="770ac-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="770ac-142">Per il cursore è stato preparato un aggiornamento con <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="770ac-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="770ac-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="770ac-144">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="770ac-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="770ac-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="770ac-146">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="770ac-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="770ac-147">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="770ac-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="770ac-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="770ac-149">È stata passata una dimensione del buffer non valida.</span><span class="sxs-lookup"><span data-stu-id="770ac-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="770ac-150">Attualmente è supportata solo JET_coltypLong, quindi il buffer deve essere di 4 byte.</span><span class="sxs-lookup"><span data-stu-id="770ac-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="770ac-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="770ac-152">È stata specificata una colonna non valida.</span><span class="sxs-lookup"><span data-stu-id="770ac-152">An invalid column has been specified.</span></span> <span data-ttu-id="770ac-153">La colonna deve essere creata con JET_bitColumnEscrowUpdate specificato.</span><span class="sxs-lookup"><span data-stu-id="770ac-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="770ac-154">È possibile specificare solo colonne fisse di JET_coltypLong come aggiornabili con deposito.</span><span class="sxs-lookup"><span data-stu-id="770ac-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="770ac-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="770ac-156">Per aggiornare una colonna, è necessario che il cursore si trovi in un record.</span><span class="sxs-lookup"><span data-stu-id="770ac-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="770ac-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="770ac-158">Gli aggiornamenti del deposito possono essere eseguiti solo da sessioni in una transazione.</span><span class="sxs-lookup"><span data-stu-id="770ac-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="770ac-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="770ac-160">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="770ac-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="770ac-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="770ac-162">Il cursore non può essere di sola lettura e aggiornare un record.</span><span class="sxs-lookup"><span data-stu-id="770ac-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="770ac-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="770ac-164">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="770ac-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="770ac-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="770ac-166">Non è possibile usare la stessa sessione da più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="770ac-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="770ac-167">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="770ac-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="770ac-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="770ac-169">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="770ac-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="770ac-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="770ac-171">La sessione deve disporre delle autorizzazioni di scrittura per aggiornare un record.</span><span class="sxs-lookup"><span data-stu-id="770ac-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="770ac-173">Errore restituito quando viene richiesto un aggiornamento in conflitto.</span><span class="sxs-lookup"><span data-stu-id="770ac-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="770ac-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="770ac-174">Remarks</span></span>

<span data-ttu-id="770ac-175">In genere, se due sessioni tentano di aggiornare contemporaneamente un record, la seconda sessione riceverà un errore di JET_errWriteConflict, a meno che le sessioni non siano completamente serializzate.</span><span class="sxs-lookup"><span data-stu-id="770ac-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="770ac-176">Per serializzare due sessioni che aggiornano lo stesso record, la seconda sessione deve avviare la relativa transazione dopo che la prima transazione ha eseguito il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="770ac-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="770ac-177">Per ulteriori informazioni, vedere [JetBeginTransaction](./jetbegintransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="770ac-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="770ac-178">È possibile aggiornare più colonne nello stesso record.</span><span class="sxs-lookup"><span data-stu-id="770ac-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="770ac-179">Gli aggiornamenti non interessano.</span><span class="sxs-lookup"><span data-stu-id="770ac-179">The updates do not affect each other.</span></span>

<span data-ttu-id="770ac-180">Solo le operazioni **JetEscrowUpdate** sono compatibili tra loro.</span><span class="sxs-lookup"><span data-stu-id="770ac-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="770ac-181">Se due diverse sessioni tentano di preparare gli aggiornamenti o di eliminare lo stesso record, verrà generato un conflitto di scrittura.</span><span class="sxs-lookup"><span data-stu-id="770ac-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="770ac-182">Sessione B</span><span class="sxs-lookup"><span data-stu-id="770ac-182">Session B</span></span><br /><span data-ttu-id="770ac-183">
<strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="770ac-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span><span class="sxs-lookup"><span data-stu-id="770ac-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="770ac-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="770ac-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="770ac-186"><strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="770ac-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="770ac-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="770ac-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="770ac-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="770ac-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span><span class="sxs-lookup"><span data-stu-id="770ac-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="770ac-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="770ac-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="770ac-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-194">Sessione A</span><span class="sxs-lookup"><span data-stu-id="770ac-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="770ac-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="770ac-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="770ac-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="770ac-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="770ac-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="770ac-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="770ac-199">Le operazioni di deposito con versione vengono annullate con [JetRollback](./jetrollback-function.md) , a meno che non sia stato specificato JET_bitEscrowNoRollback.</span><span class="sxs-lookup"><span data-stu-id="770ac-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="770ac-200">**JetEscrowUpdate** restituisce il valore non elaborato della colonna archiviata nel database, perché un'applicazione potrebbe voler eseguire un'azione speciale quando viene raggiunto un valore sentinel.</span><span class="sxs-lookup"><span data-stu-id="770ac-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="770ac-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) restituisce la visualizzazione con versione corretta della colonna ignorando gli aggiornamenti effettuati dalle sessioni simultanee.</span><span class="sxs-lookup"><span data-stu-id="770ac-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="770ac-202">Date due sessioni che operano sulla stessa colonna dello stesso record, possiamo vedere come funziona.</span><span class="sxs-lookup"><span data-stu-id="770ac-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="770ac-203">Si supponga che la colonna inizi con un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="770ac-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="770ac-204">Sessione</span><span class="sxs-lookup"><span data-stu-id="770ac-204">Session</span></span></p></th>
<th><p><span data-ttu-id="770ac-205">Operazione</span><span class="sxs-lookup"><span data-stu-id="770ac-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="770ac-206">Valore archiviato</span><span class="sxs-lookup"><span data-stu-id="770ac-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="770ac-207">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="770ac-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="770ac-208">A</span><span class="sxs-lookup"><span data-stu-id="770ac-208">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="770ac-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-210">A</span><span class="sxs-lookup"><span data-stu-id="770ac-210">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="770ac-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-212">0</span><span class="sxs-lookup"><span data-stu-id="770ac-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-213">A</span><span class="sxs-lookup"><span data-stu-id="770ac-213">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-214"><strong>JetEscrowUpdate</strong> (4)</span><span class="sxs-lookup"><span data-stu-id="770ac-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="770ac-215">4</span><span class="sxs-lookup"><span data-stu-id="770ac-215">4</span></span></p></td>
<td><p><span data-ttu-id="770ac-216">0</span><span class="sxs-lookup"><span data-stu-id="770ac-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-217">A</span><span class="sxs-lookup"><span data-stu-id="770ac-217">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="770ac-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-219">4</span><span class="sxs-lookup"><span data-stu-id="770ac-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-220">B</span><span class="sxs-lookup"><span data-stu-id="770ac-220">B</span></span></p></td>
<td><p><span data-ttu-id="770ac-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span><span class="sxs-lookup"><span data-stu-id="770ac-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-222">B</span><span class="sxs-lookup"><span data-stu-id="770ac-222">B</span></span></p></td>
<td><p><span data-ttu-id="770ac-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="770ac-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-224">0</span><span class="sxs-lookup"><span data-stu-id="770ac-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-225">B</span><span class="sxs-lookup"><span data-stu-id="770ac-225">B</span></span></p></td>
<td><p><span data-ttu-id="770ac-226"><strong>JetEscrowUpdate</strong> (3)</span><span class="sxs-lookup"><span data-stu-id="770ac-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="770ac-227">7</span><span class="sxs-lookup"><span data-stu-id="770ac-227">7</span></span></p></td>
<td><p><span data-ttu-id="770ac-228">4</span><span class="sxs-lookup"><span data-stu-id="770ac-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-229">B</span><span class="sxs-lookup"><span data-stu-id="770ac-229">B</span></span></p></td>
<td><p><span data-ttu-id="770ac-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="770ac-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-231">3</span><span class="sxs-lookup"><span data-stu-id="770ac-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-232">A</span><span class="sxs-lookup"><span data-stu-id="770ac-232">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-233"><strong>JetEscrowUpdate</strong> (2)</span><span class="sxs-lookup"><span data-stu-id="770ac-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="770ac-234">9</span><span class="sxs-lookup"><span data-stu-id="770ac-234">9</span></span></p></td>
<td><p><span data-ttu-id="770ac-235">7</span><span class="sxs-lookup"><span data-stu-id="770ac-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-236">A</span><span class="sxs-lookup"><span data-stu-id="770ac-236">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-237"><strong>JetEscrowUpdate</strong> (-7)</span><span class="sxs-lookup"><span data-stu-id="770ac-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="770ac-238">2</span><span class="sxs-lookup"><span data-stu-id="770ac-238">2</span></span></p></td>
<td><p><span data-ttu-id="770ac-239">9</span><span class="sxs-lookup"><span data-stu-id="770ac-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-240">B</span><span class="sxs-lookup"><span data-stu-id="770ac-240">B</span></span></p></td>
<td><p><span data-ttu-id="770ac-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="770ac-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-242">3</span><span class="sxs-lookup"><span data-stu-id="770ac-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-243">A</span><span class="sxs-lookup"><span data-stu-id="770ac-243">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="770ac-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-245">-1</span><span class="sxs-lookup"><span data-stu-id="770ac-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-246">B</span><span class="sxs-lookup"><span data-stu-id="770ac-246">B</span></span></p></td>
<td><p><span data-ttu-id="770ac-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span><span class="sxs-lookup"><span data-stu-id="770ac-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="770ac-248">-1</span><span class="sxs-lookup"><span data-stu-id="770ac-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-249">A</span><span class="sxs-lookup"><span data-stu-id="770ac-249">A</span></span></p></td>
<td><p><span data-ttu-id="770ac-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="770ac-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="770ac-251">-1</span><span class="sxs-lookup"><span data-stu-id="770ac-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="770ac-252">La sostituzione di un record nella stessa transazione che esegue gli aggiornamenti del deposito a un record non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="770ac-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="770ac-253">In particolare, se un aggiornamento su un record viene preparato con una [JET_TABLEID](./jet-tableid.md) e un [JET_TABLEID](./jet-tableid.md) diverso viene usato per l'aggiornamento del record, il deposito verrà perso quando viene chiamato [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="770ac-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="770ac-254">Ciò si verifica anche se la colonna escrow non è stata impostata durante l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="770ac-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="770ac-255">Quando una colonna aggiornabile del deposito ha un valore pari a zero, è possibile attivare un comportamento speciale.</span><span class="sxs-lookup"><span data-stu-id="770ac-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="770ac-256">Questo comportamento si verifica solo se un'operazione **JetEscrowUpdate** fa sì che la colonna abbia un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="770ac-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="770ac-257">L'azione non viene eseguita immediatamente, ma si verifica talvolta dopo la transazione che ha causato la presenza di un valore pari a zero commit per la colonna.</span><span class="sxs-lookup"><span data-stu-id="770ac-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="770ac-258">La colonna deve avere ancora un valore pari a zero (ovvero se nessuna altra sessione ha modificato la colonna).</span><span class="sxs-lookup"><span data-stu-id="770ac-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="770ac-259">Se la colonna è stata creata con JET_bitColumnDeleteOnZero, il record contenente la colonna verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="770ac-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="770ac-260">Se la colonna è stata creata con JET_bitColumnFinalize, verrà emesso un callback.</span><span class="sxs-lookup"><span data-stu-id="770ac-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="770ac-261">Un arresto anomalo del sistema può causare la mancata verifica di queste azioni, ma la manutenzione in linea (tramite la funzione [JetDefragment](./jetdefragment-function.md) ) ripeterà correttamente le azioni.</span><span class="sxs-lookup"><span data-stu-id="770ac-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="770ac-262">Requisiti</span><span class="sxs-lookup"><span data-stu-id="770ac-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="770ac-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="770ac-264">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="770ac-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="770ac-266">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="770ac-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-267"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="770ac-268">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="770ac-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="770ac-269"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="770ac-270">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="770ac-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="770ac-271"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="770ac-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="770ac-272">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="770ac-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="770ac-273">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="770ac-273">See Also</span></span>

[<span data-ttu-id="770ac-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="770ac-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="770ac-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="770ac-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="770ac-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="770ac-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="770ac-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="770ac-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="770ac-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="770ac-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="770ac-279">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="770ac-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="770ac-280">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="770ac-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="770ac-281">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="770ac-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="770ac-282">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="770ac-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="770ac-283">JetRollback</span><span class="sxs-lookup"><span data-stu-id="770ac-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="770ac-284">JetStopService</span><span class="sxs-lookup"><span data-stu-id="770ac-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="770ac-285">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="770ac-285">JetUpdate</span></span>](./jetupdate-function.md)
