---
description: 'Altre informazioni su: membri JET_RECORDLIST'
title: Membri JET_RECORDLIST
TOCTitle: JET_RECORDLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RECORDLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist_members(v=EXCHG.10)
ms:contentKeyID: 55103811
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d2e43304dfd554be09d410c3885ca63fd199124b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558643"
---
# <a name="jet_recordlist-members"></a><span data-ttu-id="65409-103">Membri JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="65409-103">JET_RECORDLIST members</span></span>

<span data-ttu-id="65409-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="65409-104">Include protected members</span></span>  
<span data-ttu-id="65409-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="65409-105">Include inherited members</span></span>  

<span data-ttu-id="65409-106">Informazioni su una tabella temporanea contenente informazioni su tutti gli indici per una tabella specifica.</span><span class="sxs-lookup"><span data-stu-id="65409-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="65409-107">Il tipo di [JET_RECORDLIST](./jet-recordlist-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="65409-107">The [JET_RECORDLIST](./jet-recordlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="65409-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="65409-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="65409-109">Nome</span><span class="sxs-lookup"><span data-stu-id="65409-109">Name</span></span></th>
<th><span data-ttu-id="65409-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65409-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="65409-112"><a href="dn335241(v=exchg.10).md">JET_RECORDLIST</a></span><span class="sxs-lookup"><span data-stu-id="65409-112"><a href="dn335241(v=exchg.10).md">JET_RECORDLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65409-113">Inizio</span><span class="sxs-lookup"><span data-stu-id="65409-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="65409-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="65409-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="65409-115">Nome</span><span class="sxs-lookup"><span data-stu-id="65409-115">Name</span></span></th>
<th><span data-ttu-id="65409-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65409-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="65409-118"><a href="dn335244(v=exchg.10).md">columnidBookmark</a></span><span class="sxs-lookup"><span data-stu-id="65409-118"><a href="dn335244(v=exchg.10).md">columnidBookmark</a></span></span></td>
<td><span data-ttu-id="65409-119">Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il segnalibro del record.</span><span class="sxs-lookup"><span data-stu-id="65409-119">Gets the columnid of the column in the temporary table which stores the bookmark of the record.</span></span> <span data-ttu-id="65409-120">La colonna è di tipo JET_coltyp. Testo.</span><span class="sxs-lookup"><span data-stu-id="65409-120">The column is of type JET_coltyp.Text.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="65409-122"><a href="dn335252(v=exchg.10).md">cRecords</a></span><span class="sxs-lookup"><span data-stu-id="65409-122"><a href="dn335252(v=exchg.10).md">cRecords</a></span></span></td>
<td><span data-ttu-id="65409-123">Ottiene il numero di record nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="65409-123">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="65409-125"><a href="dn335255(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="65409-125"><a href="dn335255(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="65409-126">Ottiene TableID della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="65409-126">Gets tableid of the temporary table.</span></span> <span data-ttu-id="65409-127">Questa operazione deve essere chiusa quando la tabella non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="65409-127">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65409-128">Inizio</span><span class="sxs-lookup"><span data-stu-id="65409-128">Top</span></span>

## <a name="methods"></a><span data-ttu-id="65409-129">Metodi</span><span class="sxs-lookup"><span data-stu-id="65409-129">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="65409-130">Nome</span><span class="sxs-lookup"><span data-stu-id="65409-130">Name</span></span></th>
<th><span data-ttu-id="65409-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65409-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="65409-133"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="65409-133"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="65409-134">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="65409-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="65409-136"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="65409-136"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="65409-137">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="65409-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="65409-139"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="65409-139"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="65409-140">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="65409-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="65409-142"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="65409-142"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="65409-143">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="65409-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="65409-145"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="65409-145"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="65409-146">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="65409-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="65409-148"><a href="dn335242(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="65409-148"><a href="dn335242(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="65409-149">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="65409-149">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="65409-150">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="65409-150">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65409-151">Inizio</span><span class="sxs-lookup"><span data-stu-id="65409-151">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="65409-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65409-152">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="65409-153">Riferimento</span><span class="sxs-lookup"><span data-stu-id="65409-153">Reference</span></span>

[<span data-ttu-id="65409-154">Classe JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="65409-154">JET_RECORDLIST class</span></span>](./jet-recordlist-class.md)

[<span data-ttu-id="65409-155">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="65409-155">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
