---
description: 'Altre informazioni su: funzione JetGetRecordPosition'
title: Funzione JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050112"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="9ba3d-103">Funzione JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="9ba3d-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="9ba3d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9ba3d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="9ba3d-105">Funzione JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="9ba3d-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="9ba3d-106">La funzione **JetGetRecordPosition** restituisce la posizione frazionaria del record corrente nell'indice corrente sotto forma di struttura [JET_RECPOS](./jet-recpos-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba3d-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="9ba3d-107">Questa struttura descrive le posizioni frazionarie in termini di numero approssimativo di voci di indice prima del record corrente e di un numero totale approssimativo di voci nell'indice.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="9ba3d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ba3d-108">Parameters</span></span>

<span data-ttu-id="9ba3d-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9ba3d-109">*sesid*</span></span>

<span data-ttu-id="9ba3d-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-110">The session to use for this call.</span></span>

<span data-ttu-id="9ba3d-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9ba3d-111">*tableid*</span></span>

<span data-ttu-id="9ba3d-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-112">The cursor to use for this call.</span></span>

<span data-ttu-id="9ba3d-113">*precpos*</span><span class="sxs-lookup"><span data-stu-id="9ba3d-113">*precpos*</span></span>

<span data-ttu-id="9ba3d-114">Descrizione della frazione da usare per ottenere la posizione del record corrente nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="9ba3d-115">*cbRecpos*</span><span class="sxs-lookup"><span data-stu-id="9ba3d-115">*cbRecpos*</span></span>

<span data-ttu-id="9ba3d-116">Dimensione della memoria allocata in *precpos*.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="9ba3d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ba3d-117">Return Value</span></span>

<span data-ttu-id="9ba3d-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9ba3d-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba3d-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ba3d-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9ba3d-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="9ba3d-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ba3d-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9ba3d-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ba3d-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9ba3d-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-125">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9ba3d-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-127">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ba3d-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9ba3d-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-129">Questa operazione non può essere completata perché l'istanza di associata alla sessione ha rilevato un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="9ba3d-130">È necessario che l'accesso a tutti i dati venga revocato per garantire la protezione dell'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9ba3d-131"><strong>Windows 2000:</strong>  Questo errore non verrà restituito dal sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9ba3d-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-133">Le dimensioni della memoria allocata in <em>precpos</em> non sono sufficienti.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ba3d-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9ba3d-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-135">Il cursore non si trova attualmente in un record e non può restituire una posizione.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9ba3d-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-137">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ba3d-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9ba3d-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-139">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9ba3d-140"><strong>Windows 2000:</strong>  Questo errore non verrà restituito dal sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9ba3d-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9ba3d-142">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ba3d-143">In seguito all'esito positivo, il numero approssimativo di voci di indice che precede il record corrente nell'indice viene restituito in precpos- \> centriesLT.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="9ba3d-144">1 viene restituito in precpos- \> centriesInRange.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="9ba3d-145">Il numero approssimativo di voci nell'indice viene restituito in precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="9ba3d-146">In caso di errore, non viene apportata alcuna modifica alla memoria allocata in *precpos*.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9ba3d-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ba3d-147">Remarks</span></span>

<span data-ttu-id="9ba3d-148">Questa operazione restituisce dati variabili quando gli aggiornamenti vengono eseguiti continuamente nella tabella.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="9ba3d-149">Le modifiche apportate ai valori non corrisponderanno sempre alle aspettative basate sulla conoscenza degli aggiornamenti, poiché i valori sono approssimazioni basate sulle proprietà fisiche dell'indice.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="9ba3d-150">L'isolamento transazionale non si applica alle posizioni da **JetGetRecordPosition** poiché i valori dipendono da proprietà fisiche dell'indice che non sono isolate dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="9ba3d-151">[JET_RECPOS](./jet-recpos-structure.md) non deve essere usato per descrivere un record all'interno di una tabella o per riposizionare un record vicino a un record esistente.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="9ba3d-152">Al contrario, è necessario recuperare i segnalibri per un record esistente e quindi utilizzarli per riposizionare lo stesso record.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9ba3d-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ba3d-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9ba3d-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9ba3d-155">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ba3d-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9ba3d-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9ba3d-157">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-158"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9ba3d-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9ba3d-159">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ba3d-160"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="9ba3d-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9ba3d-161">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ba3d-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9ba3d-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9ba3d-163">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9ba3d-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9ba3d-164">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9ba3d-164">See Also</span></span>

[<span data-ttu-id="9ba3d-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9ba3d-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9ba3d-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9ba3d-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9ba3d-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9ba3d-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9ba3d-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9ba3d-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9ba3d-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="9ba3d-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="9ba3d-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="9ba3d-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="9ba3d-171">JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="9ba3d-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="9ba3d-172">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9ba3d-172">JetStopService</span></span>](./jetstopservice-function.md)
