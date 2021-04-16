---
description: 'Altre informazioni su: membri JET_ENUMCOLUMN'
title: Membri JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553893"
---
# <a name="jet_enumcolumn-members"></a><span data-ttu-id="7eb8d-103">Membri JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="7eb8d-103">JET_ENUMCOLUMN members</span></span>

<span data-ttu-id="7eb8d-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="7eb8d-104">Include protected members</span></span>  
<span data-ttu-id="7eb8d-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="7eb8d-105">Include inherited members</span></span>  

<span data-ttu-id="7eb8d-106">Enumera i valori di colonna di un record utilizzando la funzione JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="7eb8d-107">JetEnumerateColumns restituisce una matrice di strutture di JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-107">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="7eb8d-108">La matrice viene restituita nella memoria allocata utilizzando il callback fornito a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="7eb8d-109">Il tipo di [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-109">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="7eb8d-110">Costruttori</span><span class="sxs-lookup"><span data-stu-id="7eb8d-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7eb8d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7eb8d-111">Name</span></span></th>
<th><span data-ttu-id="7eb8d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb8d-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="7eb8d-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eb8d-115">Inizio</span><span class="sxs-lookup"><span data-stu-id="7eb8d-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="7eb8d-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7eb8d-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7eb8d-117">Nome</span><span class="sxs-lookup"><span data-stu-id="7eb8d-117">Name</span></span></th>
<th><span data-ttu-id="7eb8d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb8d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="7eb8d-120"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-120"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="7eb8d-121">Ottiene la dimensione del valore enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-121">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="7eb8d-122">Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-122">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="7eb8d-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="7eb8d-125">Ottiene il numero di valori di colonna enumerati per la colonna.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-125">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="7eb8d-126">Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-126">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="7eb8d-128"><a href="dn335135(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-128"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="7eb8d-129">Ottiene l'ID ColumnID enumerato.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-129">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="7eb8d-131"><a href="dn335086(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-131"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="7eb8d-132">Ottiene il codice di stato della colonna risultante dall'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-132">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="7eb8d-134"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-134"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="7eb8d-135">Ottiene il valore enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-135">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="7eb8d-136">Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-136">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="7eb8d-137">Questo fa riferimento alla memoria allocata con il callback dell'allocatore <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passato a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-137">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="7eb8d-138">Ricordarsi di rilasciare la memoria al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-138">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="7eb8d-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="7eb8d-141">Ottiene i valori della colonna enumerata per la colonna.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-141">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="7eb8d-142">Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-142">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eb8d-143">Inizio</span><span class="sxs-lookup"><span data-stu-id="7eb8d-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="7eb8d-144">Metodi</span><span class="sxs-lookup"><span data-stu-id="7eb8d-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7eb8d-145">Nome</span><span class="sxs-lookup"><span data-stu-id="7eb8d-145">Name</span></span></th>
<th><span data-ttu-id="7eb8d-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb8d-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="7eb8d-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="7eb8d-149">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="7eb8d-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="7eb8d-152">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="7eb8d-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="7eb8d-155">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="7eb8d-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="7eb8d-158">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="7eb8d-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="7eb8d-161">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="7eb8d-163"><a href="dn335132(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-163"><a href="dn335132(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="7eb8d-164">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-164">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>.</span></span> <span data-ttu-id="7eb8d-165">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-165">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eb8d-166">Inizio</span><span class="sxs-lookup"><span data-stu-id="7eb8d-166">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="7eb8d-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7eb8d-167">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7eb8d-168">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7eb8d-168">Reference</span></span>

[<span data-ttu-id="7eb8d-169">Classe JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="7eb8d-169">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="7eb8d-170">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7eb8d-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
