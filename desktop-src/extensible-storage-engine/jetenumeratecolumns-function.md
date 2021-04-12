---
description: 'Altre informazioni su: funzione JetEnumerateColumns'
title: Funzione JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232557"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="10cf5-103">Funzione JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="10cf5-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="10cf5-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="10cf5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="10cf5-105">Funzione JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="10cf5-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="10cf5-106">La funzione **JetEnumerateColumns** recupera in modo efficiente un set di colonne e i relativi valori dal record corrente di un cursore o dal buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="10cf5-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="10cf5-107">Le colonne e i valori recuperati possono essere limitati da un elenco di ID di colonna, numeri *itagSequence* e altre caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="10cf5-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="10cf5-108">Questa API di recupero colonne è univoca in quanto restituisce informazioni nella memoria allocata in modo dinamico, ottenuta usando un callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="10cf5-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="10cf5-109">Questa nuova flessibilità consente di recuperare in modo efficiente i dati delle colonne con caratteristiche specifiche, ad esempio le dimensioni e la molteplicità, sconosciute al chiamante.</span><span class="sxs-lookup"><span data-stu-id="10cf5-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="10cf5-110">In questo modo si elimina la necessità di usare le modalità di individuazione di [JetRetrieveColumn](./jetretrievecolumn-function.md) per determinare tali caratteristiche per configurare una chiamata finale a [JetRetrieveColumn](./jetretrievecolumn-function.md) che recupererà correttamente i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="10cf5-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="10cf5-111">**Windows XP: JetEnumerateColumns** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10cf5-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="10cf5-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="10cf5-112">Parameters</span></span>

<span data-ttu-id="10cf5-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="10cf5-113">*sesid*</span></span>

<span data-ttu-id="10cf5-114">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="10cf5-114">The session to use for this call.</span></span>

<span data-ttu-id="10cf5-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="10cf5-115">*tableid*</span></span>

<span data-ttu-id="10cf5-116">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="10cf5-116">The cursor to use for this call.</span></span>

<span data-ttu-id="10cf5-117">*cEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="10cf5-117">*cEnumColumnId*</span></span>

<span data-ttu-id="10cf5-118">Matrice di ID di colonna, ognuno con una matrice facoltativa di numeri *itagSequence* da enumerare.</span><span class="sxs-lookup"><span data-stu-id="10cf5-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="10cf5-119">Se *cEnumColumnId* è 0 (zero), *rgEnumColumnId* viene ignorato e tutti i valori di colonna vengono enumerati e restituiti al chiamante.</span><span class="sxs-lookup"><span data-stu-id="10cf5-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="10cf5-120">Se un elemento della matrice di ID di colonna fa riferimento a un ID di colonna pari a 0 (zero), l'enumerazione di tale colonna viene ignorata e viene generato uno slot corrispondente nell'output con lo stato della colonna JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="10cf5-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="10cf5-121">Se *ctagSequence* è 0 (zero) per un determinato elemento della matrice di ID di colonna, *rgtagSequence* viene ignorato e tutti i valori di colonna per l'ID di tale colonna vengono enumerati e restituiti al chiamante.</span><span class="sxs-lookup"><span data-stu-id="10cf5-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="10cf5-122">Se un elemento di una matrice di numeri *itagSequence* fa riferimento a un numero *itagSequence* pari a 0 (zero), l'enumerazione di tale numero *itagSequence* viene ignorata e viene generato uno slot corrispondente nell'output con lo stato del valore della colonna JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="10cf5-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="10cf5-123">*rgEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="10cf5-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="10cf5-124">Vedere *cEnumColumnId*.</span><span class="sxs-lookup"><span data-stu-id="10cf5-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="10cf5-125">*pcEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="10cf5-125">*pcEnumColumn*</span></span>

<span data-ttu-id="10cf5-126">Restituisce la matrice enumerata di colonne e i relativi valori nella memoria allocata tramite il callback compatibile con *itagSequence* fornito.</span><span class="sxs-lookup"><span data-stu-id="10cf5-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="10cf5-127">Se per l'input viene richiesta una matrice di ID di colonna, l'ordine e le dimensioni della matrice di output riflettono l'ordine e le dimensioni della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="10cf5-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="10cf5-128">Analogamente, se viene richiesta una matrice di numeri *itagSequence* per un determinato ID di colonna nell'input, l'ordine e le dimensioni della matrice di output dei valori di colonna per tale colonna rifletteranno l'ordine e le dimensioni della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="10cf5-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="10cf5-129">I parametri di output vengono impostati su 0 (zero) e **null** in caso di errore, ad eccezione di JET_errBadColumnId e JET_errColumnNotFound.</span><span class="sxs-lookup"><span data-stu-id="10cf5-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="10cf5-130">Quando vengono restituiti questi errori, i dati di output sono validi e completi per tutti gli ID di colonna interessati.</span><span class="sxs-lookup"><span data-stu-id="10cf5-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="10cf5-131">Il codice di stato per ogni ID di colonna interessato viene impostato su uno di questi errori, in modo che il chiamante possa determinare quali ID di colonna erano negativi e potenzialmente eseguire un'azione correttiva.</span><span class="sxs-lookup"><span data-stu-id="10cf5-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="10cf5-132">*prgEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="10cf5-132">*prgEnumColumn*</span></span>

<span data-ttu-id="10cf5-133">Vedere *pcEnumColumn*.</span><span class="sxs-lookup"><span data-stu-id="10cf5-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="10cf5-134">*pfnRealloc*</span><span class="sxs-lookup"><span data-stu-id="10cf5-134">*pfnRealloc*</span></span>

<span data-ttu-id="10cf5-135">Identifica un callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) e un puntatore di contesto facoltativo usato per allocare memoria per la matrice di output di colonne e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="10cf5-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="10cf5-136">*pvReallocContext*</span><span class="sxs-lookup"><span data-stu-id="10cf5-136">*pvReallocContext*</span></span>

<span data-ttu-id="10cf5-137">Vedere *pfnRealloc*.</span><span class="sxs-lookup"><span data-stu-id="10cf5-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="10cf5-138">*cbDataMost*</span><span class="sxs-lookup"><span data-stu-id="10cf5-138">*cbDataMost*</span></span>

<span data-ttu-id="10cf5-139">Imposta un limite per la quantità di dati da restituire da un testo lungo o una colonna binaria di tipo Long.</span><span class="sxs-lookup"><span data-stu-id="10cf5-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="10cf5-140">Questo parametro può essere utilizzato per impedire l'enumerazione di un valore di colonna estremamente grande.</span><span class="sxs-lookup"><span data-stu-id="10cf5-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="10cf5-141">In genere, tale enumerazione potrebbe non riuscire a eseguire la chiamata API con JET_errOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="10cf5-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="10cf5-142">Se un valore di colonna di grandi dimensioni viene troncato in questo modo, lo stato del valore della colonna sarà JET_wrnColumnTruncated.</span><span class="sxs-lookup"><span data-stu-id="10cf5-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="10cf5-143">*grbit*</span><span class="sxs-lookup"><span data-stu-id="10cf5-143">*grbit*</span></span>

<span data-ttu-id="10cf5-144">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="10cf5-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10cf5-145">Valore</span><span class="sxs-lookup"><span data-stu-id="10cf5-145">Value</span></span></p></th>
<th><p><span data-ttu-id="10cf5-146">Significato</span><span class="sxs-lookup"><span data-stu-id="10cf5-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="10cf5-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="10cf5-148">Quando si enumerano i valori di colonna, tutte le colonne per cui si recuperano tutti i valori e con un solo valore di colonna non NULL possono essere restituite in formato compresso.</span><span class="sxs-lookup"><span data-stu-id="10cf5-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="10cf5-149">Lo stato di tali colonne verrà impostato su JET_wrnColumnSingleValue e la dimensione del valore della colonna e della memoria che contiene il valore della colonna verrà restituita direttamente nella struttura di <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="10cf5-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="10cf5-150">Non è garantito che tutte le colonne idonee vengano compresse in questo modo.</span><span class="sxs-lookup"><span data-stu-id="10cf5-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="10cf5-151">Per ulteriori informazioni, vedere <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="10cf5-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="10cf5-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="10cf5-153">Questa opzione indica che è necessario enumerare i valori di colonna modificati del record anziché i valori di colonna originali.</span><span class="sxs-lookup"><span data-stu-id="10cf5-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="10cf5-154">Se il valore di una colonna non è stato modificato, il valore della colonna originale viene enumerato.</span><span class="sxs-lookup"><span data-stu-id="10cf5-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="10cf5-155">In questo modo, è possibile enumerare un valore di colonna che non è ancora stato inserito o aggiornato durante l'inserimento o l'aggiornamento di un record.</span><span class="sxs-lookup"><span data-stu-id="10cf5-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="10cf5-156">Questa opzione è identica a JET_bitRetrieveCopy se utilizzata con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span><span class="sxs-lookup"><span data-stu-id="10cf5-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="10cf5-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="10cf5-158">Se una colonna specificata non è presente nel record, non verrà restituito alcun valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="10cf5-159">In genere, il valore predefinito per la colonna, se presente, verrebbe restituito in questo caso.</span><span class="sxs-lookup"><span data-stu-id="10cf5-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="10cf5-160">Si garantisce che se la colonna è impostata su un valore diverso da quello predefinito, verrà restituito un valore diverso, ovvero se una colonna con un valore predefinito viene impostata in modo esplicito su <strong>null</strong> , verrà restituito un valore <strong>null</strong> come valore per la colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="10cf5-161">Si noti che, anche se questa opzione è richiesta, è comunque possibile visualizzare un valore di colonna che corrisponde al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="10cf5-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="10cf5-162">Non viene effettuato alcun tentativo di rimuovere i valori di colonna che corrispondono ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="10cf5-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="10cf5-163">È importante notare che questa opzione influisca sull'output di <strong>JetEnumerateColumns</strong> quando viene usato con JET_bitEnumeratePresenceOnly o JET_bitEnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="10cf5-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="10cf5-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="10cf5-165">Se una colonna specificata non è presente nel record e presenta un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="10cf5-166">Questa opzione impedisce al callback che calcola il valore predefinito definito dall'utente per la colonna di essere chiamato durante l'enumerazione dei valori per la colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="10cf5-167"><strong>Windows Server 2003 e versioni precedenti:  </strong> Per Windows Server 2003 e versioni precedenti, l'operazione avrà esito negativo con JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="10cf5-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="10cf5-168"><strong>Windows Server 2003 SP1:  </strong> Questo possibile valore è disponibile solo per i sistemi operativi Windows Server 2003 SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="10cf5-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="10cf5-169">Se questo valore può essere specificato e la tabella contiene una colonna con un valore predefinito definito dall'utente, l'operazione avrà esito negativo con JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="10cf5-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="10cf5-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="10cf5-171">Se è presente un valore non NULL per il valore della colonna o della colonna richiesta, i dati associati non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="10cf5-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="10cf5-172">Lo stato associato per quel valore di colonna o colonna verrà invece impostato su JET_wrnColumnPresent.</span><span class="sxs-lookup"><span data-stu-id="10cf5-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="10cf5-173">Se il valore della colonna o della colonna è <strong>null</strong> , JET_wrnColumnNull verrà restituito come di consueto.</span><span class="sxs-lookup"><span data-stu-id="10cf5-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="10cf5-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="10cf5-175">Quando si enumerano tutti i valori di colonna nel record, ad esempio quando <em>cEnumColumnId</em> è zero, verranno restituiti solo i valori delle colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="10cf5-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="10cf5-176">Questa opzione non è consentita durante l'enumerazione di una matrice di ID di colonna specifica.</span><span class="sxs-lookup"><span data-stu-id="10cf5-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="10cf5-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="10cf5-178"><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10cf5-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="10cf5-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10cf5-179">Return Value</span></span>

<span data-ttu-id="10cf5-180">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="10cf5-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="10cf5-181">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="10cf5-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10cf5-182">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="10cf5-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="10cf5-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10cf5-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="10cf5-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="10cf5-185">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="10cf5-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="10cf5-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="10cf5-187">L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="10cf5-188">Questo errore viene restituito da <strong>JetEnumerateColumns</strong> se sono stati richiesti ID di colonna specifici, uno di questi ID di colonna non è valido e il primo ID di colonna non è riuscito con questo errore per il codice di stato della colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="10cf5-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="10cf5-190">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="10cf5-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="10cf5-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="10cf5-192">La colonna descritta dall'ID colonna specificato non esiste nella tabella.</span><span class="sxs-lookup"><span data-stu-id="10cf5-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="10cf5-193">Questo errore viene restituito da <strong>JetEnumerateColumns</strong> se sono stati richiesti ID di colonna specifici, uno di questi ID di colonna non è valido e il primo ID di colonna non è riuscito con questo errore per il codice di stato della colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="10cf5-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="10cf5-195">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="10cf5-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="10cf5-196"><strong>Windows XP:  </strong> Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="10cf5-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="10cf5-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="10cf5-198">Una delle opzioni richieste non è valida o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="10cf5-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="10cf5-199">Questo errore viene restituito da <strong>JetEnumerateColumns</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="10cf5-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="10cf5-200">JET_bitEnumerateLocal specificato.</span><span class="sxs-lookup"><span data-stu-id="10cf5-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="10cf5-201">È stato specificato un <em>grbit</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="10cf5-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="10cf5-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="10cf5-203">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="10cf5-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="10cf5-204">Questo errore viene restituito da <strong>JetEnumerateColumns</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="10cf5-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="10cf5-205"><em>pcEnumColumn</em> è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="10cf5-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="10cf5-206"><em>prgEnumColumn</em> è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="10cf5-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="10cf5-207"><em>pfnRealloc</em> è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="10cf5-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="10cf5-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="10cf5-209">Il cursore non è posizionato in corrispondenza di un record.</span><span class="sxs-lookup"><span data-stu-id="10cf5-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="10cf5-210">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="10cf5-210">This can happen for many different reasons.</span></span> <span data-ttu-id="10cf5-211">Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="10cf5-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="10cf5-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="10cf5-213">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="10cf5-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="10cf5-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="10cf5-215">Il cursore è posizionato in corrispondenza di un record che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="10cf5-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="10cf5-216">I motivi possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="10cf5-216">This can happen for many different reasons.</span></span> <span data-ttu-id="10cf5-217">Il motivo più comune è che la sessione non è in una transazione, il cursore è stato posizionato in corrispondenza di un record, tale record è stato eliminato e quindi il cursore ha tentato di fare riferimento a tale record.</span><span class="sxs-lookup"><span data-stu-id="10cf5-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="10cf5-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="10cf5-219">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="10cf5-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="10cf5-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="10cf5-221">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="10cf5-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="10cf5-222"><strong>Windows XP:  </strong> Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="10cf5-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="10cf5-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="10cf5-224">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="10cf5-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10cf5-225">In seguito all'esito positivo, i dati richiesti verranno restituiti nei buffer di output.</span><span class="sxs-lookup"><span data-stu-id="10cf5-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="10cf5-226">È responsabilità del chiamante liberare la memoria allocata da questo callback e restituita nei buffer di output.</span><span class="sxs-lookup"><span data-stu-id="10cf5-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="10cf5-227">Tale memoria deve essere liberata tramite il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito.</span><span class="sxs-lookup"><span data-stu-id="10cf5-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="10cf5-228">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="10cf5-228">No change to the database state will occur.</span></span>

<span data-ttu-id="10cf5-229">In caso di errore, non verrà restituito alcun dato richiesto.</span><span class="sxs-lookup"><span data-stu-id="10cf5-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="10cf5-230">Qualsiasi memoria allocata durante la chiamata verrà liberata automaticamente utilizzando il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito.</span><span class="sxs-lookup"><span data-stu-id="10cf5-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="10cf5-231">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="10cf5-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="10cf5-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="10cf5-232">Remarks</span></span>

<span data-ttu-id="10cf5-233">Se si enumerano tutti i valori di colonna nel record e non è stato specificato JET_bitEnumerateIgnoreDefaults, non è possibile presupporre che non venga mai visualizzato un valore di colonna o di colonna con un codice di stato JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="10cf5-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="10cf5-234">Questo codice di stato può essere visualizzato se una colonna ha un valore predefinito ed è stata impostata in modo esplicito su **null** o se la colonna è una colonna non di tipo sparse, ad esempio una colonna fissa o variabile.</span><span class="sxs-lookup"><span data-stu-id="10cf5-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="10cf5-235">Il parametro *cbDataMost* non è applicabile a tutti i valori di colonna.</span><span class="sxs-lookup"><span data-stu-id="10cf5-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="10cf5-236">Questo parametro consente di troncare solo i valori long text e long Column Binary che sono così grandi che sono stati archiviati separatamente dal record.</span><span class="sxs-lookup"><span data-stu-id="10cf5-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="10cf5-237">Se **JetEnumerateColumns** restituisce i dati nei parametri di output, il chiamante è responsabile della liberazione della memoria nell'array e della memoria a cui fanno riferimento i puntatori incorporati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="10cf5-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="10cf5-238">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10cf5-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-239"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="10cf5-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="10cf5-240">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10cf5-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-241"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="10cf5-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="10cf5-242">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="10cf5-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-243"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="10cf5-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="10cf5-244">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="10cf5-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10cf5-245"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="10cf5-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="10cf5-246">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="10cf5-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10cf5-247"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="10cf5-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="10cf5-248">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="10cf5-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="10cf5-249">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="10cf5-249">See Also</span></span>

[<span data-ttu-id="10cf5-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="10cf5-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="10cf5-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="10cf5-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="10cf5-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="10cf5-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="10cf5-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="10cf5-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="10cf5-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="10cf5-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="10cf5-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="10cf5-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="10cf5-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="10cf5-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="10cf5-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="10cf5-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="10cf5-258">realloc</span><span class="sxs-lookup"><span data-stu-id="10cf5-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="10cf5-259">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="10cf5-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="10cf5-260">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="10cf5-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
