---
description: 'Altre informazioni su: membri JET_SETINFO'
title: Membri JET_SETINFO
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750490"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="29050-103">Membri JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="29050-103">JET_SETINFO members</span></span>

<span data-ttu-id="29050-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="29050-104">Include protected members</span></span>  
<span data-ttu-id="29050-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="29050-105">Include inherited members</span></span>  

<span data-ttu-id="29050-106">Impostazioni per JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="29050-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="29050-107">Il tipo di [JET_SETINFO](./jet-setinfo-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="29050-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="29050-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="29050-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="29050-109">Nome</span><span class="sxs-lookup"><span data-stu-id="29050-109">Name</span></span></th>
<th><span data-ttu-id="29050-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29050-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="29050-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="29050-113">Inizio</span><span class="sxs-lookup"><span data-stu-id="29050-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="29050-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29050-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="29050-115">Nome</span><span class="sxs-lookup"><span data-stu-id="29050-115">Name</span></span></th>
<th><span data-ttu-id="29050-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29050-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="29050-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="29050-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="29050-119">Ottiene o imposta l'offset al primo byte da impostare in una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="29050-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="29050-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="29050-122">Ottiene o imposta il numero di sequenza del valore in una colonna multivalore da impostare.</span><span class="sxs-lookup"><span data-stu-id="29050-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="29050-123">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="29050-123">The array of values is one-based.</span></span> <span data-ttu-id="29050-124">Il primo valore è Sequence 1, non 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="29050-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="29050-125">Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence se tale valore viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="29050-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="29050-126">Il valore 0 (zero) indica di aggiungere una nuova istanza di valore di colonna alla fine della sequenza dei valori di colonna.</span><span class="sxs-lookup"><span data-stu-id="29050-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="29050-127">Inizio</span><span class="sxs-lookup"><span data-stu-id="29050-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="29050-128">Metodi</span><span class="sxs-lookup"><span data-stu-id="29050-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="29050-129">Nome</span><span class="sxs-lookup"><span data-stu-id="29050-129">Name</span></span></th>
<th><span data-ttu-id="29050-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29050-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="29050-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="29050-133">Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="29050-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="29050-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="29050-136">Restituisce una copia completa dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29050-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="29050-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="29050-139">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="29050-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="29050-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="29050-142">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="29050-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="29050-145">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="29050-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="29050-148">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="29050-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="29050-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="29050-151">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="29050-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="29050-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="29050-154">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="29050-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="29050-155">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="29050-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="29050-156">Inizio</span><span class="sxs-lookup"><span data-stu-id="29050-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="29050-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29050-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="29050-158">Riferimento</span><span class="sxs-lookup"><span data-stu-id="29050-158">Reference</span></span>

[<span data-ttu-id="29050-159">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="29050-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="29050-160">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="29050-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
