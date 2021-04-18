---
description: 'Altre informazioni su: funzione JetPrepareUpdate'
title: JetPrepareUpdate (funzione)
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319176"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="ee461-103">JetPrepareUpdate (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee461-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="ee461-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee461-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="ee461-105">JetPrepareUpdate (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee461-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="ee461-106">La funzione **JetPrepareUpdate** è la prima operazione di esecuzione di un aggiornamento, allo scopo di inserire un nuovo record o di sostituire un record esistente con nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="ee461-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="ee461-107">Gli aggiornamenti vengono eseguiti chiamando **JetPrepareUpdate**, quindi chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) zero o più volte e infine chiamando [JetUpdate](./jetupdate-function.md) per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ee461-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="ee461-108">**JetPrepareUpdate** e [JetUpdate](./jetupdate-function.md) impostano i limiti per un'operazione di aggiornamento e sono importanti per avere solo lo stato di aggiornamento finale di un record immesso negli indici.</span><span class="sxs-lookup"><span data-stu-id="ee461-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="ee461-109">Questa operazione è più efficiente, ma anche obbligatoria nei casi in cui i dati devono corrispondere a uno stato valido tramite più di un'operazione set Column.</span><span class="sxs-lookup"><span data-stu-id="ee461-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="ee461-110">Sono disponibili diverse opzioni per l'inserimento o la sostituzione dei record, che sono descritte in dettaglio di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee461-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="ee461-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee461-111">Parameters</span></span>

<span data-ttu-id="ee461-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ee461-112">*sesid*</span></span>

<span data-ttu-id="ee461-113">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="ee461-113">The session to use for this call.</span></span>

<span data-ttu-id="ee461-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="ee461-114">*tableid*</span></span>

<span data-ttu-id="ee461-115">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="ee461-115">The cursor to use for this call.</span></span>

<span data-ttu-id="ee461-116">*Prep*</span><span class="sxs-lookup"><span data-stu-id="ee461-116">*prep*</span></span>

<span data-ttu-id="ee461-117">Opzioni che possono essere utilizzate per preparare un aggiornamento, incluse le seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee461-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee461-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ee461-118">Value</span></span></p></th>
<th><p><span data-ttu-id="ee461-119">Significato</span><span class="sxs-lookup"><span data-stu-id="ee461-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee461-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="ee461-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="ee461-121">Questo flag fa in modo che <strong>JetPrepareUpdate</strong> annulli l'aggiornamento per questo cursore.</span><span class="sxs-lookup"><span data-stu-id="ee461-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="ee461-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="ee461-123">Questo flag determina la preparazione del cursore per l'inserimento di un nuovo record.</span><span class="sxs-lookup"><span data-stu-id="ee461-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="ee461-124">Tutti i dati vengono inizializzati sullo stato predefinito per il record.</span><span class="sxs-lookup"><span data-stu-id="ee461-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="ee461-125">Se la tabella include una colonna con incremento automatico, a questo record viene assegnato un nuovo valore indipendentemente dal fatto che l'aggiornamento abbia esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ee461-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="ee461-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="ee461-127">Questo flag determina la preparazione del cursore per l'inserimento di una copia del record esistente.</span><span class="sxs-lookup"><span data-stu-id="ee461-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="ee461-128">Se viene utilizzata questa opzione, deve essere presente un record corrente.</span><span class="sxs-lookup"><span data-stu-id="ee461-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="ee461-129">Lo stato iniziale del nuovo record viene copiato dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="ee461-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="ee461-130">I valori Long archiviati in modalità non registrata vengono copiati virtualmente.</span><span class="sxs-lookup"><span data-stu-id="ee461-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="ee461-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="ee461-132">Questo flag determina la preparazione del cursore per un inserimento dello stesso record e per l'eliminazione o il record originale.</span><span class="sxs-lookup"><span data-stu-id="ee461-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="ee461-133">Viene utilizzato nei casi in cui la chiave primaria è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="ee461-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="ee461-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="ee461-135">Questo flag determina la preparazione del cursore per la sostituzione del record corrente.</span><span class="sxs-lookup"><span data-stu-id="ee461-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="ee461-136">Se la tabella contiene una colonna versione, la colonna Version viene impostata sul valore successivo nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="ee461-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="ee461-137">Se l'aggiornamento non viene completato, il valore della versione nel record non sarà interessato.</span><span class="sxs-lookup"><span data-stu-id="ee461-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="ee461-138">Viene assunto un blocco di aggiornamento sul record per impedire ad altre sessioni di aggiornare questo record prima del completamento della sessione.</span><span class="sxs-lookup"><span data-stu-id="ee461-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="ee461-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="ee461-140">Questo flag è simile a JET_prepReplace, ma non viene effettuato alcun blocco per impedire ad altre sessioni di aggiornare questo record.</span><span class="sxs-lookup"><span data-stu-id="ee461-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="ee461-141">Questa sessione può invece ricevere JET_errWriteConflict quando chiama <a href="gg269288(v=exchg.10).md">JetUpdate</a> per completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee461-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ee461-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee461-142">Return Value</span></span>

<span data-ttu-id="ee461-143">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ee461-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ee461-144">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ee461-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee461-145">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ee461-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="ee461-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee461-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee461-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ee461-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ee461-148">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ee461-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="ee461-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="ee461-150"><strong>JetPrepareUpdate</strong> è stato chiamato con un flag valido per la preparazione ma non JET_prepCancel e il cursore si trovava già nello stato preparato.</span><span class="sxs-lookup"><span data-stu-id="ee461-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ee461-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ee461-152">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ee461-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ee461-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ee461-154">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="ee461-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ee461-155">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee461-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ee461-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ee461-157">Il flag di preparazione specificato non è un flag valido.</span><span class="sxs-lookup"><span data-stu-id="ee461-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ee461-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ee461-159">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="ee461-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="ee461-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ee461-161"><strong>JetPrepareUpdate</strong> è stato chiamato per sostituire un record con colonne SLV.</span><span class="sxs-lookup"><span data-stu-id="ee461-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="ee461-162">Colonne SLV.</span><span class="sxs-lookup"><span data-stu-id="ee461-162">SLV columns.</span></span> <span data-ttu-id="ee461-163">Si noti che le colonne SLV sono una funzionalità non destinata all'utilizzo generale.</span><span class="sxs-lookup"><span data-stu-id="ee461-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="ee461-164">Questa funzionalità viene utilizzata per supportare l'infrastruttura di Microsoft Exchange e non deve essere utilizzata nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee461-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ee461-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ee461-166">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="ee461-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="ee461-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="ee461-168"><strong>JetPrepareUpdate</strong> è stato chiamato con JET_prepCancel ma non è stato possibile eseguire il rollback di tutte le modifiche apportate alle colonne di tipo JET_coltypLongText e/o alle colonne di tipo JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="ee461-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ee461-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ee461-170">Non è possibile usare questo flag con la stessa sessione da più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="ee461-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="ee461-171">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee461-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ee461-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ee461-173">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="ee461-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="ee461-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="ee461-175"><strong>JetPrepareUpdate</strong> è stato chiamato con JET_prepCancel ma il cursore non si trovava nello stato preparato.</span><span class="sxs-lookup"><span data-stu-id="ee461-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee461-176">In caso di esito positivo, il cursore viene impostato sullo stato preparato per lo scopo dell'aggiornamento desiderato o, nel caso di JET_prepCancel, il cursore viene ripristinato allo stato non preparato e tutte le modifiche vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="ee461-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="ee461-177">In caso di errore, lo stato del cursore viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="ee461-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="ee461-178">Se l'errore è stato JET_errRollbackError, lo stato del cursore viene modificato nello stato non preparato, ma non tutte le modifiche sono state ripristinate.</span><span class="sxs-lookup"><span data-stu-id="ee461-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ee461-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee461-179">Remarks</span></span>

<span data-ttu-id="ee461-180">L'inserimento di una copia di un record è un'ottimizzazione importante quando i record condividono dati di tipo JET_coltypLongText e/o JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="ee461-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="ee461-181">Questi dati vengono archiviati in modalità non registrata quando è grande ed è possibile che più record condividano la stessa rappresentazione fisica dei dati.</span><span class="sxs-lookup"><span data-stu-id="ee461-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="ee461-182">In questo caso, i dati possono essere aggiornati da uno dei due record, ma in questo modo i dati verranno incrementati in modo tale che ogni record disponga di una propria copia.</span><span class="sxs-lookup"><span data-stu-id="ee461-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="ee461-183">Non è possibile modificare i dati in un record mediante una modifica da un altro record.</span><span class="sxs-lookup"><span data-stu-id="ee461-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="ee461-184">Non è inoltre possibile bloccare un aggiornamento di un record tramite un aggiornamento di un altro record.</span><span class="sxs-lookup"><span data-stu-id="ee461-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="ee461-185">Si tratta di una funzionalità centrale di ESE ed è nota come blocco a livello di record.</span><span class="sxs-lookup"><span data-stu-id="ee461-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="ee461-186">Le operazioni [JetUpdate](./jetupdate-function.md) che non riescono lasciano il cursore nello stato preparato per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee461-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="ee461-187">Questo consente la correzione ad alcuni errori, ad esempio un valore di colonna errato, senza che sia necessario ricreare lo stato di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee461-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="ee461-188">Ciò significa che in tutti i casi in cui un cursore abbandona un aggiornamento, deve chiamare in modo esplicito **JetPrepareUpdate** con JET_prepCancel.</span><span class="sxs-lookup"><span data-stu-id="ee461-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ee461-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee461-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee461-190"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ee461-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee461-191">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ee461-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-192"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ee461-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee461-193">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ee461-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-194"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ee461-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee461-195">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ee461-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee461-196"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ee461-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ee461-197">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ee461-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee461-198"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ee461-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ee461-199">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ee461-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ee461-200">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ee461-200">See Also</span></span>

[<span data-ttu-id="ee461-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ee461-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ee461-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ee461-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ee461-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ee461-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ee461-204">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="ee461-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="ee461-205">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="ee461-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="ee461-206">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="ee461-206">JetUpdate</span></span>](./jetupdate-function.md)
