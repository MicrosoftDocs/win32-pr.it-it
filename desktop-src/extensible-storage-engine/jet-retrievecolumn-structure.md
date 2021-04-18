---
description: 'Altre informazioni su: struttura JET_RETRIEVECOLUMN'
title: Struttura JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308028"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="d5b5d-103">Struttura JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d5b5d-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="d5b5d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d5b5d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="d5b5d-105">Struttura JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d5b5d-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="d5b5d-106">La struttura **JET_RETRIEVECOLUMN** contiene i parametri di input e di output per [JetRetrieveColumns](./jetretrievecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5b5d-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="d5b5d-107">I campi della struttura descrivono il valore della colonna da recuperare, il modo in cui recuperarlo e il percorso in cui salvare i risultati.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="d5b5d-108">Membri</span><span class="sxs-lookup"><span data-stu-id="d5b5d-108">Members</span></span>

<span data-ttu-id="d5b5d-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-109">**columnid**</span></span>

<span data-ttu-id="d5b5d-110">Identificatore di colonna per la colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="d5b5d-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-111">**pvData**</span></span>

<span data-ttu-id="d5b5d-112">Puntatore per iniziare a archiviare i dati recuperati dal valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="d5b5d-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-113">**cbData**</span></span>

<span data-ttu-id="d5b5d-114">Dimensione dell'allocazione a partire da **pvData**, in byte.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="d5b5d-115">Tramite l'operazione di recupero colonna non vengono archiviati più dati in **pvData** rispetto a **cbData**.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="d5b5d-116">**cbActual**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-116">**cbActual**</span></span>

<span data-ttu-id="d5b5d-117">Dimensione, in byte, dei dati recuperati da un'operazione di recupero colonna.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="d5b5d-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-118">**grbit**</span></span>

<span data-ttu-id="d5b5d-119">Gruppo di bit che contiene le opzioni per il recupero di colonne, che includono zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5b5d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d5b5d-120">Value</span></span></p></th>
<th><p><span data-ttu-id="d5b5d-121">Significato</span><span class="sxs-lookup"><span data-stu-id="d5b5d-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5b5d-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="d5b5d-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-123">Recupera il valore modificato anziché il valore originale.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="d5b5d-124">Se il valore non è stato modificato, viene recuperato il valore originale.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="d5b5d-125">In questo modo, è possibile recuperare un valore che non è ancora stato inserito o aggiornato quando si inserisce o si aggiorna un record.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5b5d-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="d5b5d-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-127">Recupera i valori di colonna dall'indice senza accedere al record, se possibile.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="d5b5d-128">In questo modo, è possibile evitare il caricamento di record superflui quando sono disponibili dati necessari dalle voci dell'indice.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="d5b5d-129">Nei casi in cui non è possibile recuperare il valore della colonna originale dall'indice a causa di trasformazioni irreversibili o troncamenti dei dati, il record sarà accessibile e i dati verranno recuperati normalmente.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="d5b5d-130">Si tratta di un'opzione relativa alle prestazioni e deve essere specificata solo quando è probabile che il valore della colonna possa essere recuperato dall'indice.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="d5b5d-131">Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster, perché le voci di indice per l'indice cluster o primario sono i record stessi.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="d5b5d-132">Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromPrimaryBookmark.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5b5d-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="d5b5d-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-134">Recupera i valori di colonna dal segnalibro dell'indice e può essere diverso dal valore di indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="d5b5d-135">Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="d5b5d-136">Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5b5d-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="d5b5d-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-138">Recupera il numero di sequenza di un valore di colonna multivalore in pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="d5b5d-139">Il campo itagSequence viene spesso usato come input per il recupero di valori di colonna multivalore da un record.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="d5b5d-140">Tuttavia, quando si recuperano i valori da un indice, è anche possibile associare la voce di indice a un determinato numero di sequenza e recuperare anche questo numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="d5b5d-141">Il recupero del numero di sequenza può essere un'operazione costosa e deve essere eseguito solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5b5d-142">JET_ bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="d5b5d-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-143">Recupera i valori NULL della colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="d5b5d-144">Se questa opzione non è specificata, i valori NULL della colonna multivalore verranno automaticamente ignorati.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5b5d-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="d5b5d-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-146">Causa la restituzione di un valore NULL quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="d5b5d-147">Questa opzione ha effetto solo sulle colonne multivalore.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5b5d-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="d5b5d-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-149">Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5b5d-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="d5b5d-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="d5b5d-151">Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5b5d-152">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-152">**ibLongValue**</span></span>

<span data-ttu-id="d5b5d-153">Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d5b5d-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="d5b5d-154">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-154">**itagSequence**</span></span>

<span data-ttu-id="d5b5d-155">Numero di sequenza dei valori contenuti in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="d5b5d-156">**itagSequence** qui nell' **JET_RETRIEVECOLUMN** può essere 0.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="d5b5d-157">Se **itagSequence** è 0, viene restituito il numero di istanze di una colonna multivalore anziché dati di colonna.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="d5b5d-158">Non è possibile usare un valore **itagSequence** pari a 0 nelle chiamate a [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5b5d-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="d5b5d-159">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-159">**columnidNextTagged**</span></span>

<span data-ttu-id="d5b5d-160">**ColumnID** della colonna contrassegnata, multivalore o di tipo sparse quando tutte le colonne con tag vengono recuperate passando 0 come **ColumnID** a [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="d5b5d-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="d5b5d-161">**Err**</span><span class="sxs-lookup"><span data-stu-id="d5b5d-161">**err**</span></span>

<span data-ttu-id="d5b5d-162">Codici di errore e avvisi restituiti dal recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="d5b5d-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5b5d-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5b5d-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d5b5d-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d5b5d-165">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5b5d-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d5b5d-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d5b5d-167">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5b5d-168"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="d5b5d-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d5b5d-169">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d5b5d-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d5b5d-170">See Also</span></span>

[<span data-ttu-id="d5b5d-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="d5b5d-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="d5b5d-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d5b5d-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d5b5d-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d5b5d-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d5b5d-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d5b5d-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d5b5d-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d5b5d-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="d5b5d-176">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d5b5d-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="d5b5d-177">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="d5b5d-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
