---
description: 'Altre informazioni su: funzione JetDelete'
title: Funzione JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315622"
---
# <a name="jetdelete-function"></a><span data-ttu-id="4c64c-103">Funzione JetDelete</span><span class="sxs-lookup"><span data-stu-id="4c64c-103">JetDelete Function</span></span>


<span data-ttu-id="4c64c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4c64c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="4c64c-105">Funzione JetDelete</span><span class="sxs-lookup"><span data-stu-id="4c64c-105">JetDelete Function</span></span>

<span data-ttu-id="4c64c-106">La funzione **JetDelete** Elimina il record corrente in una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="4c64c-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="4c64c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c64c-107">Parameters</span></span>

<span data-ttu-id="4c64c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4c64c-108">*sesid*</span></span>

<span data-ttu-id="4c64c-109">Contesto della sessione del database che verrà usato per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="4c64c-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="4c64c-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4c64c-110">*tableid*</span></span>

<span data-ttu-id="4c64c-111">Cursore su una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="4c64c-111">The cursor on a database table.</span></span> <span data-ttu-id="4c64c-112">La riga corrente verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="4c64c-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="4c64c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c64c-113">Return Value</span></span>

<span data-ttu-id="4c64c-114">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="4c64c-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4c64c-115">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="4c64c-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c64c-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4c64c-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="4c64c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c64c-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4c64c-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4c64c-119">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="4c64c-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="4c64c-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="4c64c-121">La funzione di callback ha avuto esito negativo in qualche modo.</span><span class="sxs-lookup"><span data-stu-id="4c64c-121">The callback function failed in some manner.</span></span> <span data-ttu-id="4c64c-122">Le violazioni di accesso nelle funzioni di callback, ad esempio, vengono rilevate e convertite in JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="4c64c-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="4c64c-123">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4c64c-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4c64c-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4c64c-125">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4c64c-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="4c64c-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="4c64c-127">Il cursore specificato da <em>TableID</em> non supporta l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="4c64c-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="4c64c-128">Vedere la sezione relativa alle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4c64c-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4c64c-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4c64c-130">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="4c64c-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4c64c-131">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4c64c-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="4c64c-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="4c64c-133">Il cursore specificato da <em>TableID</em> non si trova in un record.</span><span class="sxs-lookup"><span data-stu-id="4c64c-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4c64c-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4c64c-135">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="4c64c-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4c64c-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c64c-137">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="4c64c-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="4c64c-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="4c64c-139">Il motore di database non dispone di autorizzazioni sufficienti per eliminare il record.</span><span class="sxs-lookup"><span data-stu-id="4c64c-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="4c64c-140">Questo problema può verificarsi se il file di database è stato aperto con accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4c64c-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="4c64c-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="4c64c-142">Un buffer di aggiornamento (vedere <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) esiste, ma non è possibile eseguire il rollback di tutte le modifiche apportate alle colonne di tipo JET_coltypLongText e/o colonne di tipo JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="4c64c-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4c64c-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4c64c-144">Non è consentito usare la stessa sessione da più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="4c64c-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="4c64c-145">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4c64c-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4c64c-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4c64c-147">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="4c64c-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="4c64c-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4c64c-149">La transazione è di sola lettura e non supporta le eliminazioni.</span><span class="sxs-lookup"><span data-stu-id="4c64c-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="4c64c-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="4c64c-151">Operazione non riuscita perché la memoria disponibile non è sufficiente per mantenere le informazioni transazionali sull'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4c64c-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4c64c-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4c64c-153">Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4c64c-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="4c64c-154">Il tentativo di aggiornamento da questa sessione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4c64c-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c64c-155">In seguito all'esito positivo, la valuta viene lasciata immediatamente prima del record successivo.</span><span class="sxs-lookup"><span data-stu-id="4c64c-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="4c64c-156">Se il record eliminato era l'ultimo nella tabella, la valuta viene lasciata alla fine della tabella, ovvero dopo il nuovo record.</span><span class="sxs-lookup"><span data-stu-id="4c64c-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="4c64c-157">Se il record eliminato è l'unico record della tabella, la valuta viene impostata all'inizio.</span><span class="sxs-lookup"><span data-stu-id="4c64c-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="4c64c-158">Gli indici appropriati vengono aggiornati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4c64c-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="4c64c-159">Se un aggiornamento viene preparato (usando [JetPrepareUpdate](./jetprepareupdate-function.md)), verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="4c64c-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="4c64c-160">Il buffer di aggiornamento verrà reimpostato.</span><span class="sxs-lookup"><span data-stu-id="4c64c-160">The update buffer will be reset.</span></span>

<span data-ttu-id="4c64c-161">In caso di errore, la valuta rimane invariata.</span><span class="sxs-lookup"><span data-stu-id="4c64c-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="4c64c-162">Se un aggiornamento viene preparato (vedere [JetPrepareUpdate](./jetprepareupdate-function.md)), il buffer di aggiornamento potrebbe essere reimpostato.</span><span class="sxs-lookup"><span data-stu-id="4c64c-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4c64c-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c64c-163">Remarks</span></span>

<span data-ttu-id="4c64c-164">Non tutte le tabelle supportano l'eliminazione di righe.</span><span class="sxs-lookup"><span data-stu-id="4c64c-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="4c64c-165">Una tabella temporanea in genere non supporta l'eliminazione di righe.</span><span class="sxs-lookup"><span data-stu-id="4c64c-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="4c64c-166">L'eliminazione di record può essere abilitata nelle tabelle temporanee per diversi motivi, alcune delle quali sono:</span><span class="sxs-lookup"><span data-stu-id="4c64c-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="4c64c-167">JET_bitTTUpdatable specificato durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="4c64c-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="4c64c-168">Le tabelle temporanee di grandi dimensioni possono supportare l'eliminazione se sono state create con JET_bitTTScrollable o JET_bitTTIndexed.</span><span class="sxs-lookup"><span data-stu-id="4c64c-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="4c64c-169">La soglia in corrispondenza della quale una tabella temporanea diventa "large" è attualmente 64 kilobyte, ma potrebbe essere modificata nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="4c64c-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="4c64c-170">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4c64c-170">Windows XP and later.</span></span> <span data-ttu-id="4c64c-171">Le funzioni di callback possono essere richiamate da **JetDelete**, inclusi JET_cbtypBeforeDelete e JET_cbtypAfterDelete.</span><span class="sxs-lookup"><span data-stu-id="4c64c-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="4c64c-172">È importante comprendere l'effetto dell'esecuzione di un numero elevato di operazioni di aggiornamento all'interno di una singola transazione.</span><span class="sxs-lookup"><span data-stu-id="4c64c-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="4c64c-173">Ogni aggiornamento del database deve essere rilevato dal motore di database nell'archivio delle versioni.</span><span class="sxs-lookup"><span data-stu-id="4c64c-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="4c64c-174">L'archivio versione include un record live di tutte le diverse versioni di ogni voce di record o di indice nel database che possono essere visualizzate da tutte le transazioni attive.</span><span class="sxs-lookup"><span data-stu-id="4c64c-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="4c64c-175">Queste versioni vengono utilizzate per supportare il controllo della concorrenza multiversione utilizzato dal motore di database per supportare le transazioni mediante l'isolamento dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="4c64c-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="4c64c-176">Una volta che il motore di database ha esaurito le risorse usate per archiviare queste versioni, non può più accettare ulteriori modifiche fino a quando alcune transazioni non sono state terminate per consentire il ripristino di queste risorse.</span><span class="sxs-lookup"><span data-stu-id="4c64c-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="4c64c-177">Quando il motore è in questo stato, tutti gli aggiornamenti avranno esito negativo con JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="4c64c-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="4c64c-178">Le risorse disponibili per il motore di database per archiviare queste versioni possono essere controllate utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxVerPages* e *JET_paramGlobalMinVerPages*.</span><span class="sxs-lookup"><span data-stu-id="4c64c-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4c64c-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c64c-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-180"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4c64c-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4c64c-181">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4c64c-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-182"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4c64c-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4c64c-183">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4c64c-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-184"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="4c64c-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4c64c-185">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="4c64c-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c64c-186"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="4c64c-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4c64c-187">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4c64c-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c64c-188"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4c64c-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4c64c-189">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4c64c-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4c64c-190">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4c64c-190">See Also</span></span>

[<span data-ttu-id="4c64c-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4c64c-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4c64c-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4c64c-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4c64c-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4c64c-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4c64c-194">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="4c64c-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="4c64c-195">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="4c64c-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="4c64c-196">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="4c64c-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
