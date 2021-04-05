---
description: 'Altre informazioni su: membri JET_ENUMCOLUMNID'
title: Membri JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049356"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="489eb-103">Membri JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="489eb-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="489eb-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="489eb-104">Include protected members</span></span>  
<span data-ttu-id="489eb-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="489eb-105">Include inherited members</span></span>  

<span data-ttu-id="489eb-106">Enumera un set specifico di colonne e, facoltativamente, un set specifico di più valori per tali colonne quando viene utilizzata la funzione JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="489eb-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="489eb-107">JetEnumerateColumns facoltativamente accetta una matrice di strutture di JET_ENUMCOLUMNID.</span><span class="sxs-lookup"><span data-stu-id="489eb-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="489eb-108">Il tipo di [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="489eb-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="489eb-109">Costruttori</span><span class="sxs-lookup"><span data-stu-id="489eb-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="489eb-110">Nome</span><span class="sxs-lookup"><span data-stu-id="489eb-110">Name</span></span></th>
<th><span data-ttu-id="489eb-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="489eb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="489eb-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="489eb-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="489eb-114">Inizio</span><span class="sxs-lookup"><span data-stu-id="489eb-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="489eb-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="489eb-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="489eb-116">Nome</span><span class="sxs-lookup"><span data-stu-id="489eb-116">Name</span></span></th>
<th><span data-ttu-id="489eb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="489eb-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="489eb-119"><a href="dn335141(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="489eb-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="489eb-120">Ottiene o imposta l'ID ColumnID da enumerare.</span><span class="sxs-lookup"><span data-stu-id="489eb-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="489eb-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="489eb-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="489eb-123">Ottiene o imposta il conteggio dei valori di colonna (in base a un indice in base 1) da enumerare per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="489eb-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="489eb-124">Se ctagSequence è 0 (zero), rgtagSequence viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="489eb-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="489eb-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="489eb-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="489eb-127">Ottiene o imposta la matrice di indici in base uno in una matrice di valori di colonna per una colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="489eb-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="489eb-128">Un singolo elemento è un itagSequence definito in JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="489eb-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="489eb-129">Un itagSequence pari a 0 (zero) indica &quot; Skip &quot; .</span><span class="sxs-lookup"><span data-stu-id="489eb-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="489eb-130">Un itagSequence di 1 indica che restituisce il primo valore della colonna, 2 indica il secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="489eb-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="489eb-131">Inizio</span><span class="sxs-lookup"><span data-stu-id="489eb-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="489eb-132">Metodi</span><span class="sxs-lookup"><span data-stu-id="489eb-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="489eb-133">Nome</span><span class="sxs-lookup"><span data-stu-id="489eb-133">Name</span></span></th>
<th><span data-ttu-id="489eb-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="489eb-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="489eb-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="489eb-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="489eb-137">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="489eb-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="489eb-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="489eb-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="489eb-140">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="489eb-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="489eb-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="489eb-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="489eb-143">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="489eb-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="489eb-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="489eb-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="489eb-146">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="489eb-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="489eb-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="489eb-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="489eb-149">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="489eb-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="489eb-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="489eb-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="489eb-152">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="489eb-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="489eb-153">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="489eb-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="489eb-154">Inizio</span><span class="sxs-lookup"><span data-stu-id="489eb-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="489eb-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="489eb-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="489eb-156">Riferimento</span><span class="sxs-lookup"><span data-stu-id="489eb-156">Reference</span></span>

[<span data-ttu-id="489eb-157">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="489eb-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="489eb-158">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="489eb-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
