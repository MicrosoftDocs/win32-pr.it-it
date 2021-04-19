---
description: 'Altre informazioni su: funzione JetGetRecordSize2'
title: JetGetRecordSize2 (funzione)
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319631"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="caefb-103">JetGetRecordSize2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="caefb-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="caefb-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="caefb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="caefb-105">JetGetRecordSize2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="caefb-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="caefb-106">La funzione **JetGetRecordSize2** recupera le informazioni sulle dimensioni dei record dal percorso desiderato.</span><span class="sxs-lookup"><span data-stu-id="caefb-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="caefb-107">**Windows 7: JetGetRecordSize2** è stato introdotto nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="caefb-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="caefb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="caefb-108">Parameters</span></span>

<span data-ttu-id="caefb-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="caefb-109">*sesid*</span></span>

<span data-ttu-id="caefb-110">Identifica il contesto della sessione di database che verrà usato per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="caefb-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="caefb-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="caefb-111">*tableid*</span></span>

<span data-ttu-id="caefb-112">Identifica la tabella o il cursore che verrà usato per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="caefb-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="caefb-113">Il cursore deve essere posizionato su un record o avere preparato un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="caefb-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="caefb-114">*precsize*</span><span class="sxs-lookup"><span data-stu-id="caefb-114">*precsize*</span></span>

<span data-ttu-id="caefb-115">Puntatore a un buffer di output per la struttura [JET_RECSIZE2](./jet-recsize2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="caefb-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="caefb-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="caefb-116">*grbit*</span></span>

<span data-ttu-id="caefb-117">Si tratta di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="caefb-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caefb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="caefb-118">Value</span></span></p></th>
<th><p><span data-ttu-id="caefb-119">Significato</span><span class="sxs-lookup"><span data-stu-id="caefb-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caefb-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="caefb-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="caefb-121">Questo consente di recuperare le dimensioni del record che si trova nel buffer di copia preparato per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="caefb-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="caefb-122">In caso contrario, il <em>TableID</em> o il cursore deve essere posizionato su un record e tale record verrà usato.</span><span class="sxs-lookup"><span data-stu-id="caefb-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="caefb-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="caefb-124">Quando si specifica questo bit, il <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> non viene azzerato prima di compilare il contenuto, agendo efficacemente come un accumulo di statistiche per più record visitati o aggiornati.</span><span class="sxs-lookup"><span data-stu-id="caefb-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="caefb-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="caefb-126">In questo modo, l'API ignorerà i valori Long non intrinseci.</span><span class="sxs-lookup"><span data-stu-id="caefb-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="caefb-127">Ad esempio, verrà usato solo il record locale nella pagina.</span><span class="sxs-lookup"><span data-stu-id="caefb-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="caefb-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caefb-128">Return Value</span></span>

<span data-ttu-id="caefb-129">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="caefb-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="caefb-130">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="caefb-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caefb-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="caefb-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="caefb-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caefb-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caefb-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="caefb-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="caefb-134">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="caefb-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="caefb-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="caefb-136">Una delle opzioni richieste non è valida o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="caefb-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="caefb-137">Questo errore verrà restituito dalla funzione <strong>JetGetRecordSize2</strong> quando viene specificato un <em>grbit</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="caefb-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="caefb-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="caefb-139">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="caefb-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="caefb-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="caefb-141">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="caefb-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="caefb-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="caefb-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="caefb-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="caefb-144"><strong>Windows XP:  </strong> JET_errInstanceUnavailable verranno restituiti solo dal sistema operativo Windows XP e dalle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="caefb-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="caefb-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="caefb-146">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="caefb-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="caefb-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="caefb-148">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="caefb-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="caefb-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="caefb-150">Non è consentito usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="caefb-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="caefb-151"><strong>Windows XP:  </strong> JET_errInstanceUnavailable verranno restituiti solo da Windows XP e dalle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="caefb-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="caefb-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="caefb-153">Questo problema può verificarsi se il cursore è stato posizionato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="caefb-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="caefb-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="caefb-155">Se il cursore non è posizionato in una transazione, questo può verificarsi se un altro thread Elimina il record da questa sessione.</span><span class="sxs-lookup"><span data-stu-id="caefb-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="caefb-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="caefb-157">Può essere restituito se è stato passato un<em>Precsize</em> <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="caefb-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="caefb-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="caefb-158">Remarks</span></span>

<span data-ttu-id="caefb-159">La dimensione della chiave accumulata nel campo **cbOverhead** di [JET_RECSIZE2](./jet-recsize2-structure.md), è interessata dall'JET_bitRecordSizeInCopyBuffer.</span><span class="sxs-lookup"><span data-stu-id="caefb-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="caefb-160">Se viene specificato questo bit, le dimensioni della chiave accumulate nel campo **cbOverhead** sono le dimensioni della chiave completa.</span><span class="sxs-lookup"><span data-stu-id="caefb-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="caefb-161">Se questo bit non viene utilizzato, le dimensioni della chiave accumulate non includeranno alcuna dimensione salvata a causa della compressione del prefisso di chiave.</span><span class="sxs-lookup"><span data-stu-id="caefb-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="caefb-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caefb-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caefb-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="caefb-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="caefb-164">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="caefb-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="caefb-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="caefb-166">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="caefb-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-167"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="caefb-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="caefb-168">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="caefb-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caefb-169"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="caefb-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="caefb-170">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="caefb-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caefb-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="caefb-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="caefb-172">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="caefb-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="caefb-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="caefb-173">See Also</span></span>

[<span data-ttu-id="caefb-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="caefb-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="caefb-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="caefb-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="caefb-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="caefb-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="caefb-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="caefb-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="caefb-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="caefb-178">JET_TABLEID</span></span>](./jet-tableid.md)
