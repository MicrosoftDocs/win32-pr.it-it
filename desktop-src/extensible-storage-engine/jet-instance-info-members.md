---
description: 'Altre informazioni su: membri JET_INSTANCE_INFO'
title: Membri JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567594"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="42e41-103">Membri JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="42e41-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="42e41-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="42e41-104">Include protected members</span></span>  
<span data-ttu-id="42e41-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="42e41-105">Include inherited members</span></span>  

<span data-ttu-id="42e41-106">Riceve informazioni sulle istanze di database in esecuzione quando utilizzate con le funzioni JetGetInstanceInfo e JetOSSnapshotFreeze.</span><span class="sxs-lookup"><span data-stu-id="42e41-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="42e41-107">Il tipo di [JET_INSTANCE_INFO](./jet-instance-info-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="42e41-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="42e41-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42e41-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="42e41-109">Nome</span><span class="sxs-lookup"><span data-stu-id="42e41-109">Name</span></span></th>
<th><span data-ttu-id="42e41-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42e41-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="42e41-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span><span class="sxs-lookup"><span data-stu-id="42e41-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="42e41-113">Ottiene il numero di database collegati all'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="42e41-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="42e41-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span><span class="sxs-lookup"><span data-stu-id="42e41-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="42e41-116">Ottiene l'JET_INSTANCE dell'istanza di specificata.</span><span class="sxs-lookup"><span data-stu-id="42e41-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="42e41-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span><span class="sxs-lookup"><span data-stu-id="42e41-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="42e41-119">Ottiene una raccolta di stringhe, ognuna delle quali contiene il nome file di un database associato all'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="42e41-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="42e41-120">La matrice contiene elementi cDatabases.</span><span class="sxs-lookup"><span data-stu-id="42e41-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="42e41-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span><span class="sxs-lookup"><span data-stu-id="42e41-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="42e41-123">Ottiene il nome dell'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="42e41-123">Gets the name of the database instance.</span></span> <span data-ttu-id="42e41-124">Questo valore può essere null se l'istanza non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="42e41-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42e41-125">Inizio</span><span class="sxs-lookup"><span data-stu-id="42e41-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="42e41-126">Metodi</span><span class="sxs-lookup"><span data-stu-id="42e41-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="42e41-127">Nome</span><span class="sxs-lookup"><span data-stu-id="42e41-127">Name</span></span></th>
<th><span data-ttu-id="42e41-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42e41-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="42e41-130"><a href="dn335184(v=exchg.10).md">Equals (oggetto)</a></span><span class="sxs-lookup"><span data-stu-id="42e41-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="42e41-131">Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="42e41-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="42e41-132">Esegue l'override di <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.</span><span class="sxs-lookup"><span data-stu-id="42e41-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="42e41-134"><a href="dn335187(v=exchg.10).md">Uguale a (JET_INSTANCE_INFO)</a></span><span class="sxs-lookup"><span data-stu-id="42e41-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="42e41-135">Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="42e41-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="42e41-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="42e41-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="42e41-138">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="42e41-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="42e41-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="42e41-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="42e41-141">Restituisce il codice hash per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="42e41-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="42e41-142">Esegue l'override di <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.</span><span class="sxs-lookup"><span data-stu-id="42e41-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="42e41-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="42e41-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="42e41-145">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="42e41-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="42e41-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="42e41-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="42e41-148">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="42e41-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="42e41-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="42e41-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="42e41-151">Generare una rappresentazione di stringa dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="42e41-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="42e41-152">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="42e41-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42e41-153">Inizio</span><span class="sxs-lookup"><span data-stu-id="42e41-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="42e41-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42e41-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42e41-155">Riferimento</span><span class="sxs-lookup"><span data-stu-id="42e41-155">Reference</span></span>

[<span data-ttu-id="42e41-156">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="42e41-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="42e41-157">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="42e41-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
