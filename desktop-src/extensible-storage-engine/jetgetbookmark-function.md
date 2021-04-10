---
description: 'Altre informazioni su: funzione JetGetBookmark'
title: JetGetBookmark (funzione)
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131962"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="075a9-103">JetGetBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="075a9-103">JetGetBookmark Function</span></span>


<span data-ttu-id="075a9-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="075a9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="075a9-105">JetGetBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="075a9-105">JetGetBookmark Function</span></span>

<span data-ttu-id="075a9-106">La funzione **JetGetBookmark** Recupera il segnalibro per il record associato alla voce di indice in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="075a9-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="075a9-107">Questo segnalibro può quindi essere utilizzato per riposizionare il cursore sullo stesso record utilizzando [JetGoToBookmark](./jetgotobookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="075a9-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="075a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="075a9-108">Parameters</span></span>

<span data-ttu-id="075a9-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="075a9-109">*sesid*</span></span>

<span data-ttu-id="075a9-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="075a9-110">The session to use for this call.</span></span>

<span data-ttu-id="075a9-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="075a9-111">*tableid*</span></span>

<span data-ttu-id="075a9-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="075a9-112">The cursor to use for this call.</span></span>

<span data-ttu-id="075a9-113">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="075a9-113">*pvBookmark*</span></span>

<span data-ttu-id="075a9-114">Buffer di output che riceve il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="075a9-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="075a9-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="075a9-115">*cbMax*</span></span>

<span data-ttu-id="075a9-116">Dimensione massima, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="075a9-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="075a9-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="075a9-117">*pcbActual*</span></span>

<span data-ttu-id="075a9-118">Dimensioni effettive, in byte, del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="075a9-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="075a9-119">Se questo parametro è **null** , le dimensioni effettive del segnalibro non verranno restituite.</span><span class="sxs-lookup"><span data-stu-id="075a9-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="075a9-120">Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="075a9-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="075a9-121">Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="075a9-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="075a9-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="075a9-122">Return Value</span></span>

<span data-ttu-id="075a9-123">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="075a9-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="075a9-124">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="075a9-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="075a9-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="075a9-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="075a9-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="075a9-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="075a9-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="075a9-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="075a9-128">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="075a9-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="075a9-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="075a9-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="075a9-130">L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intero segnalibro.</span><span class="sxs-lookup"><span data-stu-id="075a9-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="075a9-131">Il buffer di output è stato riempito con la maggior parte del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="075a9-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="075a9-132">Anche le dimensioni effettive del segnalibro sono state restituite, se richiesto.</span><span class="sxs-lookup"><span data-stu-id="075a9-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="075a9-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="075a9-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="075a9-134">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="075a9-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="075a9-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="075a9-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="075a9-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="075a9-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="075a9-137"><strong>Windows XP:  </strong> Questi valori restituiti sono introdotti in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="075a9-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="075a9-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="075a9-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="075a9-139">Il cursore non è posizionato in corrispondenza di un record.</span><span class="sxs-lookup"><span data-stu-id="075a9-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="075a9-140">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="075a9-140">This can happen for many different reasons.</span></span> <span data-ttu-id="075a9-141">Questa situazione si verifica, ad esempio, se il cursore è posizionato dopo l'ultimo record nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="075a9-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="075a9-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="075a9-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="075a9-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="075a9-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="075a9-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="075a9-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="075a9-145">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="075a9-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="075a9-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="075a9-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="075a9-147">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="075a9-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="075a9-148"><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="075a9-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="075a9-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="075a9-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="075a9-150">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="075a9-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="075a9-151">Se questa funzione ha esito positivo, nel buffer di output verrà restituito il segnalibro per il record associato alla voce di indice in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="075a9-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="075a9-152">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="075a9-152">No change to the database state will occur.</span></span>

<span data-ttu-id="075a9-153">Se questa funzione ha esito negativo, lo stato del buffer di output e le dimensioni effettive del segnalibro saranno indefiniti a meno che non venga restituito JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="075a9-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="075a9-154">Nel caso in cui venga restituito JET_errBufferTooSmall, il buffer di output conterrà la maggior parte del segnalibro che rientrerà nello spazio fornito e le dimensioni effettive del segnalibro saranno accurate.</span><span class="sxs-lookup"><span data-stu-id="075a9-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="075a9-155">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="075a9-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="075a9-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="075a9-156">Remarks</span></span>

<span data-ttu-id="075a9-157">In genere i segnalibri devono essere trattati come blocchi opachi di dati.</span><span class="sxs-lookup"><span data-stu-id="075a9-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="075a9-158">Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati.</span><span class="sxs-lookup"><span data-stu-id="075a9-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="075a9-159">Tuttavia, le condizioni seguenti sono vere per tutti i segnalibri ESENT:</span><span class="sxs-lookup"><span data-stu-id="075a9-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="075a9-160">Un segnalibro identifica in modo univoco un record in una tabella specificata.</span><span class="sxs-lookup"><span data-stu-id="075a9-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="075a9-161">Il segnalibro di un record non viene modificato per la durata di tale record.</span><span class="sxs-lookup"><span data-stu-id="075a9-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="075a9-162">Il segnalibro di un record corrisponde alla chiave di tale record nell'indice primario della tabella che contiene il record.</span><span class="sxs-lookup"><span data-stu-id="075a9-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="075a9-163">Se nella tabella non è definito alcun indice primario, il motore di database creerà il proprio segnalibro per il record.</span><span class="sxs-lookup"><span data-stu-id="075a9-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="075a9-164">I segnalibri possono essere confrontati tra loro tramite la funzione [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice primario sulla tabella dei record di origine.</span><span class="sxs-lookup"><span data-stu-id="075a9-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="075a9-165">Se non viene definito alcun indice primario su tale tabella, non è significativo utilizzare l'ordinamento relativo dei segnalibri della tabella.</span><span class="sxs-lookup"><span data-stu-id="075a9-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="075a9-166">Non è significativo confrontare i segnalibri dei record di tabelle diverse tra loro.</span><span class="sxs-lookup"><span data-stu-id="075a9-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="075a9-167">Un segnalibro è sempre minore o uguale a JET_cbBookmarkMost (256) byte di lunghezza, prima di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="075a9-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="075a9-168">**Windows Vista:** In Windows Vista e versioni successive, i segnalibri possono essere più grandi di JET_cbBookmarkMost (256) byte.</span><span class="sxs-lookup"><span data-stu-id="075a9-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="075a9-169">La dimensione massima di un segnalibro è uguale al valore corrente di JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="075a9-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="075a9-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="075a9-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="075a9-171"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="075a9-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="075a9-172">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="075a9-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="075a9-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="075a9-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="075a9-174">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="075a9-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="075a9-175"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="075a9-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="075a9-176">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="075a9-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="075a9-177"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="075a9-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="075a9-178">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="075a9-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="075a9-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="075a9-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="075a9-180">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="075a9-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="075a9-181">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="075a9-181">See Also</span></span>

[<span data-ttu-id="075a9-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="075a9-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="075a9-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="075a9-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="075a9-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="075a9-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="075a9-185">JetGoToBookmark</span><span class="sxs-lookup"><span data-stu-id="075a9-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="075a9-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="075a9-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="075a9-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="075a9-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
