---
description: 'Altre informazioni su: Proprietà JET_INDEXLIST'
title: Proprietà JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554352"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="a78d9-103">Proprietà JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="a78d9-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="a78d9-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="a78d9-104">Include protected members</span></span>  
<span data-ttu-id="a78d9-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="a78d9-105">Include inherited members</span></span>  

<span data-ttu-id="a78d9-106">Il tipo di [JET_INDEXLIST](./jet-indexlist-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a78d9-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a78d9-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a78d9-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a78d9-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a78d9-108">Name</span></span></th>
<th><span data-ttu-id="a78d9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a78d9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="a78d9-112">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di colonne nella chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="a78d9-113">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="a78d9-116">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di voci nell'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="a78d9-117">Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="a78d9-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a78d9-118">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="a78d9-121">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di chiavi univoche nell'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="a78d9-122">Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="a78d9-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a78d9-123">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="a78d9-126">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il tipo di colonna della colonna da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="a78d9-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="a78d9-127">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="a78d9-130">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il ColumnID della colonna da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="a78d9-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="a78d9-131">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="a78d9-134">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbit che si applicano alla colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="a78d9-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="a78d9-135">Vedere <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="a78d9-136">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="a78d9-139">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviata la tabella codici della colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="a78d9-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="a78d9-140">La colonna è di tipo <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="a78d9-143">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di pagine nell'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="a78d9-144">Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="a78d9-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a78d9-145">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="a78d9-148">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbit che si applicano alla colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="a78d9-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="a78d9-149">Vedere <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="a78d9-150">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="a78d9-153">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbits usato nell'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="a78d9-154">Vedere <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="a78d9-155">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="a78d9-158">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato l'indice di della colonna nella chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="a78d9-159">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="a78d9-162">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="a78d9-163">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="a78d9-166">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato l'ID lingua (LCID) dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="a78d9-167">La colonna è di tipo <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="a78d9-170">Ottiene l'ColumnID della colonna nella tabella temporanea in cui sono archiviati i flag di normalizzazione Unicode per l'indice.</span><span class="sxs-lookup"><span data-stu-id="a78d9-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="a78d9-171">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a78d9-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="a78d9-174">Ottiene il numero di record nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="a78d9-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="a78d9-176"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="a78d9-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="a78d9-177">Ottiene TableID della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="a78d9-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="a78d9-178">Questa operazione deve essere chiusa quando la tabella non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="a78d9-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a78d9-179">Inizio</span><span class="sxs-lookup"><span data-stu-id="a78d9-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a78d9-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a78d9-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a78d9-181">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a78d9-181">Reference</span></span>

[<span data-ttu-id="a78d9-182">Classe JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="a78d9-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="a78d9-183">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a78d9-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
