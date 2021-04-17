---
description: 'Altre informazioni su: membri JET_ENUMCOLUMNVALUE'
title: Membri JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560711"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="2a9e4-103">Membri JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="2a9e4-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="2a9e4-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="2a9e4-104">Include protected members</span></span>  
<span data-ttu-id="2a9e4-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="2a9e4-105">Include inherited members</span></span>  

<span data-ttu-id="2a9e4-106">Enumera i valori di colonna di un record utilizzando la funzione JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="2a9e4-107">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) restituisce una matrice di strutture JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="2a9e4-108">La matrice viene restituita nella memoria allocata utilizzando il callback fornito a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="2a9e4-109">Il tipo di [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="2a9e4-110">Costruttori</span><span class="sxs-lookup"><span data-stu-id="2a9e4-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2a9e4-111">Nome</span><span class="sxs-lookup"><span data-stu-id="2a9e4-111">Name</span></span></th>
<th><span data-ttu-id="2a9e4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a9e4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="2a9e4-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a9e4-115">Inizio</span><span class="sxs-lookup"><span data-stu-id="2a9e4-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="2a9e4-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a9e4-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2a9e4-117">Nome</span><span class="sxs-lookup"><span data-stu-id="2a9e4-117">Name</span></span></th>
<th><span data-ttu-id="2a9e4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a9e4-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="2a9e4-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="2a9e4-121">Ottiene la dimensione del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="2a9e4-123"><a href="dn335144(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="2a9e4-124">Ottiene il codice di stato della colonna risultante dall'enumerazione del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="2a9e4-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="2a9e4-127">Ottiene il valore della colonna (in base a un indice in base 1) enumerato.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="2a9e4-129"><a href="dn335149(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="2a9e4-130">Ottiene il valore enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a9e4-131">Inizio</span><span class="sxs-lookup"><span data-stu-id="2a9e4-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="2a9e4-132">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a9e4-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2a9e4-133">Nome</span><span class="sxs-lookup"><span data-stu-id="2a9e4-133">Name</span></span></th>
<th><span data-ttu-id="2a9e4-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a9e4-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="2a9e4-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="2a9e4-137">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="2a9e4-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="2a9e4-140">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="2a9e4-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="2a9e4-143">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="2a9e4-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="2a9e4-146">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="2a9e4-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="2a9e4-149">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="2a9e4-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="2a9e4-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="2a9e4-152">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="2a9e4-153">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a9e4-154">Inizio</span><span class="sxs-lookup"><span data-stu-id="2a9e4-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2a9e4-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a9e4-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a9e4-156">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2a9e4-156">Reference</span></span>

[<span data-ttu-id="2a9e4-157">Classe JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="2a9e4-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="2a9e4-158">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2a9e4-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
