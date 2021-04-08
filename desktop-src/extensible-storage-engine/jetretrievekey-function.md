---
description: 'Altre informazioni su: funzione JetRetrieveKey'
title: Funzione JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058215"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="a3a85-103">Funzione JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="a3a85-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="a3a85-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a3a85-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="a3a85-105">Funzione JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="a3a85-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="a3a85-106">La funzione **JetRetrieveKey** recupera la chiave per la voce di indice in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="a3a85-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="a3a85-107">Tali chiavi vengono costruite mediante chiamate a [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="a3a85-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="a3a85-108">La chiave recuperata può quindi essere utilizzata per restituire in modo efficiente tale cursore alla stessa voce di indice mediante una chiamata a [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="a3a85-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a3a85-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3a85-109">Parameters</span></span>

<span data-ttu-id="a3a85-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a3a85-110">*sesid*</span></span>

<span data-ttu-id="a3a85-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a3a85-111">The session to use for this call.</span></span>

<span data-ttu-id="a3a85-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a3a85-112">*tableid*</span></span>

<span data-ttu-id="a3a85-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a3a85-113">The cursor to use for this call.</span></span>

<span data-ttu-id="a3a85-114">*pvData*</span><span class="sxs-lookup"><span data-stu-id="a3a85-114">*pvData*</span></span>

<span data-ttu-id="a3a85-115">Buffer di output che riceverà la chiave.</span><span class="sxs-lookup"><span data-stu-id="a3a85-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="a3a85-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="a3a85-116">*cbMax*</span></span>

<span data-ttu-id="a3a85-117">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a3a85-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="a3a85-118">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="a3a85-118">*pcbActual*</span></span>

<span data-ttu-id="a3a85-119">Riceve le dimensioni effettive, in byte, della chiave.</span><span class="sxs-lookup"><span data-stu-id="a3a85-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="a3a85-120">Se questo parametro è NULL, non verrà restituita la dimensione effettiva della chiave.</span><span class="sxs-lookup"><span data-stu-id="a3a85-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="a3a85-121">Se il buffer di output è troppo piccolo, verranno comunque restituite le dimensioni effettive della chiave.</span><span class="sxs-lookup"><span data-stu-id="a3a85-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="a3a85-122">Ciò significa che questo numero sarà maggiore della dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a3a85-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="a3a85-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a3a85-123">*grbit*</span></span>

<span data-ttu-id="a3a85-124">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3a85-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3a85-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a3a85-125">Value</span></span></p></th>
<th><p><span data-ttu-id="a3a85-126">Significato</span><span class="sxs-lookup"><span data-stu-id="a3a85-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="a3a85-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="a3a85-128">Quando viene specificato, il motore restituisce la chiave di ricerca per il cursore.</span><span class="sxs-lookup"><span data-stu-id="a3a85-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="a3a85-129">La chiave di ricerca viene compilata utilizzando una o più chiamate precedenti a <a href="gg269329(v=exchg.10).md">JetMakeKey</a> per la ricerca di tale chiave utilizzando <a href="gg294103(v=exchg.10).md">JetSeek</a> o l'impostazione di un intervallo di indici utilizzando <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span><span class="sxs-lookup"><span data-stu-id="a3a85-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a3a85-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3a85-130">Return Value</span></span>

<span data-ttu-id="a3a85-131">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="a3a85-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a3a85-132">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a85-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3a85-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a3a85-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="a3a85-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3a85-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a3a85-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a3a85-136">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a3a85-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a3a85-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a3a85-138">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a3a85-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a3a85-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a3a85-140">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="a3a85-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a3a85-141">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a3a85-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="a3a85-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="a3a85-143">Nessun tasto di ricerca corrente per il cursore.</span><span class="sxs-lookup"><span data-stu-id="a3a85-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="a3a85-144">Questa operazione viene eseguita per <strong>JetRetrieveKey</strong> se viene specificato JET_bitRetrieveCopy e non è stata creata una chiave di ricerca per questo cursore utilizzando una chiamata precedente a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="a3a85-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="a3a85-145">La chiave di ricerca verrà eliminata da una chiamata precedente a qualsiasi API di spostamento sul cursore diverso da <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="a3a85-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="a3a85-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="a3a85-147">Il cursore non è posizionato in corrispondenza di un record.</span><span class="sxs-lookup"><span data-stu-id="a3a85-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="a3a85-148">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="a3a85-148">This can happen for many different reasons.</span></span> <span data-ttu-id="a3a85-149">Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="a3a85-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a3a85-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a3a85-151">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="a3a85-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a3a85-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a3a85-153">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="a3a85-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a3a85-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a3a85-155">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="a3a85-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a3a85-156">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a3a85-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a3a85-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a3a85-158">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="a3a85-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="a3a85-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="a3a85-160">L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intera chiave.</span><span class="sxs-lookup"><span data-stu-id="a3a85-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="a3a85-161">Il buffer di output è stato riempito con la maggior parte della chiave.</span><span class="sxs-lookup"><span data-stu-id="a3a85-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="a3a85-162">Sono state restituite anche le dimensioni effettive della chiave, se richieste.</span><span class="sxs-lookup"><span data-stu-id="a3a85-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="a3a85-163"><strong>Nota</strong>   Se JET_bitRetrieveCopy è specificato, questo errore non verrà restituito.</span><span class="sxs-lookup"><span data-stu-id="a3a85-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="a3a85-164">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a3a85-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3a85-165">In seguito all'esito positivo, la chiave per la voce di indice in corrispondenza della posizione corrente di un cursore verrà restituita nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a3a85-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="a3a85-166">Se JET_wrnBufferTruncated viene restituito, il buffer di output conterrà la maggior parte della chiave che rientrerà nello spazio specificato e le dimensioni effettive della chiave saranno accurate.</span><span class="sxs-lookup"><span data-stu-id="a3a85-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="a3a85-167">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="a3a85-167">No change to the database state will occur.</span></span>

<span data-ttu-id="a3a85-168">In caso di errore, lo stato del buffer di output e le dimensioni effettive della chiave non saranno definiti.</span><span class="sxs-lookup"><span data-stu-id="a3a85-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="a3a85-169">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="a3a85-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a3a85-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3a85-170">Remarks</span></span>

<span data-ttu-id="a3a85-171">Generalmente, le chiavi devono essere considerate come blocchi opachi di dati.</span><span class="sxs-lookup"><span data-stu-id="a3a85-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="a3a85-172">Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati.</span><span class="sxs-lookup"><span data-stu-id="a3a85-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="a3a85-173">Tuttavia, le proprietà seguenti possono essere note su tutte le chiavi di ESENT:</span><span class="sxs-lookup"><span data-stu-id="a3a85-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="a3a85-174">Le chiavi possono essere confrontate tra loro tramite la funzione [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) per stabilire il relativo ordinamento nell'indice di origine sulla tabella delle voci dell'indice di origine.</span><span class="sxs-lookup"><span data-stu-id="a3a85-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="a3a85-175">Non è significativo confrontare le chiavi di voci di indice da indici diversi tra loro.</span><span class="sxs-lookup"><span data-stu-id="a3a85-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="a3a85-176">Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3a85-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="a3a85-177">In Windows Vista e versioni successive, le chiavi possono essere più grandi.</span><span class="sxs-lookup"><span data-stu-id="a3a85-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="a3a85-178">La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="a3a85-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="a3a85-179">Oltre alle proprietà precedenti delle chiavi di ESENT in generale, è importante notare che una chiave di ricerca è diversa dalla chiave per una voce di indice.</span><span class="sxs-lookup"><span data-stu-id="a3a85-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="a3a85-180">In particolare, una chiave di ricerca può essere più lunga di una chiave ordinaria.</span><span class="sxs-lookup"><span data-stu-id="a3a85-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="a3a85-181">Questa lunghezza aggiuntiva si verifica quando si usa un'opzione con caratteri jolly durante la costruzione della chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a3a85-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="a3a85-182">Per ulteriori informazioni, vedere [JetMakeKey](./jetmakekey-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a85-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="a3a85-183">In questa API è presente un bug importante presente in tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="a3a85-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="a3a85-184">Se la chiave di ricerca viene richiesta utilizzando l'utilizzo di JET_bitRetrieveCopy e il buffer di output è troppo piccolo per ricevere l'intera chiave, JET_wrnBufferTruncated non verrà restituito.</span><span class="sxs-lookup"><span data-stu-id="a3a85-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="a3a85-185">Viene invece restituito JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="a3a85-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="a3a85-186">È importante verificare che le dimensioni effettive della chiave restituite tramite *pcbActual* siano inferiori o uguali alla dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a3a85-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="a3a85-187">Se la dimensione effettiva è maggiore della dimensione del buffer di output, il chiamante di **JetRetrieveKey** deve reagire come se fosse stato restituito JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="a3a85-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a3a85-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3a85-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a3a85-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a3a85-190">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a3a85-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a3a85-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a3a85-192">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a3a85-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-193"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a3a85-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a3a85-194">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a3a85-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3a85-195"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a3a85-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a3a85-196">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a3a85-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3a85-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a3a85-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a3a85-198">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a3a85-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a3a85-199">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a3a85-199">See Also</span></span>

[<span data-ttu-id="a3a85-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a3a85-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a3a85-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a3a85-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a3a85-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a3a85-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a3a85-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a3a85-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a3a85-204">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="a3a85-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="a3a85-205">JetSeek</span><span class="sxs-lookup"><span data-stu-id="a3a85-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="a3a85-206">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="a3a85-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
