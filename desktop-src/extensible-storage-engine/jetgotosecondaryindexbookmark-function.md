---
description: 'Altre informazioni su: funzione JetGotoSecondaryIndexBookmark'
title: JetGotoSecondaryIndexBookmark (funzione)
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967651"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="708e0-103">JetGotoSecondaryIndexBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="708e0-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="708e0-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="708e0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="708e0-105">JetGotoSecondaryIndexBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="708e0-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="708e0-106">La funzione **JetGotoSecondaryIndexBookmark** posiziona un cursore in una voce di indice associata al segnalibro dell'indice secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="708e0-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="708e0-107">Il segnalibro dell'indice secondario deve essere usato con lo stesso indice nella stessa tabella da cui è stato originariamente recuperato.</span><span class="sxs-lookup"><span data-stu-id="708e0-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="708e0-108">Il segnalibro dell'indice secondario per una voce di indice può essere recuperato usando **JetGotoSecondaryIndexBookmark**.</span><span class="sxs-lookup"><span data-stu-id="708e0-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="708e0-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="708e0-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="708e0-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="708e0-110">Parameters</span></span>

<span data-ttu-id="708e0-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="708e0-111">*sesid*</span></span>

<span data-ttu-id="708e0-112">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="708e0-112">The session to use for this call.</span></span>

<span data-ttu-id="708e0-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="708e0-113">*tableid*</span></span>

<span data-ttu-id="708e0-114">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="708e0-114">The cursor to use for this call.</span></span>

<span data-ttu-id="708e0-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="708e0-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="708e0-116">Buffer contenente la chiave secondaria da utilizzare per posizionare il cursore.</span><span class="sxs-lookup"><span data-stu-id="708e0-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="708e0-117">*cbSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="708e0-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="708e0-118">Dimensione della chiave secondaria nel buffer.</span><span class="sxs-lookup"><span data-stu-id="708e0-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="708e0-119">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="708e0-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="708e0-120">Buffer che contiene il segnalibro della chiave primaria da utilizzare per posizionare il cursore.</span><span class="sxs-lookup"><span data-stu-id="708e0-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="708e0-121">*cbPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="708e0-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="708e0-122">Dimensioni del segnalibro della chiave primaria nel buffer.</span><span class="sxs-lookup"><span data-stu-id="708e0-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="708e0-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="708e0-123">*grbit*</span></span>

<span data-ttu-id="708e0-124">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="708e0-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="708e0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="708e0-125">Value</span></span></p></th>
<th><p><span data-ttu-id="708e0-126">Significato</span><span class="sxs-lookup"><span data-stu-id="708e0-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="708e0-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="708e0-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="708e0-128">Nel caso in cui non sia più possibile trovare la voce di indice, il cursore viene lasciato posizionato in corrispondenza del punto in cui è stata trovata in precedenza la voce di indice.</span><span class="sxs-lookup"><span data-stu-id="708e0-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="708e0-129">L'operazione avrà comunque esito negativo con JET_errRecordDeleted; Tuttavia, sarà possibile passare alla voce di indice successiva o precedente relativa alla voce di indice mancante.</span><span class="sxs-lookup"><span data-stu-id="708e0-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="708e0-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="708e0-130">Return Value</span></span>

<span data-ttu-id="708e0-131">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="708e0-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="708e0-132">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="708e0-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="708e0-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="708e0-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="708e0-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="708e0-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="708e0-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="708e0-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="708e0-136">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="708e0-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="708e0-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="708e0-138">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="708e0-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="708e0-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="708e0-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="708e0-140">Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="708e0-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="708e0-141"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="708e0-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="708e0-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="708e0-143">Il segnalibro dell'indice secondario specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="708e0-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="708e0-144">Questo errore potrebbe essersi verificato perché la chiave secondaria è zero oppure il puntatore del buffer della chiave secondaria è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="708e0-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="708e0-145">Questo errore si verifica perché</span><span class="sxs-lookup"><span data-stu-id="708e0-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="708e0-146">L'indice secondario corrente non ha un vincolo di univocità e le dimensioni del segnalibro fornito sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="708e0-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="708e0-147">Il puntatore del buffer del segnalibro è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="708e0-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="708e0-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="708e0-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="708e0-149">Il cursore non si trova attualmente in un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="708e0-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="708e0-150">Non è significativo passare a un segnalibro di indice secondario quando il cursore non usa attualmente un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="708e0-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="708e0-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve essere utilizzato quando il cursore non si trova in un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="708e0-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="708e0-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="708e0-153">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="708e0-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="708e0-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="708e0-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="708e0-155">Impossibile trovare la voce di indice associata al segnalibro dell'indice secondario.</span><span class="sxs-lookup"><span data-stu-id="708e0-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="708e0-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="708e0-157">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="708e0-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="708e0-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="708e0-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="708e0-159">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="708e0-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="708e0-160"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="708e0-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="708e0-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="708e0-162">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="708e0-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="708e0-163">Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice associata al segnalibro dell'indice secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="708e0-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="708e0-164">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="708e0-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="708e0-165">Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="708e0-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="708e0-166">Se è stata creata una chiave di ricerca per il cursore da usare, la chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="708e0-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="708e0-167">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="708e0-167">No change to the database state will occur.</span></span>

<span data-ttu-id="708e0-168">Se questa funzione ha esito negativo, la posizione del cursore rimane invariata a meno che non venga restituito JET_errRecordDeleted e JET_bitBookmarkPermitVirtualCurrency venga specificato.</span><span class="sxs-lookup"><span data-stu-id="708e0-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="708e0-169">In tal caso, il cursore verrà posizionato in corrispondenza del quale sarebbe stata la voce di indice associata al segnalibro dell'indice secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="708e0-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="708e0-170">Il cursore può essere spostato in relazione a tale posizione, ma non è ancora presente in una voce di indice valida.</span><span class="sxs-lookup"><span data-stu-id="708e0-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="708e0-171">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="708e0-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="708e0-172">Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="708e0-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="708e0-173">Se è stata creata una chiave di ricerca per il cursore da usare, la chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="708e0-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="708e0-174">In ogni caso, non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="708e0-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="708e0-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="708e0-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="708e0-176"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="708e0-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="708e0-177">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="708e0-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-178"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="708e0-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="708e0-179">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="708e0-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="708e0-180"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="708e0-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="708e0-181">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="708e0-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="708e0-182"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="708e0-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="708e0-183">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="708e0-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="708e0-184"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="708e0-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="708e0-185">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="708e0-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="708e0-186">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="708e0-186">See Also</span></span>

[<span data-ttu-id="708e0-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="708e0-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="708e0-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="708e0-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="708e0-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="708e0-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="708e0-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="708e0-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="708e0-191">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="708e0-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="708e0-192">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="708e0-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="708e0-193">JetStopService</span><span class="sxs-lookup"><span data-stu-id="708e0-193">JetStopService</span></span>](./jetstopservice-function.md)
