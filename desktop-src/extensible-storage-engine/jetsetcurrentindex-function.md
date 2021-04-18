---
description: 'Altre informazioni su: funzione JetSetCurrentIndex'
title: Funzione JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306217"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="f1703-103">Funzione JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="f1703-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="f1703-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f1703-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="f1703-105">Funzione JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="f1703-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="f1703-106">La funzione **JetSetCurrentIndex** può essere utilizzata per impostare l'indice corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="f1703-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="f1703-107">L'indice corrente di un cursore definisce quali record di una tabella sono visibili a tale cursore e l'ordine in cui vengono visualizzati selezionando il set di voci di indice da utilizzare per esporre tali record.</span><span class="sxs-lookup"><span data-stu-id="f1703-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="f1703-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1703-108">Parameters</span></span>

<span data-ttu-id="f1703-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f1703-109">*sesid*</span></span>

<span data-ttu-id="f1703-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="f1703-110">The session to use for this call.</span></span>

<span data-ttu-id="f1703-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f1703-111">*tableid*</span></span>

<span data-ttu-id="f1703-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="f1703-112">The cursor to use for this call.</span></span>

<span data-ttu-id="f1703-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="f1703-113">*szIndexName*</span></span>

<span data-ttu-id="f1703-114">Nome dell'indice da selezionare per il cursore.</span><span class="sxs-lookup"><span data-stu-id="f1703-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="f1703-115">Se questo parametro è NULL o una stringa vuota, verrà selezionato l'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="f1703-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="f1703-116">Se viene definito un indice primario per la tabella, l'indice verrà selezionato perché corrisponde all'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="f1703-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="f1703-117">Se per la tabella non è definito alcun indice primario, verrà selezionato l'indice sequenziale.</span><span class="sxs-lookup"><span data-stu-id="f1703-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="f1703-118">La definizione dell'indice sequenziale non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f1703-118">The sequential index has no index definition.</span></span> <span data-ttu-id="f1703-119">Per ulteriori informazioni, vedere [JetCreateIndex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f1703-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="f1703-120">Se *pIndexID* non è null, il nome dell'indice verrà ignorato e l'indice verrà selezionato in base al relativo ID di indice.</span><span class="sxs-lookup"><span data-stu-id="f1703-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="f1703-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1703-121">Return Value</span></span>

<span data-ttu-id="f1703-122">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f1703-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f1703-123">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f1703-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1703-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f1703-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="f1703-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1703-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1703-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f1703-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f1703-127">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f1703-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="f1703-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="f1703-129">Viene selezionato un indice secondario con l'opzione JET_bitNoMove e non è presente alcun valore per la prima colonna chiave multivalore nella definizione del nuovo indice che corrisponde al numero di sequenza specificato.</span><span class="sxs-lookup"><span data-stu-id="f1703-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f1703-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f1703-131">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f1703-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="f1703-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="f1703-133">Il contenuto dell'ID di indice non è valido o è scaduto e deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f1703-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="f1703-134">Questo problema può verificarsi per <strong>JetSetCurrentIndex</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="f1703-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1703-135">pIndexID- &gt; cbStruct non è della dimensione prevista (Windows Server 2003 e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="f1703-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="f1703-136">Il motore è stato arrestato perché è stato recuperato l'ID dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f1703-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="f1703-137">Tutti i cursori che fanno riferimento alla tabella contenente l'indice corrispondente all'ID dell'indice sono stati chiusi e il motore ha rimosso la definizione di tale indice dalla cache dello schema.</span><span class="sxs-lookup"><span data-stu-id="f1703-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="f1703-138">L'ID di indice viene utilizzato con un cursore aperto nella tabella errata.</span><span class="sxs-lookup"><span data-stu-id="f1703-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="f1703-139">L'indice è stato eliminato o non è ancora visibile alla sessione.</span><span class="sxs-lookup"><span data-stu-id="f1703-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f1703-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f1703-141">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="f1703-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f1703-142">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f1703-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="f1703-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="f1703-144">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="f1703-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="f1703-145">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="f1703-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="f1703-146">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1703-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1703-147">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="f1703-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="f1703-148">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="f1703-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="f1703-149">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="f1703-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="f1703-150">I nomi degli oggetti non possono iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="f1703-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="f1703-151">I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="f1703-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="f1703-152">I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</span><span class="sxs-lookup"><span data-stu-id="f1703-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="f1703-153">Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1703-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="f1703-154">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="f1703-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f1703-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f1703-156">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="f1703-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="f1703-157">Questo problema può verificarsi per <strong>JetSetCurrentIndex</strong> quando <em>PINDEXID</em> non è null e pIndexID- &gt; cbStruct non è della dimensione prevista (Windows XP e versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="f1703-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="f1703-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="f1703-159">Un indice secondario viene selezionato con l'opzione JET_bitNoMove e non è presente alcuna voce di indice nel nuovo indice che corrisponde al record associato alla voce di indice nella posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="f1703-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f1703-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f1703-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="f1703-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="f1703-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="f1703-163">Il motore ha esaurito il pool di risorse utilizzate per aprire i cursori.</span><span class="sxs-lookup"><span data-stu-id="f1703-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="f1703-164">Il numero massimo di cursori che è possibile aprire in qualsiasi momento viene controllato utilizzando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="f1703-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="f1703-165">Per ulteriori informazioni, vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> .</span><span class="sxs-lookup"><span data-stu-id="f1703-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="f1703-166">Questo problema può verificarsi per <strong>JetSetCurrentIndex</strong> quando è stato selezionato un indice secondario e il motore non è in grado di aprire un cursore interno per utilizzare tale indice.</span><span class="sxs-lookup"><span data-stu-id="f1703-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f1703-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f1703-168">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="f1703-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f1703-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f1703-170">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="f1703-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="f1703-171">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f1703-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f1703-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f1703-173">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="f1703-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1703-174">In seguito all'esito positivo, l'indice corrente del cursore viene impostato sull'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="f1703-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="f1703-175">È ora possibile cercare le voci di indice usando [JetSeek](./jetseek-function.md) in base alla definizione dell'indice dell'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="f1703-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="f1703-176">È inoltre possibile enumerare le voci di indice utilizzando [JetMove](./jetmove-function.md) nell'ordine specificato dalla definizione di tale indice.</span><span class="sxs-lookup"><span data-stu-id="f1703-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="f1703-177">La posizione corrente del cursore viene impostata sulla prima voce di indice nell'indice (JET_bitMoveFirst) o su una voce di indice specifica correlata alla posizione corrente del cursore sull'indice precedente (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="f1703-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="f1703-178">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="f1703-178">No change to the database state will occur.</span></span>

<span data-ttu-id="f1703-179">In caso di errore, l'indice corrente e la posizione corrente del cursore sono in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="f1703-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="f1703-180">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="f1703-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f1703-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1703-181">Remarks</span></span>

<span data-ttu-id="f1703-182">Se l'hint ID dell'indice non è aggiornato, l'API ha semplicemente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f1703-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="f1703-183">In questo caso, non esiste alcun fallback al nome di testo dell'indice, come si può prevedere.</span><span class="sxs-lookup"><span data-stu-id="f1703-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="f1703-184">Questo fallback deve essere eseguito manualmente dal chiamante dell'API.</span><span class="sxs-lookup"><span data-stu-id="f1703-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f1703-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1703-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1703-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f1703-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1703-187">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f1703-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f1703-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1703-189">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f1703-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-190"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f1703-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1703-191">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f1703-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-192"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f1703-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f1703-193">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f1703-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1703-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f1703-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f1703-195">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f1703-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1703-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f1703-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f1703-197">Implementato come <strong>JetSetCurrentIndexW</strong> (Unicode) e <strong>JetSetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f1703-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f1703-198">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f1703-198">See Also</span></span>

[<span data-ttu-id="f1703-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f1703-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f1703-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f1703-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f1703-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f1703-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f1703-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f1703-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f1703-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f1703-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="f1703-204">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f1703-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="f1703-205">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="f1703-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="f1703-206">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f1703-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="f1703-207">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f1703-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="f1703-208">JetMove</span><span class="sxs-lookup"><span data-stu-id="f1703-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="f1703-209">JetSeek</span><span class="sxs-lookup"><span data-stu-id="f1703-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="f1703-210">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="f1703-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="f1703-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="f1703-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="f1703-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f1703-212">JetStopService</span></span>](./jetstopservice-function.md)
