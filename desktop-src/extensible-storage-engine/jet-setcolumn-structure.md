---
description: 'Altre informazioni su: struttura JET_SETCOLUMN'
title: Struttura JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750519"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="e62be-103">Struttura JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e62be-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="e62be-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e62be-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="e62be-105">Struttura JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e62be-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="e62be-106">La struttura **JET_SETCOLUMN** contiene i parametri di input e di output per [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="e62be-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="e62be-107">I campi della struttura descrivono il valore della colonna da impostare, come impostarlo e dove ottenere i dati del set di colonne.</span><span class="sxs-lookup"><span data-stu-id="e62be-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="e62be-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e62be-108">Members</span></span>

<span data-ttu-id="e62be-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="e62be-109">**columnid**</span></span>

<span data-ttu-id="e62be-110">Identificatore di colonna per una colonna da impostare.</span><span class="sxs-lookup"><span data-stu-id="e62be-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="e62be-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="e62be-111">**pvData**</span></span>

<span data-ttu-id="e62be-112">Puntatore ai dati da impostare in una colonna.</span><span class="sxs-lookup"><span data-stu-id="e62be-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="e62be-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="e62be-113">**cbData**</span></span>

<span data-ttu-id="e62be-114">Dimensione dell'allocazione, in byte, a partire da **pvData** in byte.</span><span class="sxs-lookup"><span data-stu-id="e62be-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="e62be-115">**grbit**</span><span class="sxs-lookup"><span data-stu-id="e62be-115">**grbit**</span></span>

<span data-ttu-id="e62be-116">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e62be-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e62be-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e62be-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e62be-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e62be-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e62be-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="e62be-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="e62be-120">Accoda i dati a una colonna di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="e62be-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="e62be-121">È possibile ottenere lo stesso comportamento determinando la dimensione del valore Long esistente e specificando <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span><span class="sxs-lookup"><span data-stu-id="e62be-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="e62be-122">Tuttavia, è più semplice usare questo <em>grbit</em>, poiché la conoscenza delle dimensioni del valore della colonna esistente non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="e62be-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e62be-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="e62be-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="e62be-124">Sostituisce il valore Long esistente con i nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="e62be-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="e62be-125">Quando si utilizza questa opzione, è come se il valore Long esistente fosse stato impostato su 0 (zero) lunghezza prima dell'impostazione dei nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="e62be-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e62be-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="e62be-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="e62be-127">Interpreta il buffer di input come numero intero di byte da impostare come lunghezza del valore Long descritto dal ColumnID specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="e62be-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="e62be-128">Se la dimensione specificata è maggiore del valore della colonna esistente, la colonna verrà estesa con 0.</span><span class="sxs-lookup"><span data-stu-id="e62be-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="e62be-129">Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</span><span class="sxs-lookup"><span data-stu-id="e62be-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e62be-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="e62be-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="e62be-131">Imposta un valore di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="e62be-131">Sets a value to zero length.</span></span> <span data-ttu-id="e62be-132">In genere, un valore di colonna è impostato su NULL passando un cbMax di 0.</span><span class="sxs-lookup"><span data-stu-id="e62be-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="e62be-133">Tuttavia, per alcuni tipi, ad esempio <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valore di colonna può essere di lunghezza 0 anziché null e questa opzione viene utilizzata per distinguere la lunghezza tra null e 0.</span><span class="sxs-lookup"><span data-stu-id="e62be-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e62be-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="e62be-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="e62be-135">Forza un valore Long, le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, da archiviare separatamente dal resto dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="e62be-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="e62be-136">Questa situazione si verifica in genere quando la dimensione del valore Long impedisce che venga archiviata con i dati dei record rimanenti.</span><span class="sxs-lookup"><span data-stu-id="e62be-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="e62be-137">Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore Long.</span><span class="sxs-lookup"><span data-stu-id="e62be-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="e62be-138">Si noti che non è possibile forzare la separazione dei valori long di quattro byte o di dimensioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="e62be-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="e62be-139">In questi casi, l'opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="e62be-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e62be-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="e62be-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="e62be-141">Applica valori distinct in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e62be-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="e62be-142">Questa opzione consente di confrontare i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato.</span><span class="sxs-lookup"><span data-stu-id="e62be-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="e62be-143">Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="e62be-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e62be-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="e62be-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="e62be-145">Applica valori distinct in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e62be-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="e62be-146">Questa opzione Confronta la principale trasformazione normalizzata dei dati della colonna con altri valori di colonna in modo analogo e viene restituito un errore se viene trovato un duplicato.</span><span class="sxs-lookup"><span data-stu-id="e62be-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="e62be-147">Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV.</span><span class="sxs-lookup"><span data-stu-id="e62be-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e62be-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="e62be-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="e62be-149">Determina la restituzione del valore di colonna predefinito da parte della colonna nelle successive operazioni di recupero colonne.</span><span class="sxs-lookup"><span data-stu-id="e62be-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="e62be-150">Tutti i valori di colonna esistenti vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="e62be-150">All existing column values are removed.</span></span> <span data-ttu-id="e62be-151">Questa opzione è applicabile solo per le colonne con tag, sparse o multivalore.</span><span class="sxs-lookup"><span data-stu-id="e62be-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e62be-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="e62be-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="e62be-153">Mantiene il valore Long, le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o JET_coltypeLongBinary, archiviate con i dati record rimanenti, se possibile.</span><span class="sxs-lookup"><span data-stu-id="e62be-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="e62be-154">Normalmente, le colonne lunghe vengono archiviate separatamente quando la loro lunghezza supera i 1024 byte o altrimenti la lunghezza del record supera la limitazione della dimensione relativa alle dimensioni della pagina.</span><span class="sxs-lookup"><span data-stu-id="e62be-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="e62be-155">Tuttavia, se questa opzione è impostata, l'operazione set Column avrà esito negativo e si verificherà un errore JET_errColumnTooBig anziché archiviare questo valore di colonna separato dai dati rimanenti del record.</span><span class="sxs-lookup"><span data-stu-id="e62be-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e62be-156">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="e62be-156">**ibLongValue**</span></span>

<span data-ttu-id="e62be-157">Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e62be-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="e62be-158">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="e62be-158">**itagSequence**</span></span>

<span data-ttu-id="e62be-159">Descrive il numero di sequenza del valore in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e62be-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="e62be-160">Il valore 0 di **itagSequence** indica che il set di valori di colonna deve essere aggiunto come nuova istanza di una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e62be-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="e62be-161">**Err**</span><span class="sxs-lookup"><span data-stu-id="e62be-161">**err**</span></span>

<span data-ttu-id="e62be-162">Codici di errore e avvisi restituiti dall'operazione set Column.</span><span class="sxs-lookup"><span data-stu-id="e62be-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="e62be-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e62be-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e62be-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e62be-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e62be-165">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e62be-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e62be-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e62be-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e62be-167">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e62be-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e62be-168"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e62be-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e62be-169">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e62be-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e62be-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e62be-170">See Also</span></span>

[<span data-ttu-id="e62be-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="e62be-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="e62be-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e62be-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e62be-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e62be-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e62be-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e62be-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e62be-175">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="e62be-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
