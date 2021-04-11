---
description: 'Altre informazioni su: funzione JetSetColumns'
title: Funzione JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128159"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="cc160-103">Funzione JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="cc160-103">JetSetColumns Function</span></span>


<span data-ttu-id="cc160-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc160-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="cc160-105">Funzione JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="cc160-105">JetSetColumns Function</span></span>

<span data-ttu-id="cc160-106">La funzione **JetSetColumns** ha un comportamento simile a [JetSetColumn](./jetsetcolumn-function.md) , ma consente a un'applicazione di impostare più valori di colonna in una singola operazione.</span><span class="sxs-lookup"><span data-stu-id="cc160-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="cc160-107">Una matrice di strutture di [JET_SETCOLUMN](./jet-setcolumn-structure.md) viene utilizzata per descrivere il set di valori di colonna da impostare e per descrivere i buffer di input per ogni valore di colonna da impostare.</span><span class="sxs-lookup"><span data-stu-id="cc160-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="cc160-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc160-108">Parameters</span></span>

<span data-ttu-id="cc160-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cc160-109">*sesid*</span></span>

<span data-ttu-id="cc160-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc160-110">The session to use for this call.</span></span>

<span data-ttu-id="cc160-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="cc160-111">*tableid*</span></span>

<span data-ttu-id="cc160-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc160-112">The cursor to use for this call.</span></span>

<span data-ttu-id="cc160-113">*psetcolumn*</span><span class="sxs-lookup"><span data-stu-id="cc160-113">*psetcolumn*</span></span>

<span data-ttu-id="cc160-114">Puntatore a una matrice di una o più strutture di [JET_SETCOLUMN](./jet-setcolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="cc160-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="cc160-115">Ogni struttura include le descrizioni del valore di colonna da impostare e da dove ottenere i dati della colonna da impostare.</span><span class="sxs-lookup"><span data-stu-id="cc160-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="cc160-116">*csetcolumn*</span><span class="sxs-lookup"><span data-stu-id="cc160-116">*csetcolumn*</span></span>

<span data-ttu-id="cc160-117">Numero di strutture di [JET_SETCOLUMN](./jet-setcolumn-structure.md) nella matrice specificata da *psetcolumn*.</span><span class="sxs-lookup"><span data-stu-id="cc160-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="cc160-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc160-118">Return Value</span></span>

<span data-ttu-id="cc160-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="cc160-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cc160-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="cc160-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc160-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cc160-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="cc160-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc160-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc160-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="cc160-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="cc160-124">L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="cc160-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cc160-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cc160-126">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="cc160-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="cc160-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="cc160-128">Uguale a JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="cc160-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="cc160-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="cc160-130">La colonna descritta dal <em>ColumnID</em> specificato non esiste nella tabella.</span><span class="sxs-lookup"><span data-stu-id="cc160-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="cc160-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="cc160-132">È stato effettuato un tentativo non valido di aggiornare un valore Long durante un'operazione di eliminazione dell'aggiornamento originale della copia di inserimento.</span><span class="sxs-lookup"><span data-stu-id="cc160-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="cc160-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="cc160-134">I dati del valore di colonna specificati nel buffer di input superano il limite di dimensione naturale per una colonna a lunghezza fissa o sono configurati per colonne di tipo text o binary a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="cc160-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="cc160-135">Questo errore viene restituito anche quando si passano più di 1024 byte di dati per una colonna estesa e si imposta il flag di JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="cc160-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cc160-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cc160-137">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="cc160-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cc160-138">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc160-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="cc160-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="cc160-140">La dimensione dei dati del valore della colonna specificata non corrisponde a quanto è naturale per il tipo di dati a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="cc160-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="cc160-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="cc160-142">È stato effettuato un tentativo non valido di aggiornare una colonna con incremento automatico durante un'operazione di inserimento o aggiornamento oppure di aggiornare una colonna della versione durante un'operazione di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="cc160-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="cc160-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="cc160-144">Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</span><span class="sxs-lookup"><span data-stu-id="cc160-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cc160-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cc160-146">Il valore di psetinfo- &gt; cbStruct specificato non è una dimensione valida per la struttura <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="cc160-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="cc160-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="cc160-148">L'operazione set Column ha tentato di creare un valore duplicato e ha specificato JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="cc160-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cc160-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cc160-150">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="cc160-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="cc160-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="cc160-152">È stato effettuato un tentativo non valido di aggiornare un valore di colonna lungo quando la sessione chiamante non era presente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="cc160-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="cc160-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="cc160-154">È stato effettuato un tentativo non valido di impostare una colonna non NULL su NULL.</span><span class="sxs-lookup"><span data-stu-id="cc160-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="cc160-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="cc160-156">Il valore della colonna non può essere impostato sul valore nel buffer di input perché avrebbe causato il superamento del limite di dimensioni relative alle dimensioni della pagina.</span><span class="sxs-lookup"><span data-stu-id="cc160-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="cc160-157">Le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> possono essere archiviate separatamente dai dati rimanenti del record.</span><span class="sxs-lookup"><span data-stu-id="cc160-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="cc160-158">Tuttavia, altre colonne devono essere archiviate con il record e possono causare il superamento del limite delle dimensioni del record.</span><span class="sxs-lookup"><span data-stu-id="cc160-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="cc160-159">Anche le colonne lunghe richiedono 5 byte di spazio all'interno del record come collegamento e questo può comportare la restituzione di JET_errRecordTooBig.</span><span class="sxs-lookup"><span data-stu-id="cc160-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cc160-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc160-161">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="cc160-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cc160-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cc160-163">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="cc160-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="cc160-164">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc160-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cc160-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc160-166">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="cc160-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="cc160-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="cc160-168">Il cursore non è attualmente in fase di inserimento di un nuovo record o di aggiornamento di un record esistente.</span><span class="sxs-lookup"><span data-stu-id="cc160-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="cc160-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="cc160-170">Il valore della colonna nel buffer di input supera la lunghezza massima configurata per una colonna a lunghezza variabile ed è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="cc160-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc160-171">In seguito all'esito positivo, per ogni colonna descritta in psetcolumns, la parte desiderata del valore della colonna viene impostata con i dati copiati dal buffer di input.</span><span class="sxs-lookup"><span data-stu-id="cc160-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="cc160-172">Il set di dati della colonna potrebbe essere stato troncato se è stata superata la lunghezza massima specificata per una colonna a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="cc160-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="cc160-173">In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato di valore di colonna viene aggiornato nel buffer di copia.</span><span class="sxs-lookup"><span data-stu-id="cc160-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc160-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc160-174">Remarks</span></span>

<span data-ttu-id="cc160-175">Se una singola operazione set Column restituisce un errore, l'intera operazione **JetSetColumns** restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="cc160-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="cc160-176">Gli avvisi, in generale, vengono restituiti in psetcolumns- \> Error e non nel codice restituito da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="cc160-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="cc160-177">Tuttavia, se l'ultimo set di colonne presenta un avviso, questo avviso verrà restituito da **JetSetColumns** stesso.</span><span class="sxs-lookup"><span data-stu-id="cc160-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc160-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc160-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc160-179"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cc160-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc160-180">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cc160-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cc160-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc160-182">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cc160-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-183"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="cc160-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc160-184">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc160-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc160-185"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="cc160-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cc160-186">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cc160-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc160-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cc160-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cc160-188">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cc160-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc160-189">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cc160-189">See Also</span></span>

[<span data-ttu-id="cc160-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="cc160-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="cc160-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc160-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc160-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cc160-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cc160-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cc160-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cc160-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="cc160-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="cc160-195">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="cc160-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="cc160-196">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="cc160-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
