---
description: 'Altre informazioni su: funzione JetGetSecondaryIndexBookmark'
title: JetGetSecondaryIndexBookmark (funzione)
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313098"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="611b5-103">JetGetSecondaryIndexBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="611b5-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="611b5-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="611b5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="611b5-105">JetGetSecondaryIndexBookmark (funzione)</span><span class="sxs-lookup"><span data-stu-id="611b5-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="611b5-106">La funzione **JetGetSecondaryIndexBookmark** recupera un segnalibro speciale per la voce di indice secondaria in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="611b5-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="611b5-107">Questo segnalibro può quindi essere utilizzato per riposizionare in modo efficiente il cursore sulla stessa voce di indice utilizzando [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="611b5-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="611b5-108">Questa operazione è particolarmente utile quando si riposiziona in un indice secondario che contiene chiavi duplicate o che contiene più voci di indice per lo stesso record.</span><span class="sxs-lookup"><span data-stu-id="611b5-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="611b5-109">**Windows XP: JetGetSecondaryIndexBookmark** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="611b5-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="611b5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="611b5-110">Parameters</span></span>

<span data-ttu-id="611b5-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="611b5-111">*sesid*</span></span>

<span data-ttu-id="611b5-112">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="611b5-112">The session to use for this call.</span></span>

<span data-ttu-id="611b5-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="611b5-113">*tableid*</span></span>

<span data-ttu-id="611b5-114">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="611b5-114">The cursor to use for this call.</span></span>

<span data-ttu-id="611b5-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="611b5-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="611b5-116">Buffer di output che riceve la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="611b5-117">*cbSecondaryKeyMax*</span><span class="sxs-lookup"><span data-stu-id="611b5-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="611b5-118">Dimensione massima, in byte, del buffer di output per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="611b5-119">*pcbSecondaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="611b5-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="611b5-120">Riceve le dimensioni effettive, in byte, della chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="611b5-121">Se questo parametro è NULL, le dimensioni effettive della chiave secondaria non verranno restituite.</span><span class="sxs-lookup"><span data-stu-id="611b5-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="611b5-122">Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive della chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="611b5-123">Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="611b5-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="611b5-124">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="611b5-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="611b5-125">Buffer di output che riceve il segnalibro della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="611b5-126">*cbPrimaryBookmarkMax*</span><span class="sxs-lookup"><span data-stu-id="611b5-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="611b5-127">Dimensione massima, in byte, del buffer di output per il segnalibro della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="611b5-128">*pcbPrimaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="611b5-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="611b5-129">Riceve le dimensioni effettive, in byte, del segnalibro della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="611b5-130">Se questo parametro è NULL, non verranno restituite le dimensioni effettive del segnalibro della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="611b5-131">Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive del segnalibro della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="611b5-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="611b5-132">Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="611b5-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="611b5-133">*grbit*</span><span class="sxs-lookup"><span data-stu-id="611b5-133">*grbit*</span></span>

<span data-ttu-id="611b5-134">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="611b5-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="611b5-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="611b5-135">Return Value</span></span>

<span data-ttu-id="611b5-136">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="611b5-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="611b5-137">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="611b5-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="611b5-138">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="611b5-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="611b5-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="611b5-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="611b5-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="611b5-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="611b5-141">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="611b5-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="611b5-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="611b5-143">L'operazione è stata completata correttamente, ma uno dei buffer di output era troppo piccolo per ricevere i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="611b5-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="611b5-144">Il buffer di output è stato riempito con la maggior parte del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="611b5-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="611b5-145">Anche le dimensioni effettive del segnalibro sono state restituite, se richiesto.</span><span class="sxs-lookup"><span data-stu-id="611b5-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="611b5-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="611b5-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="611b5-147">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="611b5-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="611b5-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="611b5-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="611b5-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="611b5-150">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="611b5-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="611b5-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="611b5-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="611b5-152">Il cursore non si trova attualmente in un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="611b5-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="611b5-153">Non è significativo recuperare un segnalibro di indice secondario quando il cursore non sta attualmente usando un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="611b5-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="611b5-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> deve essere utilizzato quando il cursore non si trova in un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="611b5-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="611b5-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="611b5-156">Il cursore non è posizionato in corrispondenza di un record.</span><span class="sxs-lookup"><span data-stu-id="611b5-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="611b5-157">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="611b5-157">This can happen for many different reasons.</span></span> <span data-ttu-id="611b5-158">Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="611b5-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="611b5-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="611b5-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="611b5-160">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="611b5-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="611b5-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="611b5-162">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="611b5-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="611b5-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="611b5-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="611b5-164">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="611b5-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="611b5-165">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="611b5-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="611b5-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="611b5-167">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="611b5-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="611b5-168">In seguito all'esito positivo, il segnalibro dell'indice secondario per la voce di indice in corrispondenza della posizione corrente di un cursore verrà restituito nei buffer di output.</span><span class="sxs-lookup"><span data-stu-id="611b5-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="611b5-169">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="611b5-169">No change to the database state will occur.</span></span>

<span data-ttu-id="611b5-170">In caso di errore, lo stato dei buffer di output e le dimensioni effettive del segnalibro dell'indice secondario saranno indefiniti a meno che non venga restituito JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="611b5-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="611b5-171">Nel caso in cui venga restituito JET_errBufferTooSmall, i buffer di output conterranno la maggior parte del segnalibro dell'indice secondario che rientrerà nello spazio fornito e le dimensioni effettive del segnalibro dell'indice secondario saranno accurate.</span><span class="sxs-lookup"><span data-stu-id="611b5-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="611b5-172">In ogni caso, non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="611b5-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="611b5-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="611b5-173">Remarks</span></span>

<span data-ttu-id="611b5-174">In genere i segnalibri devono essere trattati come blocchi opachi di dati.</span><span class="sxs-lookup"><span data-stu-id="611b5-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="611b5-175">Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati.</span><span class="sxs-lookup"><span data-stu-id="611b5-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="611b5-176">Tuttavia, le proprietà seguenti possono essere note su tutti i segnalibri ESENT:</span><span class="sxs-lookup"><span data-stu-id="611b5-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="611b5-177">Un segnalibro identifica in modo univoco un record in una tabella specificata.</span><span class="sxs-lookup"><span data-stu-id="611b5-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="611b5-178">Il segnalibro di un record non viene modificato per la durata di tale record.</span><span class="sxs-lookup"><span data-stu-id="611b5-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="611b5-179">Il segnalibro di un record corrisponde alla chiave di tale record nell'indice primario della tabella che contiene il record.</span><span class="sxs-lookup"><span data-stu-id="611b5-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="611b5-180">Se non viene definito alcun indice primario su tale tabella, il motore di database creerà il proprio segnalibro per il record.</span><span class="sxs-lookup"><span data-stu-id="611b5-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="611b5-181">I segnalibri possono essere confrontati tra loro usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice primario sulla tabella dei record di origine.</span><span class="sxs-lookup"><span data-stu-id="611b5-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="611b5-182">Se non viene definito alcun indice primario su tale tabella, l'ordine relativo dei segnalibri da tale tabella non è significativo.</span><span class="sxs-lookup"><span data-stu-id="611b5-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="611b5-183">Non è significativo confrontare i segnalibri dei record di tabelle diverse tra loro.</span><span class="sxs-lookup"><span data-stu-id="611b5-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="611b5-184">Un segnalibro è sempre minore o uguale a JET_cbBookmarkMost (256) byte di lunghezza prima di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="611b5-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="611b5-185">In Windows Vista e versioni successive, i segnalibri possono essere più grandi.</span><span class="sxs-lookup"><span data-stu-id="611b5-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="611b5-186">La dimensione massima di un segnalibro è uguale al valore corrente di JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="611b5-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="611b5-187">Generalmente, le chiavi devono essere considerate come blocchi opachi di dati.</span><span class="sxs-lookup"><span data-stu-id="611b5-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="611b5-188">Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati.</span><span class="sxs-lookup"><span data-stu-id="611b5-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="611b5-189">Tuttavia, le proprietà seguenti possono essere note su tutte le chiavi di ESENT:</span><span class="sxs-lookup"><span data-stu-id="611b5-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="611b5-190">Le chiavi possono essere confrontate tra loro utilizzando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire l'ordine relativo nell'indice di origine sulla tabella delle voci dell'indice di origine.</span><span class="sxs-lookup"><span data-stu-id="611b5-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="611b5-191">Non è significativo confrontare le chiavi di voci di indice da indici diversi tra loro.</span><span class="sxs-lookup"><span data-stu-id="611b5-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="611b5-192">Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="611b5-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="611b5-193">In Windows Vista e versioni successive, le chiavi possono essere più grandi.</span><span class="sxs-lookup"><span data-stu-id="611b5-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="611b5-194">La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="611b5-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="611b5-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="611b5-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="611b5-196"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="611b5-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="611b5-197">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="611b5-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="611b5-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="611b5-199">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="611b5-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="611b5-200"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="611b5-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="611b5-201">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="611b5-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="611b5-202"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="611b5-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="611b5-203">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="611b5-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="611b5-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="611b5-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="611b5-205">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="611b5-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="611b5-206">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="611b5-206">See Also</span></span>

[<span data-ttu-id="611b5-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="611b5-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="611b5-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="611b5-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="611b5-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="611b5-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="611b5-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="611b5-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="611b5-211">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="611b5-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="611b5-212">JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="611b5-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="611b5-213">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="611b5-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="611b5-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="611b5-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
