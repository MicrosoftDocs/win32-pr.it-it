---
description: 'Altre informazioni su: funzione JetSetColumn'
title: Funzione JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307808"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="50b5e-103">Funzione JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="50b5e-103">JetSetColumn Function</span></span>


<span data-ttu-id="50b5e-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="50b5e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="50b5e-105">Funzione JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="50b5e-105">JetSetColumn Function</span></span>

<span data-ttu-id="50b5e-106">La funzione **JetSetColumn** modifica un valore di colonna singolo in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="50b5e-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="50b5e-107">Può sovrascrivere un valore esistente, aggiungere un nuovo valore a una sequenza di valori in una colonna multivalore, rimuovere un valore da una sequenza di valori in una colonna multivalore o aggiornare tutto o parte di un valore Long, una colonna di tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="50b5e-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="50b5e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="50b5e-108">Parameters</span></span>

<span data-ttu-id="50b5e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="50b5e-109">*sesid*</span></span>

<span data-ttu-id="50b5e-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="50b5e-110">The session to use for this call.</span></span>

<span data-ttu-id="50b5e-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="50b5e-111">*tableid*</span></span>

<span data-ttu-id="50b5e-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="50b5e-112">The cursor to use for this call.</span></span>

<span data-ttu-id="50b5e-113">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="50b5e-113">*columnid*</span></span>

<span data-ttu-id="50b5e-114">[JET_COLUMNID](./jet-columnid.md) della colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="50b5e-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="50b5e-115">In alternativa, è possibile assegnare un valore *ColumnID* pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="50b5e-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="50b5e-116">Quando viene specificato *ColumnID* 0 (zero), tutte le colonne con tag, le colonne di tipo sparse e multivalore vengono considerate come una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="50b5e-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="50b5e-117">Ciò facilita il recupero di tutte le colonne di tipo sparse presenti in un record.</span><span class="sxs-lookup"><span data-stu-id="50b5e-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="50b5e-118">*pvData*</span><span class="sxs-lookup"><span data-stu-id="50b5e-118">*pvData*</span></span>

<span data-ttu-id="50b5e-119">Buffer di input contenente i dati da utilizzare per il valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="50b5e-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="50b5e-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="50b5e-120">*cbData*</span></span>

<span data-ttu-id="50b5e-121">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="50b5e-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="50b5e-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="50b5e-122">*grbit*</span></span>

<span data-ttu-id="50b5e-123">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="50b5e-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50b5e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="50b5e-124">Value</span></span></p></th>
<th><p><span data-ttu-id="50b5e-125">Significato</span><span class="sxs-lookup"><span data-stu-id="50b5e-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="50b5e-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="50b5e-127">Questa opzione consente di accodare i dati a una colonna di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="50b5e-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="50b5e-128">È possibile ottenere lo stesso comportamento determinando la dimensione del valore Long esistente e specificando <em>ibLongValue</em> in <em>psetinfo</em>.</span><span class="sxs-lookup"><span data-stu-id="50b5e-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="50b5e-129">Tuttavia, è più semplice utilizzare questo <em>grbit</em> poiché la conoscenza delle dimensioni del valore della colonna esistente non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="50b5e-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="50b5e-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="50b5e-131">Questa opzione consente di sostituire il valore Long esistente con i dati appena forniti.</span><span class="sxs-lookup"><span data-stu-id="50b5e-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="50b5e-132">Quando si utilizza questa opzione, è come se il valore Long esistente fosse stato impostato su 0 (zero) lunghezza prima dell'impostazione dei nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="50b5e-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="50b5e-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="50b5e-134">Questa opzione è applicabile solo per le colonne con tag, sparse o multivalore.</span><span class="sxs-lookup"><span data-stu-id="50b5e-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="50b5e-135">Causa la restituzione del valore predefinito della colonna nelle successive operazioni di recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="50b5e-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="50b5e-136">Tutti i valori di colonna esistenti vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="50b5e-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="50b5e-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="50b5e-138">Questa opzione viene usata per forzare un valore Long, colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, da archiviare separatamente dal resto dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="50b5e-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="50b5e-139">Questa situazione si verifica in genere quando la dimensione del valore Long impedisce che venga archiviata con i dati dei record rimanenti.</span><span class="sxs-lookup"><span data-stu-id="50b5e-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="50b5e-140">Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore Long.</span><span class="sxs-lookup"><span data-stu-id="50b5e-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="50b5e-141">Si noti che non è possibile forzare la separazione dei valori long di quattro byte di dimensioni minori.</span><span class="sxs-lookup"><span data-stu-id="50b5e-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="50b5e-142">In questi casi, l'opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="50b5e-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="50b5e-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="50b5e-144">Questa opzione viene usata per interpretare il buffer di input come numero intero di byte da impostare come lunghezza del valore Long descritto dal <em>ColumnID</em> specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="50b5e-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="50b5e-145">Se la dimensione specificata è maggiore del valore della colonna esistente, la colonna verrà estesa con 0.</span><span class="sxs-lookup"><span data-stu-id="50b5e-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="50b5e-146">Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</span><span class="sxs-lookup"><span data-stu-id="50b5e-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="50b5e-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="50b5e-148">Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti.</span><span class="sxs-lookup"><span data-stu-id="50b5e-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="50b5e-149">Questa opzione consente di confrontare i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato.</span><span class="sxs-lookup"><span data-stu-id="50b5e-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="50b5e-150">Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLV JET_bitSetOverwriteLV e JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="50b5e-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="50b5e-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="50b5e-152">Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti.</span><span class="sxs-lookup"><span data-stu-id="50b5e-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="50b5e-153">Questa opzione Confronta la chiave di trasformazione normalizzata dei dati della colonna, ad altri valori di colonna esistenti trasformati in modo simile e viene restituito un errore se viene trovato un duplicato.</span><span class="sxs-lookup"><span data-stu-id="50b5e-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="50b5e-154">Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLV JET_bitSetOverwriteLV e JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="50b5e-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="50b5e-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="50b5e-156">Questa opzione viene utilizzata per impostare un valore su una lunghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="50b5e-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="50b5e-157">In genere, un valore di colonna è impostato su <strong>null</strong> passando un cbMax di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="50b5e-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="50b5e-158">Tuttavia, per alcuni tipi, ad esempio <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valore di colonna può essere 0 (zero) Length anziché <strong>null</strong>e questa opzione viene usata per distinguere tra <strong>null</strong> e 0 (zero) Length.</span><span class="sxs-lookup"><span data-stu-id="50b5e-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="50b5e-159"><strong>Nota</strong>  In generale, se la colonna è una colonna a lunghezza fissa, questo bit viene ignorato e la colonna viene impostata su <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="50b5e-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="50b5e-160">Tuttavia, se la colonna è una colonna con tag a lunghezza fissa, la lunghezza della colonna viene impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="50b5e-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="50b5e-161">Quando la colonna con tag a lunghezza fissa è impostata su 0, i tentativi di recuperare la colonna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> riusciranno, ma la lunghezza effettiva restituita nel parametro <em>cbActual</em> è 0.</span><span class="sxs-lookup"><span data-stu-id="50b5e-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="50b5e-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="50b5e-163">Questa opzione viene usata per archiviare l'intero valore lungo nel record.</span><span class="sxs-lookup"><span data-stu-id="50b5e-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="50b5e-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="50b5e-165">Questa opzione viene usata per tentare la compressione dei dati durante l'archiviazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="50b5e-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="50b5e-166"><strong>Windows 7:</strong>  JET_bitSetCompressed è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50b5e-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="50b5e-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="50b5e-168">Questa opzione non consente di eseguire la compressione durante l'archiviazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="50b5e-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="50b5e-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50b5e-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50b5e-170">*psetinfo*</span><span class="sxs-lookup"><span data-stu-id="50b5e-170">*psetinfo*</span></span>

<span data-ttu-id="50b5e-171">Puntatore a parametri di input facoltativi che possono essere impostati per questa funzione utilizzando la struttura [JET_SETINFO](./jet-setinfo-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="50b5e-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="50b5e-172">Se *psetinfo* viene specificato come **null** , la funzione si comporta come se venisse assegnato un *itagSequence* di 1 e un *ibLongValue* di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="50b5e-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="50b5e-173">In questo modo column set imposta il primo valore di una colonna multivalore e imposta i dati lunghi a partire dall'offset 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="50b5e-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="50b5e-174">Per questo parametro è possibile impostare le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="50b5e-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50b5e-175">Valore</span><span class="sxs-lookup"><span data-stu-id="50b5e-175">Value</span></span></p></th>
<th><p><span data-ttu-id="50b5e-176">Significato</span><span class="sxs-lookup"><span data-stu-id="50b5e-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-177">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="50b5e-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="50b5e-178">Offset binario in un valore di colonna lungo in cui devono iniziare i dati impostati.</span><span class="sxs-lookup"><span data-stu-id="50b5e-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-179">itagSequence</span><span class="sxs-lookup"><span data-stu-id="50b5e-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="50b5e-180">Numero di sequenza del valore della colonna multivalore desiderato da impostare.</span><span class="sxs-lookup"><span data-stu-id="50b5e-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="50b5e-181">Se <em>itagSequence</em> è impostato su 0 (zero), il valore specificato deve essere aggiunto alla fine della sequenza di valori multivalore.</span><span class="sxs-lookup"><span data-stu-id="50b5e-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="50b5e-182">Se il numero di sequenza specificato è maggiore dell'ultimo valore multivalore esistente, il valore specificato viene aggiunto alla fine della sequenza di valori.</span><span class="sxs-lookup"><span data-stu-id="50b5e-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="50b5e-183">Se il numero di sequenza corrisponde a un valore esistente, il valore viene sostituito con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="50b5e-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="50b5e-184">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50b5e-184">Return Value</span></span>

<span data-ttu-id="50b5e-185">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="50b5e-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="50b5e-186">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="50b5e-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50b5e-187">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="50b5e-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="50b5e-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50b5e-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="50b5e-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="50b5e-190">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="50b5e-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="50b5e-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="50b5e-192">L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="50b5e-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="50b5e-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="50b5e-194">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="50b5e-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="50b5e-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="50b5e-196">La colonna descritta dal <em>ColumnID</em> specificato non esiste nella tabella.</span><span class="sxs-lookup"><span data-stu-id="50b5e-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="50b5e-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="50b5e-198">È stato effettuato un tentativo non valido di aggiornare un valore Long durante un'operazione di eliminazione dell'aggiornamento originale della copia di inserimento.</span><span class="sxs-lookup"><span data-stu-id="50b5e-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="50b5e-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="50b5e-200">I dati del valore di colonna specificati nel buffer di input superano il limite di dimensione naturale per una colonna a lunghezza fissa o sono configurati per colonne di tipo text o binary a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="50b5e-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="50b5e-201">Questo errore viene restituito anche quando si passano più di 1024 byte di dati per una colonna estesa e si imposta il flag di JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="50b5e-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="50b5e-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="50b5e-203">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="50b5e-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="50b5e-204"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="50b5e-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="50b5e-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="50b5e-206">La dimensione dei dati del valore della colonna specificata non corrisponde a quanto è naturale per il tipo di dati a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="50b5e-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="50b5e-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="50b5e-208">È stato effettuato un tentativo non valido di aggiornare una colonna con incremento automatico durante un'operazione di inserimento o aggiornamento oppure di aggiornare una colonna della versione durante un'operazione di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="50b5e-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="50b5e-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="50b5e-210">Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</span><span class="sxs-lookup"><span data-stu-id="50b5e-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="50b5e-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="50b5e-212">Il valore di psetinfo- &gt; cbStruct specificato non è una dimensione valida per la struttura <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="50b5e-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="50b5e-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="50b5e-214">L'operazione set Column ha tentato di creare un valore duplicato e ha specificato JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="50b5e-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="50b5e-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="50b5e-216">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="50b5e-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="50b5e-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="50b5e-218">È stato effettuato un tentativo non valido di aggiornare un valore di colonna lungo quando la sessione chiamante non era presente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="50b5e-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="50b5e-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="50b5e-220">È stato effettuato un tentativo non valido di impostare una colonna non<strong>null</strong> su <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="50b5e-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="50b5e-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="50b5e-222">Uguale a JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="50b5e-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="50b5e-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="50b5e-224">Il valore della colonna non può essere impostato sul valore nel buffer di input perché avrebbe causato il superamento del limite di dimensioni relative alle dimensioni della pagina.</span><span class="sxs-lookup"><span data-stu-id="50b5e-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="50b5e-225">Le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> possono essere archiviate separatamente dai dati rimanenti del record.</span><span class="sxs-lookup"><span data-stu-id="50b5e-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="50b5e-226">Tuttavia, altre colonne devono essere archiviate con il record e possono causare il superamento del limite delle dimensioni del record.</span><span class="sxs-lookup"><span data-stu-id="50b5e-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="50b5e-227">Anche le colonne lunghe richiedono 5 byte di spazio all'interno del record come collegamento e questo può comportare la restituzione di JET_errRecordTooBig.</span><span class="sxs-lookup"><span data-stu-id="50b5e-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="50b5e-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="50b5e-229">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="50b5e-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="50b5e-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="50b5e-231">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="50b5e-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="50b5e-232"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="50b5e-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="50b5e-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="50b5e-234">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="50b5e-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="50b5e-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="50b5e-236">Il cursore non è attualmente in fase di inserimento di un nuovo record o di aggiornamento di un record esistente.</span><span class="sxs-lookup"><span data-stu-id="50b5e-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="50b5e-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="50b5e-238">Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="50b5e-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="50b5e-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="50b5e-240">Il valore della colonna nel buffer di input supera la lunghezza massima configurata per una colonna a lunghezza variabile ed è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="50b5e-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50b5e-241">In seguito all'esito positivo, la parte desiderata di un valore di colonna per la colonna specificata viene impostata con i dati copiati dal buffer di input.</span><span class="sxs-lookup"><span data-stu-id="50b5e-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="50b5e-242">Il set di dati potrebbe essere stato troncato se è stata superata la lunghezza massima specificata per una colonna a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="50b5e-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="50b5e-243">In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato di valore di colonna viene aggiornato nel buffer di copia.</span><span class="sxs-lookup"><span data-stu-id="50b5e-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50b5e-244">Commenti</span><span class="sxs-lookup"><span data-stu-id="50b5e-244">Remarks</span></span>

<span data-ttu-id="50b5e-245">L'impostazione di valori Long, valori per le colonne [JET_coltypLongBinary](./jet-coltyp.md) di tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md), deve essere eseguita solo quando la sessione chiamante si trova in una transazione.</span><span class="sxs-lookup"><span data-stu-id="50b5e-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="50b5e-246">Se la sessione chiamante non si trova in una transazione, è possibile eseguire il commit completo delle modifiche apportate ai valori Long archiviati separatamente, anche quando l'operazione di aggiornamento viene annullata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="50b5e-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="50b5e-247">Se la sessione chiamante si trova in una transazione, è possibile eseguire il rollback completo degli effetti dell'aggiornamento annullando l'aggiornamento ed eseguendo il rollback della transazione di sessione.</span><span class="sxs-lookup"><span data-stu-id="50b5e-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="50b5e-248">Gli aggiornamenti dell'indice non vengono eseguiti come risultato delle operazioni di **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="50b5e-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="50b5e-249">Gli indici vengono invece aggiornati solo dopo il completamento di tutte le modifiche apportate alle colonne e viene chiamato [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="50b5e-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="50b5e-250">Ciò consente di aggiornare più efficacemente gli indici quando gli indici coinvolgono più di una colonna da modificare.</span><span class="sxs-lookup"><span data-stu-id="50b5e-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="50b5e-251">Le dimensioni di un record sono limitate in base alle dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="50b5e-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="50b5e-252">Tutti i valori Long nel record di dimensioni maggiori di cinque byte verranno archiviati separatamente dal record qualora i dati nel record superino il limite risultante da un'operazione **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="50b5e-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="50b5e-253">Il JET_errRecordTooBig di errore viene restituito solo dopo che tutti i dati della colonna di record separabili sono stati archiviati separatamente dal record e il record supera ancora il limite delle dimensioni dei record.</span><span class="sxs-lookup"><span data-stu-id="50b5e-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="50b5e-254">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50b5e-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="50b5e-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="50b5e-256">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="50b5e-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="50b5e-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="50b5e-258">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="50b5e-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-259"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="50b5e-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="50b5e-260">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="50b5e-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b5e-261"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="50b5e-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="50b5e-262">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="50b5e-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b5e-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="50b5e-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="50b5e-264">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="50b5e-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="50b5e-265">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="50b5e-265">See Also</span></span>

[<span data-ttu-id="50b5e-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="50b5e-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="50b5e-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="50b5e-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="50b5e-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="50b5e-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="50b5e-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="50b5e-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="50b5e-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="50b5e-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="50b5e-271">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="50b5e-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="50b5e-272">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="50b5e-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
