---
description: 'Altre informazioni su: membri JET_INDEXLIST'
title: Membri JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058088"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="b59a3-103">Membri JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="b59a3-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="b59a3-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="b59a3-104">Include protected members</span></span>  
<span data-ttu-id="b59a3-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="b59a3-105">Include inherited members</span></span>  

<span data-ttu-id="b59a3-106">Informazioni su una tabella temporanea contenente informazioni su tutti gli indici per una tabella specifica.</span><span class="sxs-lookup"><span data-stu-id="b59a3-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="b59a3-107">Il tipo di [JET_INDEXLIST](./jet-indexlist-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b59a3-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="b59a3-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="b59a3-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b59a3-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b59a3-109">Name</span></span></th>
<th><span data-ttu-id="b59a3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b59a3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="b59a3-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b59a3-113">Inizio</span><span class="sxs-lookup"><span data-stu-id="b59a3-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="b59a3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b59a3-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b59a3-115">Nome</span><span class="sxs-lookup"><span data-stu-id="b59a3-115">Name</span></span></th>
<th><span data-ttu-id="b59a3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b59a3-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="b59a3-119">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di colonne nella chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="b59a3-120">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="b59a3-123">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di voci nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="b59a3-124">Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="b59a3-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="b59a3-125">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="b59a3-128">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di chiavi univoche nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="b59a3-129">Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="b59a3-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="b59a3-130">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="b59a3-133">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il tipo di colonna della colonna da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="b59a3-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="b59a3-134">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="b59a3-137">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il ColumnID della colonna da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="b59a3-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="b59a3-138">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="b59a3-141">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbit che si applicano alla colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="b59a3-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="b59a3-142">Vedere <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="b59a3-143">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="b59a3-146">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviata la tabella codici della colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="b59a3-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="b59a3-147">La colonna è di tipo <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="b59a3-150">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di pagine nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="b59a3-151">Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="b59a3-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="b59a3-152">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="b59a3-155">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbit che si applicano alla colonna indicizzata.</span><span class="sxs-lookup"><span data-stu-id="b59a3-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="b59a3-156">Vedere <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="b59a3-157">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="b59a3-160">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbits usato nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="b59a3-161">Vedere <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="b59a3-162">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="b59a3-165">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato l'indice di della colonna nella chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="b59a3-166">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="b59a3-169">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="b59a3-170">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Text</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="b59a3-173">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato l'ID lingua (LCID) dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="b59a3-174">La colonna è di tipo <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="b59a3-177">Ottiene l'ColumnID della colonna nella tabella temporanea in cui sono archiviati i flag di normalizzazione Unicode per l'indice.</span><span class="sxs-lookup"><span data-stu-id="b59a3-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="b59a3-178">La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="b59a3-181">Ottiene il numero di record nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b59a3-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b59a3-183"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="b59a3-184">Ottiene TableID della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b59a3-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="b59a3-185">Questa operazione deve essere chiusa quando la tabella non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="b59a3-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b59a3-186">Inizio</span><span class="sxs-lookup"><span data-stu-id="b59a3-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="b59a3-187">Metodi</span><span class="sxs-lookup"><span data-stu-id="b59a3-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b59a3-188">Nome</span><span class="sxs-lookup"><span data-stu-id="b59a3-188">Name</span></span></th>
<th><span data-ttu-id="b59a3-189">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b59a3-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="b59a3-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="b59a3-192">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="b59a3-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="b59a3-195">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="b59a3-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="b59a3-198">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="b59a3-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="b59a3-201">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="b59a3-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="b59a3-204">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="b59a3-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="b59a3-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="b59a3-207">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="b59a3-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="b59a3-208">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="b59a3-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b59a3-209">Inizio</span><span class="sxs-lookup"><span data-stu-id="b59a3-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b59a3-210">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b59a3-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b59a3-211">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b59a3-211">Reference</span></span>

[<span data-ttu-id="b59a3-212">Classe JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="b59a3-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="b59a3-213">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b59a3-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
