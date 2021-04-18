---
description: 'Altre informazioni su: struttura JET_COLUMNLIST'
title: Struttura JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308511"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="048d3-103">Struttura JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="048d3-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="048d3-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="048d3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="048d3-105">Struttura JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="048d3-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="048d3-106">La struttura **JET_COLUMNLIST** contiene le informazioni necessarie per attraversare la tabella temporanea creata dalle funzioni [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="048d3-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="048d3-107">Ogni riga nella tabella temporanea descrive una colonna della tabella specificata nella chiamata API.</span><span class="sxs-lookup"><span data-stu-id="048d3-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="048d3-108">Questa struttura viene utilizzata solo con [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="048d3-109">Membri</span><span class="sxs-lookup"><span data-stu-id="048d3-109">Members</span></span>

<span data-ttu-id="048d3-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="048d3-110">**cbStruct**</span></span>

<span data-ttu-id="048d3-111">Dimensioni in byte della struttura.</span><span class="sxs-lookup"><span data-stu-id="048d3-111">The size of the structure in bytes.</span></span> <span data-ttu-id="048d3-112">La chiamata API aggiornerà questo campo, in modo che il chiamante assicuri che questo valore corrisponda a sizeof (JET_COLUMNLIST).</span><span class="sxs-lookup"><span data-stu-id="048d3-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="048d3-113">**TableID**</span><span class="sxs-lookup"><span data-stu-id="048d3-113">**tableid**</span></span>

<span data-ttu-id="048d3-114">Identificatore di tabella della tabella temporanea creata.</span><span class="sxs-lookup"><span data-stu-id="048d3-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="048d3-115">È responsabilità del chiamante chiudere la tabella.</span><span class="sxs-lookup"><span data-stu-id="048d3-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="048d3-116">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="048d3-116">**cRecord**</span></span>

<span data-ttu-id="048d3-117">Numero di record nella tabella temporanea creata dalla chiamata API.</span><span class="sxs-lookup"><span data-stu-id="048d3-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="048d3-118">**columnidPresentationOrder**</span><span class="sxs-lookup"><span data-stu-id="048d3-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="048d3-119">Identificatore di colonna dell'ordine di presentazione.</span><span class="sxs-lookup"><span data-stu-id="048d3-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="048d3-120">L'ordine di presentazione viene utilizzato per ordinare le righe della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="048d3-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="048d3-121">L'ordine di presentazione è un [JET_coltypLong](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="048d3-122">Se il livello di informazioni specificato non è un livello di compattazione, viene anche contrassegnato come JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="048d3-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="048d3-123">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="048d3-123">**columnidcolumnname**</span></span>

<span data-ttu-id="048d3-124">Identificatore di colonna del nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="048d3-125">Se il livello di informazioni specificato non è Compact, viene anche contrassegnato come JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="048d3-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="048d3-126">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="048d3-126">**columnidcolumnid**</span></span>

<span data-ttu-id="048d3-127">Identificatore di colonna dell'identificatore di colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="048d3-128">L'identificatore di colonna è un [JET_coltypLong](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-129">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="048d3-129">**columnidcoltyp**</span></span>

<span data-ttu-id="048d3-130">Identificatore di colonna del tipo di colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-130">The column identifier of the column type.</span></span>

<span data-ttu-id="048d3-131">Il tipo di colonna è un [JET_coltypLong](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-132">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="048d3-132">**columnidCountry**</span></span>

<span data-ttu-id="048d3-133">Identificatore di colonna del codice paese.</span><span class="sxs-lookup"><span data-stu-id="048d3-133">The column identifier of the country code.</span></span>

<span data-ttu-id="048d3-134">Il codice paese è un [JET_coltypShort](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-135">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="048d3-135">**columnidLangid**</span></span>

<span data-ttu-id="048d3-136">Identificatore di colonna dell'identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="048d3-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="048d3-137">L'identificatore di lingua è un [JET_coltypShort](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-138">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="048d3-138">**columnidCp**</span></span>

<span data-ttu-id="048d3-139">Identificatore di colonna della tabella codici.</span><span class="sxs-lookup"><span data-stu-id="048d3-139">The column identifier of the code page.</span></span>

<span data-ttu-id="048d3-140">La tabella codici è un [JET_coltypShort](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-141">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="048d3-141">**columnidCollate**</span></span>

<span data-ttu-id="048d3-142">Identificatore di colonna della sequenza delle regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="048d3-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="048d3-143">La sequenza delle regole di confronto è un [JET_coltypShort](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-144">**columnidcbMax**</span><span class="sxs-lookup"><span data-stu-id="048d3-144">**columnidcbMax**</span></span>

<span data-ttu-id="048d3-145">Identificatore di colonna del campo **cbMax** .</span><span class="sxs-lookup"><span data-stu-id="048d3-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="048d3-146">**CbMax** è un [JET_coltypLong](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-147">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="048d3-147">**columnidgrbit**</span></span>

<span data-ttu-id="048d3-148">Identificatore di colonna del *grbits* della colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="048d3-149">Il campo *grbit* è un [JET_coltypLong](./jet-coltyp.md)fisso.</span><span class="sxs-lookup"><span data-stu-id="048d3-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="048d3-150">Per ulteriori informazioni su questi bit, vedere [JET_COLUMNDEF](./jet-columndef-structure.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="048d3-151">Di seguito sono riportati i valori possibili per **columnidgrbit**:</span><span class="sxs-lookup"><span data-stu-id="048d3-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="048d3-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="048d3-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="048d3-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="048d3-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="048d3-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="048d3-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="048d3-155">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="048d3-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="048d3-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="048d3-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="048d3-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="048d3-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="048d3-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="048d3-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="048d3-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="048d3-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="048d3-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="048d3-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="048d3-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="048d3-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="048d3-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="048d3-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="048d3-163">**columnidDefault**</span><span class="sxs-lookup"><span data-stu-id="048d3-163">**columnidDefault**</span></span>

<span data-ttu-id="048d3-164">Identificatore di colonna del valore predefinito della colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="048d3-165">Il valore predefinito è un [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-166">**columnidBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="048d3-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="048d3-167">Identificatore di colonna del nome della tabella da cui è stata derivata la tabella.</span><span class="sxs-lookup"><span data-stu-id="048d3-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="048d3-168">Il nome della tabella è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-169">**columnidBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="048d3-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="048d3-170">Identificatore di colonna del nome della colonna da cui è stata derivata la colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="048d3-171">Il nome della colonna è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="048d3-172">**columnidDefinitionName**</span><span class="sxs-lookup"><span data-stu-id="048d3-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="048d3-173">Identificatore di colonna del nome della definizione di colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="048d3-174">Il nome della definizione di colonna è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="048d3-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="048d3-175">Remarks</span></span>

<span data-ttu-id="048d3-176">Per impostazione predefinita, l'ordine delle righe nella tabella temporanea viene ordinato in base al nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="048d3-177">Può anche essere ordinato in base all'identificatore di colonna.</span><span class="sxs-lookup"><span data-stu-id="048d3-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="048d3-178">Per ulteriori informazioni sull'ordinamento in base all'identificatore di colonna, vedere [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="048d3-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="048d3-179">La chiamata a [JetGetColumnInfo](./jetgetcolumninfo-function.md) o [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) può specificare una forma compatta di risultati.</span><span class="sxs-lookup"><span data-stu-id="048d3-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="048d3-180">Se sono state ereditate colonne da una tabella modello, i risultati di Compact non li archivia.</span><span class="sxs-lookup"><span data-stu-id="048d3-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="048d3-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="048d3-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="048d3-182"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="048d3-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="048d3-183">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="048d3-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048d3-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="048d3-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="048d3-185">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="048d3-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048d3-186"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="048d3-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="048d3-187">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="048d3-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="048d3-188">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="048d3-188">See Also</span></span>

[<span data-ttu-id="048d3-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="048d3-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="048d3-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="048d3-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="048d3-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="048d3-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="048d3-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="048d3-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="048d3-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="048d3-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="048d3-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="048d3-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="048d3-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="048d3-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="048d3-196">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="048d3-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="048d3-197">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="048d3-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
