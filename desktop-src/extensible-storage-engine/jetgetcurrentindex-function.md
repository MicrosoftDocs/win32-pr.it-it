---
description: 'Altre informazioni su: funzione JetGetCurrentIndex'
title: JetGetCurrentIndex (funzione)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315071"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="27408-103">JetGetCurrentIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="27408-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="27408-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="27408-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="27408-105">JetGetCurrentIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="27408-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="27408-106">La funzione **JetGetCurrentIndex** determina il nome dell'indice corrente di un determinato cursore.</span><span class="sxs-lookup"><span data-stu-id="27408-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="27408-107">Questo nome viene usato anche per riselezionare in seguito l'indice come indice corrente usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="27408-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="27408-108">Può essere usato anche per individuare le proprietà dell'indice usando [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="27408-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="27408-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="27408-109">Parameters</span></span>

<span data-ttu-id="27408-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="27408-110">*sesid*</span></span>

<span data-ttu-id="27408-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="27408-111">The session to use for this call.</span></span>

<span data-ttu-id="27408-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="27408-112">*tableid*</span></span>

<span data-ttu-id="27408-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="27408-113">The cursor to use for this call.</span></span>

<span data-ttu-id="27408-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="27408-114">*szIndexName*</span></span>

<span data-ttu-id="27408-115">Buffer di output che riceve il nome dell'indice corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="27408-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="27408-116">*cchIndexName*</span><span class="sxs-lookup"><span data-stu-id="27408-116">*cchIndexName*</span></span>

<span data-ttu-id="27408-117">Dimensione massima in caratteri del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="27408-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="27408-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27408-118">Return Value</span></span>

<span data-ttu-id="27408-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="27408-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="27408-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="27408-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27408-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="27408-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="27408-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27408-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27408-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="27408-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="27408-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="27408-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="27408-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="27408-126">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="27408-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27408-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="27408-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="27408-128">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="27408-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="27408-129">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="27408-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="27408-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="27408-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="27408-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27408-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="27408-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="27408-133">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="27408-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="27408-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="27408-135">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="27408-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="27408-136">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="27408-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27408-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="27408-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="27408-138">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="27408-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="27408-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="27408-140">L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intero nome di indice.</span><span class="sxs-lookup"><span data-stu-id="27408-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="27408-141">Il buffer di output è stato riempito con la maggior parte del nome di indice.</span><span class="sxs-lookup"><span data-stu-id="27408-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="27408-142">Se il buffer di output è di almeno un carattere di lunghezza, la stringa in tale buffer di output sarà terminata con null.</span><span class="sxs-lookup"><span data-stu-id="27408-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="27408-143"><strong>Nota  </strong> Questo errore non viene restituito se cchIndexName è zero.</span><span class="sxs-lookup"><span data-stu-id="27408-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="27408-144">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="27408-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27408-145">In seguito all'esito positivo, il nome dell'indice corrente del cursore specificato verrà restituito nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="27408-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="27408-146">Se JET_wrnBufferTruncated viene restituito, il buffer di output conterrà la maggior parte del nome dell'indice che rientrerà nello spazio fornito.</span><span class="sxs-lookup"><span data-stu-id="27408-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="27408-147">Se il buffer di output è di almeno un carattere di lunghezza, la stringa restituita in tale buffer sarà terminata con null.</span><span class="sxs-lookup"><span data-stu-id="27408-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="27408-148">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="27408-148">No change to the database state will occur.</span></span>

<span data-ttu-id="27408-149">In caso di errore, lo stato del buffer di output sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="27408-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="27408-150">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="27408-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="27408-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="27408-151">Remarks</span></span>

<span data-ttu-id="27408-152">Se non è presente alcun indice corrente per il cursore, verrà restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="27408-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="27408-153">Questo problema può verificarsi quando il cursore si trova nell'indice cluster della tabella e non è stato definito alcun indice primario.</span><span class="sxs-lookup"><span data-stu-id="27408-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="27408-154">Questo indice è noto come indice sequenziale della tabella e non ha alcuna definizione.</span><span class="sxs-lookup"><span data-stu-id="27408-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="27408-155">In ogni caso, l'impostazione dell'indice corrente su una stringa vuota utilizzando [JetSetCurrentIndex](./jetsetcurrentindex-function.md) consente di selezionare l'indice cluster indipendentemente dalla presenza di una definizione di indice primario.</span><span class="sxs-lookup"><span data-stu-id="27408-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="27408-156">In questa funzione è presente un bug importante presente in tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="27408-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="27408-157">Se il buffer di output è troppo piccolo per ricevere l'intero nome di indice e il buffer di output è di almeno un carattere di lunghezza, JET_wrnBufferTruncated non verrà restituito.</span><span class="sxs-lookup"><span data-stu-id="27408-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="27408-158">Viene invece restituito JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="27408-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="27408-159">Per evitare questo problema, il buffer di output deve contenere sempre almeno JET_cbNameMost + 1 (65) caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="27408-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="27408-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27408-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27408-161"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="27408-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="27408-162">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="27408-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="27408-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="27408-164">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="27408-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27408-165"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="27408-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="27408-166">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="27408-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-167"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="27408-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="27408-168">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="27408-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27408-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="27408-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="27408-170">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="27408-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27408-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="27408-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="27408-172">Implementato come <strong>JetGetCurrentIndexW</strong> (Unicode) e <strong>JetGetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="27408-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="27408-173">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="27408-173">See Also</span></span>

[<span data-ttu-id="27408-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="27408-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="27408-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="27408-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="27408-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="27408-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="27408-177">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="27408-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="27408-178">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="27408-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
