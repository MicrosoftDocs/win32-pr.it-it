---
description: 'Altre informazioni su: funzione JetRetrieveColumns'
title: Funzione JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233633"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="c0225-103">Funzione JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="c0225-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="c0225-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c0225-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="c0225-105">Funzione JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="c0225-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="c0225-106">La funzione **JetRetrieveColumns** recupera più valori di colonna dal record corrente in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="c0225-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="c0225-107">Una matrice di strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) viene utilizzata per descrivere il set di valori di colonna da recuperare e per descrivere i buffer di output per ogni valore di colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c0225-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="c0225-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0225-108">Parameters</span></span>

<span data-ttu-id="c0225-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c0225-109">*sesid*</span></span>

<span data-ttu-id="c0225-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c0225-110">The session to use for this call.</span></span>

<span data-ttu-id="c0225-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c0225-111">*tableid*</span></span>

<span data-ttu-id="c0225-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c0225-112">The cursor to use for this call.</span></span>

<span data-ttu-id="c0225-113">*pretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="c0225-113">*pretrievecolumn*</span></span>

<span data-ttu-id="c0225-114">Puntatore a una matrice di una o più strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c0225-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="c0225-115">Ogni struttura include le descrizioni del valore della colonna da recuperare e la posizione in cui archiviare i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="c0225-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="c0225-116">*cretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="c0225-116">*cretrievecolumn*</span></span>

<span data-ttu-id="c0225-117">Numero di strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) nella matrice specificata da *pretrievecolumn*.</span><span class="sxs-lookup"><span data-stu-id="c0225-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="c0225-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0225-118">Return Value</span></span>

<span data-ttu-id="c0225-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c0225-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c0225-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c0225-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0225-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c0225-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="c0225-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0225-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0225-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c0225-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c0225-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c0225-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="c0225-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="c0225-126">È stato passato un valore del numero di sequenza di colonna multivalore non valido in pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="c0225-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="c0225-127">I valori validi per i numeri di sequenza dei valori di colonna multivalore sono pari a 1 o superiore.</span><span class="sxs-lookup"><span data-stu-id="c0225-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="c0225-128">Il valore 0 (zero) è valido per questa funzione ma non è valido per <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="c0225-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="c0225-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="c0225-130">L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c0225-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c0225-132">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c0225-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="c0225-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="c0225-134">La colonna descritta dal <em>ColumnID</em> specificato non esiste nella tabella.</span><span class="sxs-lookup"><span data-stu-id="c0225-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="c0225-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="c0225-136">Le colonne indicizzate come sottostringhe non possono essere recuperate dall'indice, perché solo una piccola parte della colonna è in genere presente in ogni voce di indice.</span><span class="sxs-lookup"><span data-stu-id="c0225-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="c0225-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="c0225-138">In alcuni casi, il buffer fornito per la colonna di recupero deve essere sufficientemente dimensionato per restituire qualsiasi quantità di valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="c0225-139">Ad esempio, le colonne aggiornabili con deposito sono regolate in modo da essere coerenti per il contesto transazionale della sessione chiamante e questa regolazione richiede il buffer fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="c0225-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="c0225-140">Se viene fornito spazio sufficiente nel buffer, viene restituito JET_errInvalidBufferSize e non vengono restituiti dati di colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="c0225-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="c0225-142">Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</span><span class="sxs-lookup"><span data-stu-id="c0225-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c0225-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c0225-144">Uno o più parametri specificati non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="c0225-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="c0225-145">Questo problema può verificarsi se retinfo. cbStruct è più piccolo della dimensione del <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="c0225-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c0225-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c0225-147">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="c0225-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c0225-148"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c0225-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="c0225-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="c0225-150">Il cursore non è posizionato in corrispondenza di un record.</span><span class="sxs-lookup"><span data-stu-id="c0225-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="c0225-151">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="c0225-151">This can happen for many different reasons.</span></span> <span data-ttu-id="c0225-152">Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="c0225-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c0225-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c0225-154">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c0225-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c0225-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c0225-156">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c0225-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c0225-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c0225-158">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c0225-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c0225-159"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c0225-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c0225-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c0225-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="c0225-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="c0225-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="c0225-163">Impossibile recuperare l'intero valore della colonna perché il buffer specificato è inferiore alle dimensioni della colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0225-164">In seguito all'esito positivo, i dati delle colonne e le dimensioni della colonna vengono restituiti nei buffer forniti descritti in matrice di strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c0225-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="c0225-165">Se un *itagSequence* è stato impostato su 0 (zero) per indicare che è stato richiesto il numero di istanze di un campo multivalore anziché i dati della colonna, il numero di istanze di una colonna multivalore viene restituito nel campo *itagSequence* .</span><span class="sxs-lookup"><span data-stu-id="c0225-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="c0225-166">Ogni struttura [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) dispone di un campo di errore che contiene avvisi per la colonna recuperata.</span><span class="sxs-lookup"><span data-stu-id="c0225-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="c0225-167">Se la colonna è di valore **null** , il codice di errore verrà impostato su JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="c0225-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="c0225-168">In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato viene copiato nel buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="c0225-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c0225-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0225-169">Remarks</span></span>

<span data-ttu-id="c0225-170">**JetRetrieveColumns** supporta una funzionalità che non è supportata da [JetRetrieveColumn](./jetretrievecolumn-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c0225-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="c0225-171">Si tratta della possibilità di recuperare il numero di istanze di una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="c0225-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="c0225-172">Lo scopo di questa funzionalità è quello di consentire a un'applicazione di recuperare tutti i valori di una colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="c0225-173">Questa operazione può essere eseguita determinando innanzitutto il numero di valori di una colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="c0225-174">Successivamente, è possibile determinare la loro lunghezza chiamando di nuovo **JetRetrieveColumns** con una struttura [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) allocata per ogni valore per determinare la lunghezza dei dati della colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="c0225-175">Questa operazione può essere eseguita passando i puntatori _PvData_ **null** con *cbMax* 0 (zero) e recuperando la lunghezza della colonna in *cbActual*.</span><span class="sxs-lookup"><span data-stu-id="c0225-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="c0225-176">La terza e ultima chiamata può essere effettuata con la memoria allocata per i dati del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="c0225-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="c0225-177">Se una colonna recuperata viene troncata a causa di un buffer di lunghezza insufficiente, l'API restituirà JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="c0225-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="c0225-178">Tuttavia, altri errori JET_wrnColumnNull vengono restituiti solo nel campo errore [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c0225-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="c0225-179">Il motivo è che le applicazioni spesso vogliono garantire che tutti i dati siano stati recuperati e la restituzione di questo errore da **JetRetrieveColumns** facilita questa comprensione.</span><span class="sxs-lookup"><span data-stu-id="c0225-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c0225-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0225-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0225-181"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c0225-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c0225-182">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c0225-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-183"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c0225-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c0225-184">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c0225-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-185"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c0225-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c0225-186">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c0225-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0225-187"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c0225-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c0225-188">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c0225-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0225-189"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c0225-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c0225-190">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c0225-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c0225-191">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c0225-191">See Also</span></span>

[<span data-ttu-id="c0225-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c0225-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c0225-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c0225-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c0225-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c0225-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c0225-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="c0225-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="c0225-196">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="c0225-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="c0225-197">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="c0225-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="c0225-198">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="c0225-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
