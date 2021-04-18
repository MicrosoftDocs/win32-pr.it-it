---
description: 'Altre informazioni su: funzione JetIndexRecordCount'
title: JetIndexRecordCount (funzione)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524966"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="d7ea5-103">JetIndexRecordCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="d7ea5-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="d7ea5-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d7ea5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="d7ea5-105">JetIndexRecordCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="d7ea5-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="d7ea5-106">La funzione **JetIndexRecordCount** conta il numero di voci nell'indice corrente dalla posizione corrente in poi.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="d7ea5-107">La posizione corrente è inclusa nel conteggio.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-107">The current position is included in the count.</span></span> <span data-ttu-id="d7ea5-108">Il conteggio può essere maggiore del numero totale di record nella tabella se l'indice corrente è su una colonna multivalore e le istanze della colonna hanno più valori.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="d7ea5-109">Se la tabella è vuota, verrà restituito 0 per il conteggio.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="d7ea5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7ea5-110">Parameters</span></span>

<span data-ttu-id="d7ea5-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d7ea5-111">*sesid*</span></span>

<span data-ttu-id="d7ea5-112">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-112">The session to use for this call.</span></span>

<span data-ttu-id="d7ea5-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d7ea5-113">*tableid*</span></span>

<span data-ttu-id="d7ea5-114">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-114">The cursor to use for this call.</span></span>

<span data-ttu-id="d7ea5-115">*pcrec*</span><span class="sxs-lookup"><span data-stu-id="d7ea5-115">*pcrec*</span></span>

<span data-ttu-id="d7ea5-116">Puntatore a un valore long senza segno per la ricezione del conteggio.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="d7ea5-117">*crecMax*</span><span class="sxs-lookup"><span data-stu-id="d7ea5-117">*crecMax*</span></span>

<span data-ttu-id="d7ea5-118">Numero massimo di record da contare.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-118">The maximum number of records to count.</span></span> <span data-ttu-id="d7ea5-119">Il valore 0 di *crecMax* indica che il conteggio è illimitato.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="d7ea5-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7ea5-120">Return Value</span></span>

<span data-ttu-id="d7ea5-121">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d7ea5-122">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ea5-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7ea5-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d7ea5-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="d7ea5-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7ea5-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d7ea5-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-126">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ea5-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d7ea5-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-128">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d7ea5-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-130">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d7ea5-131"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ea5-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d7ea5-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-133">Il cursore non si trova attualmente in un record e la tabella non è vuota.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="d7ea5-134"><strong>Windows XP, Windows server 2003, windows 2000 Server e windows 2000 Professional:</strong>  Se il cursore è posizionato in corrispondenza di un indice o di un intervallo di indici vuoti, <strong>JetIndexRecordCount</strong> restituisce erroneamente JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d7ea5-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ea5-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d7ea5-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-138">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d7ea5-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-140">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d7ea5-141"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ea5-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d7ea5-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d7ea5-143">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d7ea5-144">Se questa funzione ha esito positivo, il numero esatto di voci di indice, inclusa la posizione corrente e fino a *crecMax* (se non è 0), viene restituito nella lunghezza senza segno a cui punta *pcrec*.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="d7ea5-145">Se questa funzione ha esito negativo, non viene apportata alcuna modifica alla memoria allocata in *precpos*.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d7ea5-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7ea5-146">Remarks</span></span>

<span data-ttu-id="d7ea5-147">Se la tabella non è vuota, il cursore deve essere posizionato sul record dal quale iniziare il conteggio.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="d7ea5-148">Il conteggio includerà questo record e verrà conteggiato fino al limite specificato in *crecMax*.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="d7ea5-149">Se *crecMax* è 0, l'operazione continuerà a contare fino alla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="d7ea5-150">Gli intervalli di indice possono essere utilizzati per creare limitazioni di fine Indice artificiali per il conteggio.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="d7ea5-151">In questo modo, è possibile conteggiare esattamente intervalli secondari di un indice.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="d7ea5-152">Il cursore deve essere posizionato sulla prima riga nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="d7ea5-153">È necessario impostare la fine della chiave di intervallo, quindi utilizzare [JetSetIndexRange](./jetsetindexrange-function.md) per impostare l'intervallo superiore, in modo inclusivo o esclusivo.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="d7ea5-154">Infine, è necessario chiamare **JetIndexRecordCount** per contare esattamente l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="d7ea5-155">**JetIndexRecordCount** rispetta la semantica delle transazioni e restituisce un conteggio accurato per questa particolare sessione nello stato transazionale corrente.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="d7ea5-156">**JetIndexRecordCount** accede alle pagine foglia dell'indice per conteggiare esattamente le voci.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="d7ea5-157">Di conseguenza, può eseguire una grande quantità di operazioni di I/O e può essere lenta.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="d7ea5-158">Per evitare un carico eccessivo, è necessario utilizzare la limitazione *crecMax* .</span><span class="sxs-lookup"><span data-stu-id="d7ea5-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="d7ea5-159">Se un intervallo è di grandi dimensioni, potrebbe essere possibile contare l'intervallo in modo approssimativo usando [JetGetRecordPosition](./jetgetrecordposition-function.md).</span><span class="sxs-lookup"><span data-stu-id="d7ea5-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="d7ea5-160">**Windows XP, Windows server 2003, windows 2000 Server e windows 2000 Professional:**  Se il cursore è posizionato in corrispondenza di un indice o di un intervallo di indici vuoti, **JetIndexRecordCount** restituisce erroneamente JET_errNoCurrentRecord anziché restituire un numero di record pari a zero.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="d7ea5-161">L'applicazione deve verificare se l'indice o l'intervallo di indici è vuoto in questo caso.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d7ea5-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7ea5-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d7ea5-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d7ea5-164">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ea5-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d7ea5-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d7ea5-166">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-167"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="d7ea5-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d7ea5-168">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7ea5-169"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="d7ea5-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d7ea5-170">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7ea5-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d7ea5-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d7ea5-172">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d7ea5-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d7ea5-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d7ea5-173">See Also</span></span>

[<span data-ttu-id="d7ea5-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d7ea5-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d7ea5-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d7ea5-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d7ea5-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d7ea5-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d7ea5-177">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="d7ea5-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="d7ea5-178">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d7ea5-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="d7ea5-179">JetStopService</span><span class="sxs-lookup"><span data-stu-id="d7ea5-179">JetStopService</span></span>](./jetstopservice-function.md)
