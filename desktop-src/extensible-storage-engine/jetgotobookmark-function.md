---
description: 'Altre informazioni su: funzione JetGotoBookmark'
title: JetGotoBookmark (funzione)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318090"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="1fae3-103">JetGotoBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="1fae3-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="1fae3-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1fae3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="1fae3-105">JetGotoBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="1fae3-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="1fae3-106">La funzione **JetGotoBookmark** posiziona un cursore in una voce di indice per il record associato al segnalibro specificato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="1fae3-107">Il segnalibro può essere utilizzato con qualsiasi indice definito in una tabella.</span><span class="sxs-lookup"><span data-stu-id="1fae3-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="1fae3-108">Il segnalibro per un record può essere recuperato usando [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="1fae3-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="1fae3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fae3-109">Parameters</span></span>

<span data-ttu-id="1fae3-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1fae3-110">*sesid*</span></span>

<span data-ttu-id="1fae3-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1fae3-111">The session to use for this call.</span></span>

<span data-ttu-id="1fae3-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1fae3-112">*tableid*</span></span>

<span data-ttu-id="1fae3-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1fae3-113">The cursor to use for this call.</span></span>

<span data-ttu-id="1fae3-114">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="1fae3-114">*pvBookmark*</span></span>

<span data-ttu-id="1fae3-115">Buffer che contiene il segnalibro da utilizzare per posizionare il cursore.</span><span class="sxs-lookup"><span data-stu-id="1fae3-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="1fae3-116">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="1fae3-116">*cbBookmark*</span></span>

<span data-ttu-id="1fae3-117">Dimensioni del segnalibro nel buffer.</span><span class="sxs-lookup"><span data-stu-id="1fae3-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="1fae3-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fae3-118">Return Value</span></span>

<span data-ttu-id="1fae3-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="1fae3-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1fae3-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1fae3-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fae3-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1fae3-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="1fae3-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fae3-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1fae3-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1fae3-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="1fae3-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1fae3-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1fae3-126">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="1fae3-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1fae3-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1fae3-128">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="1fae3-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1fae3-129"><strong>Windows XP:</strong>   Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1fae3-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="1fae3-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="1fae3-131">Il segnalibro fornito non è valido.</span><span class="sxs-lookup"><span data-stu-id="1fae3-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="1fae3-132">Questa situazione potrebbe essersi verificata perché le dimensioni del segnalibro sono pari a zero oppure il puntatore del buffer del segnalibro è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="1fae3-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="1fae3-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="1fae3-134">Il cursore si trova in un indice secondario e non è stata trovata alcuna voce di indice per il record associato al segnalibro.</span><span class="sxs-lookup"><span data-stu-id="1fae3-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1fae3-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1fae3-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="1fae3-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="1fae3-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="1fae3-138">Impossibile trovare il record associato al segnalibro.</span><span class="sxs-lookup"><span data-stu-id="1fae3-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1fae3-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1fae3-140">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1fae3-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1fae3-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1fae3-142">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="1fae3-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1fae3-143"><strong>Windows XP:</strong>   Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1fae3-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1fae3-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1fae3-145">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="1fae3-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1fae3-146">Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice per il record associato al segnalibro specificato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="1fae3-147">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="1fae3-148">Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="1fae3-149">Se è stata creata una chiave di ricerca per il cursore, tale chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="1fae3-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="1fae3-150">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="1fae3-150">No change to the database state will occur.</span></span>

<span data-ttu-id="1fae3-151">Se questa funzione ha esito negativo, la posizione del cursore rimarrà invariata.</span><span class="sxs-lookup"><span data-stu-id="1fae3-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="1fae3-152">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="1fae3-153">Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="1fae3-154">Se è stata creata una chiave di ricerca per il cursore, tale chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="1fae3-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="1fae3-155">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="1fae3-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1fae3-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fae3-156">Remarks</span></span>

<span data-ttu-id="1fae3-157">Esistono due modi per utilizzare un segnalibro per posizionare un cursore su un indice.</span><span class="sxs-lookup"><span data-stu-id="1fae3-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="1fae3-158">Il primo consiste nell'usare il segnalibro per posizionare direttamente il record.</span><span class="sxs-lookup"><span data-stu-id="1fae3-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="1fae3-159">Questo errore si verifica quando l'indice corrente del cursore è l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="1fae3-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="1fae3-160">Questa tecnica funziona perché un segnalibro ESENT è uguale alla chiave primaria del record associato.</span><span class="sxs-lookup"><span data-stu-id="1fae3-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="1fae3-161">Il secondo modo per usare un segnalibro è posizionarlo in una voce in un indice secondario che corrisponde al record associato a tale segnalibro.</span><span class="sxs-lookup"><span data-stu-id="1fae3-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="1fae3-162">Durante questo processo, il motore cerca il record effettivo utilizzando il segnalibro nell'indice primario.</span><span class="sxs-lookup"><span data-stu-id="1fae3-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="1fae3-163">USA quindi i dati del record e la definizione dell'indice secondario per calcolare una chiave nell'indice secondario che punta al record.</span><span class="sxs-lookup"><span data-stu-id="1fae3-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="1fae3-164">Quindi posiziona il cursore sulla voce di indice per tale chiave.</span><span class="sxs-lookup"><span data-stu-id="1fae3-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="1fae3-165">Se il cursore si trova attualmente in un indice secondario su una o più colonne chiave multivalore, il cursore verrà posizionato sulla voce di indice corrispondente al primo multivalore di ognuna di queste colonne chiave.</span><span class="sxs-lookup"><span data-stu-id="1fae3-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1fae3-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fae3-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1fae3-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1fae3-168">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1fae3-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1fae3-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1fae3-170">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1fae3-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-171"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1fae3-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1fae3-172">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1fae3-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fae3-173"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1fae3-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1fae3-174">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1fae3-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fae3-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1fae3-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1fae3-176">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1fae3-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1fae3-177">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1fae3-177">See Also</span></span>

[<span data-ttu-id="1fae3-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1fae3-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1fae3-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1fae3-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1fae3-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1fae3-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1fae3-181">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="1fae3-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)
