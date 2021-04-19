---
description: 'Altre informazioni su: funzione JetRetrieveColumn'
title: Funzione JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318084"
---
# <a name="jetretrievecolumn-function"></a><span data-ttu-id="054a7-103">Funzione JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="054a7-103">JetRetrieveColumn Function</span></span>


<span data-ttu-id="054a7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="054a7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumn-function"></a><span data-ttu-id="054a7-105">Funzione JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="054a7-105">JetRetrieveColumn Function</span></span>

<span data-ttu-id="054a7-106">La funzione **JetRetrieveColumn** recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="054a7-106">The **JetRetrieveColumn** function retrieves a single column value from the current record.</span></span> <span data-ttu-id="054a7-107">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="054a7-107">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="054a7-108">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="054a7-108">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="054a7-109">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="054a7-109">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="054a7-110">Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare **JetRetrieveColumn** anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="054a7-110">In addition to retrieving the actual column value, **JetRetrieveColumn** can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="054a7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="054a7-111">Parameters</span></span>

<span data-ttu-id="054a7-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="054a7-112">*sesid*</span></span>

<span data-ttu-id="054a7-113">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="054a7-113">The session to use for this call.</span></span>

<span data-ttu-id="054a7-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="054a7-114">*tableid*</span></span>

<span data-ttu-id="054a7-115">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="054a7-115">The cursor to use for this call.</span></span>

<span data-ttu-id="054a7-116">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="054a7-116">*columnid*</span></span>

<span data-ttu-id="054a7-117">[JET_COLUMNID](./jet-columnid.md) della colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="054a7-117">The [JET_COLUMNID](./jet-columnid.md) of the column to retrieve.</span></span>

<span data-ttu-id="054a7-118">È possibile specificare un valore *ColumnID* pari a 0 (zero) che non si riferisce a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-118">A *columnid* value of 0 (zero) can be given which does not itself refer to any individual column.</span></span> <span data-ttu-id="054a7-119">Quando viene specificato *ColumnID* 0 (zero), tutte le colonne con tag, le colonne di tipo sparse e quelle multivalore vengono considerate come una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-119">When *columnid* 0 (zero) is given, all tagged columns, sparse, and multi-valued columns are treated as a single column.</span></span> <span data-ttu-id="054a7-120">Ciò facilita il recupero di tutte le colonne di tipo sparse presenti in un record.</span><span class="sxs-lookup"><span data-stu-id="054a7-120">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="054a7-121">*pvData*</span><span class="sxs-lookup"><span data-stu-id="054a7-121">*pvData*</span></span>

<span data-ttu-id="054a7-122">Buffer di output che riceve il valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-122">The output buffer that receives the column value.</span></span>

<span data-ttu-id="054a7-123">*cbData*</span><span class="sxs-lookup"><span data-stu-id="054a7-123">*cbData*</span></span>

<span data-ttu-id="054a7-124">Dimensione massima, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="054a7-124">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="054a7-125">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="054a7-125">*pcbActual*</span></span>

<span data-ttu-id="054a7-126">Riceve le dimensioni effettive, in byte, del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-126">Receives the actual size, in bytes, of the column value.</span></span>

<span data-ttu-id="054a7-127">Se questo parametro è **null**, le dimensioni effettive del valore della colonna non verranno restituite.</span><span class="sxs-lookup"><span data-stu-id="054a7-127">If this parameter is **NULL**, then the actual size of the column value will not be returned.</span></span>

<span data-ttu-id="054a7-128">*grbit*</span><span class="sxs-lookup"><span data-stu-id="054a7-128">*grbit*</span></span>

<span data-ttu-id="054a7-129">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="054a7-129">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="054a7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="054a7-130">Value</span></span></p></th>
<th><p><span data-ttu-id="054a7-131">Significato</span><span class="sxs-lookup"><span data-stu-id="054a7-131">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="054a7-132">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="054a7-132">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="054a7-133">Questo flag consente a retrieve Column di recuperare il valore modificato anziché il valore originale.</span><span class="sxs-lookup"><span data-stu-id="054a7-133">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="054a7-134">Se il valore non è stato modificato, viene recuperato il valore originale.</span><span class="sxs-lookup"><span data-stu-id="054a7-134">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="054a7-135">In questo modo, è possibile recuperare un valore che non è ancora stato inserito o aggiornato durante l'operazione di inserimento o aggiornamento di un record.</span><span class="sxs-lookup"><span data-stu-id="054a7-135">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-136">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="054a7-136">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="054a7-137">Questa opzione viene utilizzata per recuperare i valori di colonna dall'indice, se possibile, senza accedere al record.</span><span class="sxs-lookup"><span data-stu-id="054a7-137">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="054a7-138">In questo modo, è possibile evitare il caricamento di record superflui quando sono disponibili dati necessari dalle voci dell'indice.</span><span class="sxs-lookup"><span data-stu-id="054a7-138">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="054a7-139">Nei casi in cui non è possibile recuperare il valore della colonna originale dall'indice a causa di trasformazioni irreversibili o troncamenti dei dati, il record sarà accessibile e i dati verranno recuperati normalmente.</span><span class="sxs-lookup"><span data-stu-id="054a7-139">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="054a7-140">Si tratta di un'opzione relativa alle prestazioni e deve essere specificata solo quando è probabile che il valore della colonna possa essere recuperato dall'indice.</span><span class="sxs-lookup"><span data-stu-id="054a7-140">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="054a7-141">Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster, perché le voci di indice per l'indice cluster o primario sono i record stessi.</span><span class="sxs-lookup"><span data-stu-id="054a7-141">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="054a7-142">Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromPrimaryBookmark.</span><span class="sxs-lookup"><span data-stu-id="054a7-142">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-143">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="054a7-143">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="054a7-144">Questa opzione viene utilizzata per recuperare i valori di colonna dal segnalibro index e può variare dal valore di indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="054a7-144">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="054a7-145">Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario.</span><span class="sxs-lookup"><span data-stu-id="054a7-145">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="054a7-146">Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="054a7-146">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-147">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="054a7-147">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="054a7-148">Questa opzione viene utilizzata per recuperare il numero di sequenza di un valore di colonna multivalore in pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="054a7-148">This option is used to retrieve the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="054a7-149">Il campo itagSequence è in genere un input per il recupero di valori di colonna multivalore da un record.</span><span class="sxs-lookup"><span data-stu-id="054a7-149">The itagSequence field is commonly an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="054a7-150">Tuttavia, quando si recuperano i valori da un indice, è anche possibile associare la voce di indice a un determinato numero di sequenza e recuperare anche questo numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="054a7-150">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="054a7-151">Il recupero del numero di sequenza può essere un'operazione costosa e deve essere eseguito solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="054a7-151">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-152">JET_bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="054a7-152">JET_bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="054a7-153">Questa opzione viene utilizzata per recuperare i valori <strong>null</strong> della colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="054a7-153">This option is used to retrieve multi-valued column <strong>NULL</strong> values.</span></span> <span data-ttu-id="054a7-154">Se questa opzione non è specificata, i valori <strong>null</strong> della colonna multivalore verranno automaticamente ignorati.</span><span class="sxs-lookup"><span data-stu-id="054a7-154">If this option is not specified, multi-valued column <strong>NULL</strong> values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-155">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="054a7-155">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="054a7-156">Questa opzione ha effetto solo sulle colonne multivalore e causa la restituzione di un valore <strong>null</strong> quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record.</span><span class="sxs-lookup"><span data-stu-id="054a7-156">This option affects only multi-valued columns and causes a <strong>NULL</strong> value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-157">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="054a7-157">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="054a7-158">Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="054a7-158">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-159">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="054a7-159">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="054a7-160">Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="054a7-160">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-161">JET_bitRetrieveTuple</span><span class="sxs-lookup"><span data-stu-id="054a7-161">JET_bitRetrieveTuple</span></span></p></td>
<td><p><span data-ttu-id="054a7-162">Questo flag consente il recupero di un segmento di tupla dell'indice.</span><span class="sxs-lookup"><span data-stu-id="054a7-162">This flag will allow the retrieval of a tuple segment of the index.</span></span> <span data-ttu-id="054a7-163">Questo bit deve essere specificato con JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="054a7-163">This bit must be specified with JET_bitRetrieveFromIndex.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="054a7-164">*pretinfo*</span><span class="sxs-lookup"><span data-stu-id="054a7-164">*pretinfo*</span></span>

<span data-ttu-id="054a7-165">Se *pretinfo* viene fornito come **null** , la funzione si comporta come se fosse stato specificato un *itagSequence* di 1 e un *ibLongValue* di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="054a7-165">If *pretinfo* is give as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="054a7-166">In questo modo il recupero della colonna Recupera il primo valore di una colonna multivalore e recupera i dati lunghi in corrispondenza dell'offset 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="054a7-166">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

<span data-ttu-id="054a7-167">Questo parametro viene usato per fornire uno o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="054a7-167">This parameter is used to provide one or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="054a7-168">Valore</span><span class="sxs-lookup"><span data-stu-id="054a7-168">Value</span></span></p></th>
<th><p><span data-ttu-id="054a7-169">Significato</span><span class="sxs-lookup"><span data-stu-id="054a7-169">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="054a7-170">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="054a7-170">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="054a7-171">Restituisce un offset binario in un valore di colonna lungo durante il recupero di una parte di un valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-171">Gives a binary offset into a long column value when retrieving a portion of a column value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-172">itagSequence</span><span class="sxs-lookup"><span data-stu-id="054a7-172">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="054a7-173">Indica il numero di sequenza del valore della colonna multivalore desiderato.</span><span class="sxs-lookup"><span data-stu-id="054a7-173">Gives the sequence number of the desired multi-valued column value.</span></span> <span data-ttu-id="054a7-174">Si noti che questo campo viene impostato solo se viene specificato il JET_bitRetrieveTag.</span><span class="sxs-lookup"><span data-stu-id="054a7-174">Note that this field is only set if the JET_bitRetrieveTag is specified.</span></span> <span data-ttu-id="054a7-175">In caso contrario, non sarà modificato.</span><span class="sxs-lookup"><span data-stu-id="054a7-175">Otherwise, it is unmodified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-176">columnidNextTagged</span><span class="sxs-lookup"><span data-stu-id="054a7-176">columnidNextTagged</span></span></p></td>
<td><p><span data-ttu-id="054a7-177">Restituisce l'ID di colonna del valore della colonna restituito durante il recupero di tutte le colonne con tag, di tipo sparse e multivalore, usando il passaggio di <em>ColumnID</em> di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="054a7-177">Returns the column ID of the returned column value when retrieving all tagged, sparse and multi-valued, columns using passing <em>columnid</em> of 0 (zero).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="054a7-178">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="054a7-178">Return Value</span></span>

<span data-ttu-id="054a7-179">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="054a7-179">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="054a7-180">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="054a7-180">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="054a7-181">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="054a7-181">Return code</span></span></p></th>
<th><p><span data-ttu-id="054a7-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="054a7-182">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="054a7-183">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="054a7-183">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="054a7-184">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="054a7-184">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-185">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="054a7-185">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="054a7-186">L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-186">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-187">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="054a7-187">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="054a7-188">È stato passato un valore del numero di sequenza di colonna multivalore non valido in pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="054a7-188">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="054a7-189">I valori validi per i numeri di sequenza dei valori di colonna multivalore sono pari a 1 o superiore.</span><span class="sxs-lookup"><span data-stu-id="054a7-189">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="054a7-190">Il valore 0 (zero) non è valido per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="054a7-190">A value of 0 (zero) is invalid for this function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="054a7-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="054a7-192">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="054a7-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-193">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="054a7-193">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="054a7-194">La colonna descritta dal <em>ColumnID</em> specificato non esiste nella tabella.</span><span class="sxs-lookup"><span data-stu-id="054a7-194">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-195">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="054a7-195">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="054a7-196">Le colonne indicizzate come sottostringhe non possono essere recuperate dall'indice, perché solo una piccola parte della colonna è in genere presente in ogni voce di indice.</span><span class="sxs-lookup"><span data-stu-id="054a7-196">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-197">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="054a7-197">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="054a7-198">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="054a7-198">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="054a7-199">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="054a7-199">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-200">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="054a7-200">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="054a7-201">In alcuni casi, il buffer fornito per la colonna di recupero deve essere sufficientemente dimensionato per restituire qualsiasi quantità di valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-201">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="054a7-202">Ad esempio, le colonne aggiornabili con deposito sono regolate in modo da essere coerenti per il contesto transazionale della sessione chiamante e questa regolazione richiede il buffer fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="054a7-202">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="054a7-203">Se viene fornito spazio sufficiente nel buffer, viene restituito JET_errInvalidBufferSize e non vengono restituiti dati di colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-203">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-204">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="054a7-204">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="054a7-205">Uno o più parametri specificati non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="054a7-205">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="054a7-206">Questo problema può verificarsi se retinfo. cbStruct è più piccolo della dimensione del <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="054a7-206">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-207">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="054a7-207">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="054a7-208">Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</span><span class="sxs-lookup"><span data-stu-id="054a7-208">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-209">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="054a7-209">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="054a7-210">Il cursore non è posizionato in corrispondenza di un record.</span><span class="sxs-lookup"><span data-stu-id="054a7-210">The cursor is not positioned on a record.</span></span> <span data-ttu-id="054a7-211">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="054a7-211">This can happen for many different reasons.</span></span> <span data-ttu-id="054a7-212">Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="054a7-212">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-213">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="054a7-213">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="054a7-214">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="054a7-214">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-215">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="054a7-215">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="054a7-216">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="054a7-216">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-217">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="054a7-217">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="054a7-218">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="054a7-218">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="054a7-219"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="054a7-219"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-220">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="054a7-220">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="054a7-221">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="054a7-221">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-222">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="054a7-222">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="054a7-223">Impossibile recuperare l'intero valore della colonna perché il buffer specificato è inferiore alle dimensioni della colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-223">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-224">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="054a7-224">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="054a7-225">Il valore della colonna recuperato è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="054a7-225">The column value retrieved is <strong>NULL</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="054a7-226">In seguito all'esito positivo, il valore della colonna per la colonna specificata viene copiato nel buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="054a7-226">On success, the column value for the given column, is copied into the given buffer.</span></span> <span data-ttu-id="054a7-227">Viene copiato un valore inferiore a quello di tutte le colonne con l'avviso JET_wrnBufferTruncated viene restituito.</span><span class="sxs-lookup"><span data-stu-id="054a7-227">Less than all of the column value is copied with the warning JET_wrnBufferTruncated is returned.</span></span> <span data-ttu-id="054a7-228">Se è stato specificato *pcbActual* , vengono restituite le dimensioni effettive del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-228">If the *pcbActual* was given, the actual size of the column value is returned.</span></span> <span data-ttu-id="054a7-229">Si noti che i valori **null** hanno una lunghezza pari a 0 (zero) e in questo modo le dimensioni restituite vengono impostate su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="054a7-229">Note that **NULL** values have 0 (zero) length and will thus set the returned size to 0 (zero).</span></span> <span data-ttu-id="054a7-230">Se la colonna recuperata è una colonna multivalore e è stato specificato *pretinfo* e JET_bitReturnTag è stato impostato come opzione, il numero di sequenza del valore della colonna viene restituito in pretinfo- \> itagSequence.</span><span class="sxs-lookup"><span data-stu-id="054a7-230">If the column retrieved was a multi-valued column, and *pretinfo* was given, and JET_bitReturnTag was set as an option, then the sequence number of the column value is returned in pretinfo-\>itagSequence.</span></span>

<span data-ttu-id="054a7-231">In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato viene copiato nel buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="054a7-231">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="054a7-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="054a7-232">Remarks</span></span>

<span data-ttu-id="054a7-233">Questa chiamata viene utilizzata una sola volta per recuperare dati di dimensioni fisse o note per le colonne non multivalore.</span><span class="sxs-lookup"><span data-stu-id="054a7-233">This call is used just once to retrieve data of fixed or known size for non-multi-valued columns.</span></span> <span data-ttu-id="054a7-234">Tuttavia, quando i dati della colonna sono di dimensioni sconosciute, questa chiamata viene in genere utilizzata due volte.</span><span class="sxs-lookup"><span data-stu-id="054a7-234">However, when column data is of unknown size, this call is typically used twice.</span></span> <span data-ttu-id="054a7-235">Viene chiamato per primo per determinare le dimensioni dei dati in modo da poter allocare lo spazio di archiviazione necessario.</span><span class="sxs-lookup"><span data-stu-id="054a7-235">It is called first to determine the size of the data so it can allocate the necessary storage space.</span></span> <span data-ttu-id="054a7-236">Viene quindi eseguita di nuovo la stessa chiamata per recuperare i dati della colonna.</span><span class="sxs-lookup"><span data-stu-id="054a7-236">Then, the same call is made again to retrieve the column data.</span></span> <span data-ttu-id="054a7-237">Quando il numero effettivo di valori è sconosciuto, perché una colonna è multivalore, la chiamata viene in genere utilizzata tre volte.</span><span class="sxs-lookup"><span data-stu-id="054a7-237">When the actual number of values is unknown, because a column is multi-valued, the call is typically used three times.</span></span> <span data-ttu-id="054a7-238">Per prima cosa, ottenere il numero di valori e quindi due volte più per allocare spazio di archiviazione e recuperare i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="054a7-238">First to get the number of values and then twice more to allocate storage and retrieve the actual data.</span></span>

<span data-ttu-id="054a7-239">Il recupero di tutti i valori per una colonna multivalore può essere eseguito chiamando ripetutamente questa funzione con un valore pretinfo- \> itagSequence a partire da 1 e aumentando a ogni chiamata successiva.</span><span class="sxs-lookup"><span data-stu-id="054a7-239">Retrieving all the values for a multi-valued column can be done by repeatedly calling this function with a pretinfo-\>itagSequence value beginning at 1 and increasing on each subsequent call.</span></span> <span data-ttu-id="054a7-240">Il valore dell'ultima colonna è noto per essere recuperato quando una JET_wrnColumnNull viene restituita dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="054a7-240">The last column value is known to be retrieved when a JET_wrnColumnNull is returned from the function.</span></span> <span data-ttu-id="054a7-241">Si noti che questo metodo non può essere eseguito se per la colonna multivalore sono impostati valori **null** espliciti nella sequenza di valori, perché questi valori verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="054a7-241">Note that this method cannot be done if the multi-value column has explicit **NULL** values set in its value sequence, since these values would be skipped.</span></span> <span data-ttu-id="054a7-242">Se un'applicazione desidera recuperare tutti i valori di colonna multivalore, inclusi quelli impostati in modo esplicito su **null**, è necessario utilizzare [JetRetrieveColumns](./jetretrievecolumns-function.md) anziché **JetRetrieveColumn**.</span><span class="sxs-lookup"><span data-stu-id="054a7-242">If an application desires to retrieve all multi-valued column values, including those explicitly set to **NULL**, then [JetRetrieveColumns](./jetretrievecolumns-function.md) must be used instead of **JetRetrieveColumn**.</span></span> <span data-ttu-id="054a7-243">Si noti che questa funzione non restituisce il numero di valori per una funzione multivalore quando viene specificato un valore *itagSequence* pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="054a7-243">Note that this function does not return the number of values for a multi-valued function when an *itagSequence* value of 0 (zero) is given.</span></span> <span data-ttu-id="054a7-244">Solo [JetRetrieveColumns](./jetretrievecolumns-function.md) restituirà il numero di valori di un valore di colonna quando viene passato un valore *itagSequence* pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="054a7-244">Only [JetRetrieveColumns](./jetretrievecolumns-function.md) will return the number of values of a column value when an *itagSequence* value of 0 (zero) is passed.</span></span>

<span data-ttu-id="054a7-245">Se questa funzione viene chiamata a livello di transazione 0 (zero), ad esempio, la sessione chiamante non si trova in una transazione, una transazione viene aperta e chiusa all'interno della funzione.</span><span class="sxs-lookup"><span data-stu-id="054a7-245">If this function is called at transaction level 0 (zero), for example, the calling session is not itself in a transaction, then a transaction is opened and closed within the function.</span></span> <span data-ttu-id="054a7-246">Lo scopo è quello di restituire risultati coerenti nel caso in cui un valore Long estenda le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="054a7-246">The purpose of this is to return consistent results in the case that a long value spans database pages.</span></span> <span data-ttu-id="054a7-247">Si noti che la transazione viene rilasciata tra le chiamate di funzione e una serie di chiamate a questa funzione quando la sessione non è in una transazione può restituire dati aggiornati dopo la prima chiamata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="054a7-247">Note that the transaction is released between function calls and a series of calls to this function when the session is not in a transaction may return data updated after the first call to this function.</span></span>

<span data-ttu-id="054a7-248">Il valore predefinito della colonna verrà recuperato quando la colonna non è stata impostata in modo esplicito su un altro valore, a meno che non sia impostata l'opzione JET_bitRetrieveIgnoreDefault.</span><span class="sxs-lookup"><span data-stu-id="054a7-248">The default column value will be retrieved when the column has not been set explicitly to another value, unless the JET_bitRetrieveIgnoreDefault option is set.</span></span>

<span data-ttu-id="054a7-249">Il recupero del valore della colonna AutoIncrement dal buffer di copia prima dell'inserimento è un metodo comune per identificare in modo univoco un record per il collegamento quando si inseriscono dati normalizzati in più tabelle.</span><span class="sxs-lookup"><span data-stu-id="054a7-249">Retrieving the autoincrement column value from the copy buffer prior to insert is a common means of identifying a record uniquely for linkage when inserting normalized data into multiple tables.</span></span> <span data-ttu-id="054a7-250">Il valore di incremento automatico viene allocato all'inizio dell'operazione di inserimento e può essere recuperato dal buffer di copia in qualsiasi momento fino al completamento dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="054a7-250">The autoincrement value is allocated when the insert operation begins and can be retrieved from the copy buffer at any time until the update is complete.</span></span>

<span data-ttu-id="054a7-251">Quando si recuperano tutte le colonne con tag, multivalore e di tipo sparse, impostando *ColumnID* su 0 (zero), le colonne vengono recuperate nell'ordine *ColumnID* dalla *ColumnID* più bassa alla *ColumnID* più alta.</span><span class="sxs-lookup"><span data-stu-id="054a7-251">When retrieving all tagged, multi-valued, and sparse columns, by setting *columnid* to 0 (zero), columns are retrieved in *columnid* order from lowest *columnid* to highest *columnid*.</span></span> <span data-ttu-id="054a7-252">Viene restituito lo stesso ordine dei valori di colonna ogni volta che i valori delle colonne vengono recuperati.</span><span class="sxs-lookup"><span data-stu-id="054a7-252">The same order of column values is returned each time column values are retrieved.</span></span> <span data-ttu-id="054a7-253">L'ordine è deterministico.</span><span class="sxs-lookup"><span data-stu-id="054a7-253">The order is deterministic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="054a7-254">Requisiti</span><span class="sxs-lookup"><span data-stu-id="054a7-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="054a7-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="054a7-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="054a7-256">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="054a7-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="054a7-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="054a7-258">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="054a7-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-259"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="054a7-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="054a7-260">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="054a7-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054a7-261"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="054a7-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="054a7-262">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="054a7-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054a7-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="054a7-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="054a7-264">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="054a7-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="054a7-265">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="054a7-265">See Also</span></span>

[<span data-ttu-id="054a7-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="054a7-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="054a7-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="054a7-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="054a7-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="054a7-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="054a7-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="054a7-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="054a7-270">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="054a7-270">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="054a7-271">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="054a7-271">JetSetColumn</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="054a7-272">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="054a7-272">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
