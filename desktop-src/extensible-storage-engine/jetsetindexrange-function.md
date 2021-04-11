---
description: 'Altre informazioni su: funzione JetSetIndexRange'
title: Funzione JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226249"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="a1b56-103">Funzione JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="a1b56-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="a1b56-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a1b56-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="a1b56-105">Funzione JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="a1b56-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="a1b56-106">La funzione **JetSetIndexRange** limita temporaneamente il set di voci di indice che il cursore può utilizzare [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e termina in corrispondenza della voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e ai criteri associati specificati.</span><span class="sxs-lookup"><span data-stu-id="a1b56-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="a1b56-107">È necessario che una chiave di ricerca sia stata costruita in precedenza usando [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="a1b56-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a1b56-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1b56-108">Parameters</span></span>

<span data-ttu-id="a1b56-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a1b56-109">*sesid*</span></span>

<span data-ttu-id="a1b56-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-110">The session to use for this call.</span></span>

<span data-ttu-id="a1b56-111">*tableidSrc*</span><span class="sxs-lookup"><span data-stu-id="a1b56-111">*tableidSrc*</span></span>

<span data-ttu-id="a1b56-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-112">The cursor to use for this call.</span></span>

<span data-ttu-id="a1b56-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a1b56-113">*grbit*</span></span>

<span data-ttu-id="a1b56-114">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1b56-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1b56-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b56-115">Value</span></span></p></th>
<th><p><span data-ttu-id="a1b56-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a1b56-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="a1b56-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="a1b56-118">Questa presenza o assenza di questa opzione indica i criteri limite dell'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="a1b56-119">Quando è presente, questa opzione indica che il limite dell'intervallo di indici è incluso.</span><span class="sxs-lookup"><span data-stu-id="a1b56-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="a1b56-120">Se assente, questa opzione indica che il limite dell'intervallo di indici è esclusivo.</span><span class="sxs-lookup"><span data-stu-id="a1b56-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="a1b56-121">Quando il limite dell'intervallo di indici è incluso, le voci di indice che corrispondono esattamente ai criteri di ricerca sono incluse nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a1b56-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="a1b56-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="a1b56-123">Questa opzione richiede che l'intervallo di indici venga rimosso non appena è stato stabilito.</span><span class="sxs-lookup"><span data-stu-id="a1b56-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="a1b56-124">Tutti gli altri aspetti dell'operazione restano invariati.</span><span class="sxs-lookup"><span data-stu-id="a1b56-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="a1b56-125">Questa operazione è utile per verificare l'esistenza di voci di indice che corrispondono ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1b56-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="a1b56-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="a1b56-127">Questa opzione richiede che un intervallo di indice esistente nel cursore venga annullato.</span><span class="sxs-lookup"><span data-stu-id="a1b56-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="a1b56-128">Una volta annullato l'intervallo di indici, sarà possibile passare oltre la fine dell'intervallo di indici utilizzando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="a1b56-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="a1b56-129">Se non è già attivo un intervallo di indici, <strong>JetSetIndexRange</strong> avrà esito negativo con JET_errInvalidOperation.</span><span class="sxs-lookup"><span data-stu-id="a1b56-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="a1b56-130">Quando si specifica questa opzione, tutte le altre opzioni vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="a1b56-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="a1b56-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="a1b56-132">Se si utilizza questa opzione, la chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina alla fine dell'indice che corrisponderà all'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="a1b56-133">L'intervallo di indici verrà stabilito tra la posizione corrente del cursore e questa voce di indice, in modo che tutte le corrispondenze possano essere individuate procedendo in avanti sull'indice utilizzando <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MoveNext o un offset positivo.</span><span class="sxs-lookup"><span data-stu-id="a1b56-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="a1b56-134">Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine all'inizio dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a1b56-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="a1b56-135">Se questa opzione viene omessa, la chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina all'inizio dell'indice che corrisponderà all'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="a1b56-136">L'intervallo di indici verrà stabilito tra la posizione corrente del cursore e questa voce di indice, in modo che tutte le corrispondenze possano essere rilevate tornando indietro sull'indice utilizzando <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MovePrevious o un offset negativo.</span><span class="sxs-lookup"><span data-stu-id="a1b56-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="a1b56-137">Non è significativo omettere questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine alla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a1b56-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a1b56-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1b56-138">Return Value</span></span>

<span data-ttu-id="a1b56-139">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="a1b56-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a1b56-140">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b56-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1b56-141">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a1b56-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="a1b56-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1b56-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a1b56-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a1b56-144">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a1b56-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="a1b56-145">Per <strong>JetSetIndexRange</strong>, ciò significa che un intervallo di indici esistente è stato annullato o che è presente almeno una voce di indice all'interno dell'intervallo di indice.</span><span class="sxs-lookup"><span data-stu-id="a1b56-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a1b56-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a1b56-147">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a1b56-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a1b56-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a1b56-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="a1b56-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a1b56-150">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a1b56-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="a1b56-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="a1b56-152">Questo errore viene restituito da <strong>JetSetIndexRange</strong> quando JET_bitRangeRemove è stato specificato e non è attivo alcun intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="a1b56-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="a1b56-154">Nessun tasto di ricerca corrente per il cursore.</span><span class="sxs-lookup"><span data-stu-id="a1b56-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="a1b56-155"><strong>JetSetIndexRange</strong> richiede che il cursore disponga di una chiave di ricerca valida perché verrà utilizzata per i criteri di ricerca utilizzati per individuare le voci dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a1b56-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="a1b56-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="a1b56-157">Nessun indice corrente per il cursore.</span><span class="sxs-lookup"><span data-stu-id="a1b56-157">There is no current index for the cursor.</span></span> <span data-ttu-id="a1b56-158">Questo problema si verifica per <strong>JetSetIndexRange</strong> se il cursore si trova nell'indice cluster di una tabella, non è stato definito un indice primario.</span><span class="sxs-lookup"><span data-stu-id="a1b56-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="a1b56-159">L'impostazione di un intervallo di indice su un indice di questo tipo non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="a1b56-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="a1b56-161">Questo errore viene restituito da <strong>JetSetIndexRange</strong> per indicare che non sono presenti voci di indice nell'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a1b56-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a1b56-163">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a1b56-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1b56-165">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="a1b56-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a1b56-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a1b56-167">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="a1b56-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a1b56-168">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a1b56-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a1b56-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1b56-170">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1b56-171">In caso di esito positivo, se viene specificato JET_bitRangeRemove, l'intervallo di indici attualmente in vigore viene annullato.</span><span class="sxs-lookup"><span data-stu-id="a1b56-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="a1b56-172">Se JET_bitRangeRemove non è specificato e viene specificato JET_bitRangeInstantDuration, non è attivo alcun intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="a1b56-173">Se non viene specificato né JET_bitRangeRemove né JET_bitRangeInstantDuration, viene applicato un nuovo intervallo di indice.</span><span class="sxs-lookup"><span data-stu-id="a1b56-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="a1b56-174">Questo intervallo di indici limita temporaneamente il set di voci di indice che il cursore può utilizzare [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e termina in corrispondenza della voce di indice corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1b56-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="a1b56-175">La posizione del cursore rimarrà invariata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="a1b56-176">Se è stata creata una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="a1b56-177">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="a1b56-177">No change to the database state will occur.</span></span>

<span data-ttu-id="a1b56-178">In caso di errore, se non viene restituito JET_errNoCurrentRecord, non è attivo alcun intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="a1b56-179">Se viene restituito JET_errNoCurrentRecord, viene applicato un nuovo intervallo di indice.</span><span class="sxs-lookup"><span data-stu-id="a1b56-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="a1b56-180">Questo intervallo di indici limita temporaneamente il set di voci di indice che il cursore può utilizzare [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e termina in corrispondenza della voce di indice corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1b56-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="a1b56-181">La posizione del cursore rimarrà invariata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="a1b56-182">Se JET_errNoCurrentRecord è stato restituito ed è stata costruita una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="a1b56-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="a1b56-183">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="a1b56-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a1b56-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1b56-184">Remarks</span></span>

<span data-ttu-id="a1b56-185">Un intervallo di indice è volatile e verrà annullato automaticamente se nel cursore viene eseguita una navigazione diversa da [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b56-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="a1b56-186">Gli intervalli di indice funzionano solo in una direzione.</span><span class="sxs-lookup"><span data-stu-id="a1b56-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="a1b56-187">Se viene stabilito un limite superiore, viene impedito solo il movimento in diretta usando [JetMove](./jetmove-function.md) con JET_MoveNext o un offset positivo dopo che è stata raggiunta la fine dell'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a1b56-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="a1b56-188">In questo caso è comunque possibile lasciare l'intervallo di indici utilizzando [JetMove](./jetmove-function.md) con JET_MovePrevious o un offset negativo.</span><span class="sxs-lookup"><span data-stu-id="a1b56-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="a1b56-189">Una situazione analoga si verifica per un limite inferiore.</span><span class="sxs-lookup"><span data-stu-id="a1b56-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a1b56-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1b56-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-191"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a1b56-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b56-192">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a1b56-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a1b56-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b56-194">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a1b56-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-195"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a1b56-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b56-196">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a1b56-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b56-197"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a1b56-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b56-198">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a1b56-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b56-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a1b56-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b56-200">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a1b56-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a1b56-201">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a1b56-201">See Also</span></span>

[<span data-ttu-id="a1b56-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a1b56-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a1b56-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a1b56-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a1b56-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a1b56-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a1b56-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a1b56-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a1b56-206">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="a1b56-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="a1b56-207">JetMove</span><span class="sxs-lookup"><span data-stu-id="a1b56-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a1b56-208">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="a1b56-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="a1b56-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a1b56-209">JetStopService</span></span>](./jetstopservice-function.md)
