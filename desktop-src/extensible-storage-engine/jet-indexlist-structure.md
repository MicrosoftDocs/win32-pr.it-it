---
description: 'Altre informazioni su: struttura JET_INDEXLIST'
title: Struttura JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346996"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="39059-103">Struttura JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="39059-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="39059-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="39059-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="39059-105">Struttura JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="39059-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="39059-106">La struttura **JET_INDEXLIST** contiene le informazioni necessarie per attraversare una tabella temporanea creata dalle funzioni [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="39059-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="39059-107">Ogni riga della tabella temporanea descrive una colonna di un indice.</span><span class="sxs-lookup"><span data-stu-id="39059-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="39059-108">Membri</span><span class="sxs-lookup"><span data-stu-id="39059-108">Members</span></span>

<span data-ttu-id="39059-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="39059-109">**cbStruct**</span></span>

<span data-ttu-id="39059-110">Dimensioni in byte della struttura.</span><span class="sxs-lookup"><span data-stu-id="39059-110">The size of the structure in bytes.</span></span> <span data-ttu-id="39059-111">La chiamata API aggiornerà questo campo, in modo che il chiamante assicuri che questo valore corrisponda a sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="39059-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="39059-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="39059-112">**tableid**</span></span>

<span data-ttu-id="39059-113">Identificatore di tabella della tabella temporanea creata.</span><span class="sxs-lookup"><span data-stu-id="39059-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="39059-114">È responsabilità del chiamante chiudere la tabella.</span><span class="sxs-lookup"><span data-stu-id="39059-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="39059-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="39059-115">**cRecord**</span></span>

<span data-ttu-id="39059-116">Numero di record nella tabella temporanea creata.</span><span class="sxs-lookup"><span data-stu-id="39059-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="39059-117">**columnidindexname**</span><span class="sxs-lookup"><span data-stu-id="39059-117">**columnidindexname**</span></span>

<span data-ttu-id="39059-118">Identificatore di colonna del nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="39059-119">Questa colonna è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-120">**columnidgrbitIndex**</span><span class="sxs-lookup"><span data-stu-id="39059-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="39059-121">Identificatore di colonna di *grbits* utilizzato nell'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="39059-122">Per un elenco di bit validi, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="39059-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="39059-123">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-124">**columnidcKey**</span><span class="sxs-lookup"><span data-stu-id="39059-124">**columnidcKey**</span></span>

<span data-ttu-id="39059-125">Identificatore di colonna del numero di chiavi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="39059-126">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-127">**columnidcEntry**</span><span class="sxs-lookup"><span data-stu-id="39059-127">**columnidcEntry**</span></span>

<span data-ttu-id="39059-128">Identificatore di colonna del numero di voci nell'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="39059-129">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-130">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="39059-130">**columnidcPage**</span></span>

<span data-ttu-id="39059-131">Identificatore di colonna del numero di pagine utilizzate dall'indice. Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-132">**columnidcColumn**</span><span class="sxs-lookup"><span data-stu-id="39059-132">**columnidcColumn**</span></span>

<span data-ttu-id="39059-133">Identificatore di colonna del numero totale di colonne di cui l'indice si estende.</span><span class="sxs-lookup"><span data-stu-id="39059-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="39059-134">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-135">**columnidiColumn**</span><span class="sxs-lookup"><span data-stu-id="39059-135">**columnidiColumn**</span></span>

<span data-ttu-id="39059-136">Identificatore di colonna del numero di colonne nell'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="39059-137">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="39059-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="39059-138">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39059-139">Valore</span><span class="sxs-lookup"><span data-stu-id="39059-139">Value</span></span></p></th>
<th><p><span data-ttu-id="39059-140">Significato</span><span class="sxs-lookup"><span data-stu-id="39059-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39059-141">cIndexInfoCols</span><span class="sxs-lookup"><span data-stu-id="39059-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="39059-142">15</span><span class="sxs-lookup"><span data-stu-id="39059-142">15</span></span></p></td>
<td><p><span data-ttu-id="39059-143">Specifica che sono consentite 15 colonne.</span><span class="sxs-lookup"><span data-stu-id="39059-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39059-144">cColumnInfoCols</span><span class="sxs-lookup"><span data-stu-id="39059-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="39059-145">14</span><span class="sxs-lookup"><span data-stu-id="39059-145">14</span></span></p></td>
<td><p><span data-ttu-id="39059-146">Specifica che sono consentite 14 colonne.</span><span class="sxs-lookup"><span data-stu-id="39059-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39059-147">cObjectInfoCols</span><span class="sxs-lookup"><span data-stu-id="39059-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="39059-148">9</span><span class="sxs-lookup"><span data-stu-id="39059-148">9</span></span></p></td>
<td><p><span data-ttu-id="39059-149">Specifica che sono consentite 9 colonne.</span><span class="sxs-lookup"><span data-stu-id="39059-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="39059-150">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="39059-150">**columnidcolumnid**</span></span>

<span data-ttu-id="39059-151">Identificatore di colonna della colonna indicizzata. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="39059-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="39059-152">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-153">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="39059-153">**columnidcoltyp**</span></span>

<span data-ttu-id="39059-154">Identificatore di colonna di coltyp della colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="39059-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="39059-155">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="39059-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="39059-156">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-157">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="39059-157">**columnidCountry**</span></span>

<span data-ttu-id="39059-158">Identificatore di colonna del codice paese della colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="39059-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="39059-159">Il codice paese è deprecato.</span><span class="sxs-lookup"><span data-stu-id="39059-159">The country code is deprecated.</span></span>

<span data-ttu-id="39059-160">Questa colonna è un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-161">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="39059-161">**columnidLangid**</span></span>

<span data-ttu-id="39059-162">Identificatore di colonna dell'identificatore di lingua (LCID) in cui è stato creato l'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="39059-163">Per ulteriori informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="39059-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="39059-164">Questa colonna è un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-165">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="39059-165">**columnidCp**</span></span>

<span data-ttu-id="39059-166">Identificatore di colonna della tabella codici in cui è stato creato l'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="39059-167">Per ulteriori informazioni, vedere [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="39059-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="39059-168">Questa colonna è un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-169">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="39059-169">**columnidCollate**</span></span>

<span data-ttu-id="39059-170">Identificatore di colonna della sequenza delle regole di confronto in cui è stato creato l'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="39059-171">La sequenza delle regole di confronto è deprecata.</span><span class="sxs-lookup"><span data-stu-id="39059-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="39059-172">Questa colonna è un [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-173">**columnidgrbitColumn**</span><span class="sxs-lookup"><span data-stu-id="39059-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="39059-174">Identificatore di colonna di *grbits* che si applicano all'ordine della colonna nell'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="39059-175">I dati di questa colonna possono essere ordinati come JET_bitKeyAscending o JET_bitKeyDescending.</span><span class="sxs-lookup"><span data-stu-id="39059-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="39059-176">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="39059-177">Ad esempio, un indice definito come "-Column1 \\ 0 + Column2 \\ 0" avrà JET_bitKeyDescending per "Column1" e JET_bitKeyAscending per "Column2".</span><span class="sxs-lookup"><span data-stu-id="39059-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="39059-178">Per questo membro sono valide le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="39059-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39059-179">Valore</span><span class="sxs-lookup"><span data-stu-id="39059-179">Value</span></span></p></th>
<th><p><span data-ttu-id="39059-180">Significato</span><span class="sxs-lookup"><span data-stu-id="39059-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39059-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="39059-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="39059-182">Segmento di indice in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="39059-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39059-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="39059-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="39059-184">Segmento di indice in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="39059-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="39059-185">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="39059-185">**columnidcolumnname**</span></span>

<span data-ttu-id="39059-186">Identificatore di colonna del nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="39059-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="39059-187">Questa colonna è un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="39059-188">**columnidLCMapFlags**</span><span class="sxs-lookup"><span data-stu-id="39059-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="39059-189">Identificatore di colonna dei flag utilizzati per creare l'indice.</span><span class="sxs-lookup"><span data-stu-id="39059-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="39059-190">Per ulteriori informazioni, vedere la sezione **dwMapFlags** di [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span><span class="sxs-lookup"><span data-stu-id="39059-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="39059-191">Questa colonna è un [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="39059-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="39059-192">Commenti</span><span class="sxs-lookup"><span data-stu-id="39059-192">Remarks</span></span>

<span data-ttu-id="39059-193">Ogni riga della tabella temporanea corrisponde a una colonna in un particolare indice.</span><span class="sxs-lookup"><span data-stu-id="39059-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="39059-194">Ad esempio, l'indice "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0" è più di cinque colonne e occuperà cinque righe nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="39059-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="39059-195">Ognuna di queste cinque righe avrà un valore pari a 5 nella colonna identificata dalla colonna ColumnID.</span><span class="sxs-lookup"><span data-stu-id="39059-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="39059-196">Tuttavia, ogni riga avrà un valore diverso per la colonna ColumnID, che va da 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="39059-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="39059-197">Il numero di chiavi in un particolare indice corrisponde al numero di valori univoci per cui un chiamante può cercare e ottenere una corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="39059-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="39059-198">Il numero di voci indica il numero di righe corrispondenti a un indice.</span><span class="sxs-lookup"><span data-stu-id="39059-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="39059-199">Se un indice ha un vincolo di univocità, il numero di chiavi è uguale al numero di voci.</span><span class="sxs-lookup"><span data-stu-id="39059-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="39059-200">Se, ad esempio, una tabella contiene le informazioni seguenti e viene creato un indice sulla colonna denominata "Key", sono disponibili tre chiavi (100, 200 e 500), ma vi sono quattro voci ("This", "is", "an" e "example").</span><span class="sxs-lookup"><span data-stu-id="39059-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39059-201">Chiave</span><span class="sxs-lookup"><span data-stu-id="39059-201">Key</span></span></p></th>
<th><p><span data-ttu-id="39059-202">Voce</span><span class="sxs-lookup"><span data-stu-id="39059-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39059-203">100</span><span class="sxs-lookup"><span data-stu-id="39059-203">100</span></span></p></td>
<td><p><span data-ttu-id="39059-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="39059-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39059-205">100</span><span class="sxs-lookup"><span data-stu-id="39059-205">100</span></span></p></td>
<td><p><span data-ttu-id="39059-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="39059-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39059-207">200</span><span class="sxs-lookup"><span data-stu-id="39059-207">200</span></span></p></td>
<td><p><span data-ttu-id="39059-208">&quot;un&quot;</span><span class="sxs-lookup"><span data-stu-id="39059-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39059-209">500</span><span class="sxs-lookup"><span data-stu-id="39059-209">500</span></span></p></td>
<td><p><span data-ttu-id="39059-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="39059-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="39059-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39059-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39059-212"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="39059-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="39059-213">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="39059-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39059-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="39059-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39059-215">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="39059-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39059-216"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="39059-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="39059-217">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="39059-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="39059-218">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="39059-218">See Also</span></span>

[<span data-ttu-id="39059-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="39059-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="39059-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="39059-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="39059-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="39059-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="39059-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="39059-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="39059-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="39059-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="39059-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="39059-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="39059-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="39059-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="39059-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="39059-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="39059-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="39059-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="39059-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="39059-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="39059-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="39059-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
