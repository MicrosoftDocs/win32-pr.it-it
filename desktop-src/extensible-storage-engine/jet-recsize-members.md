---
description: 'Altre informazioni su: membri JET_RECSIZE'
title: Membri di JET_RECSIZE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551823"
---
# <a name="jet_recsize-members"></a><span data-ttu-id="16ed7-103">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="16ed7-103">JET_RECSIZE members</span></span>

<span data-ttu-id="16ed7-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="16ed7-104">Include protected members</span></span>  
<span data-ttu-id="16ed7-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="16ed7-105">Include inherited members</span></span>  

<span data-ttu-id="16ed7-106">Utilizzato da [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) per restituire informazioni sui requisiti di utilizzo di un record nello spazio dati utente, il numero di colonne set, il numero di valori e lo spazio overhead della struttura del record esent.</span><span class="sxs-lookup"><span data-stu-id="16ed7-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="16ed7-107">Il tipo di [JET_RECSIZE](./jet-recsize-structure2.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="16ed7-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="16ed7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16ed7-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="16ed7-109">Nome</span><span class="sxs-lookup"><span data-stu-id="16ed7-109">Name</span></span></th>
<th><span data-ttu-id="16ed7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ed7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="16ed7-113">Ottiene il set di dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="16ed7-116">Ottiene la dimensione compressa dei dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="16ed7-117">Si tratta dello stesso valore di <a href="hh557581(v=exchg.10).md">cbData</a> se non vengono compressi valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="16ed7-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="16ed7-120">Ottiene il set di dati utente nel record, ma archiviato nell'albero dei valori Long.</span><span class="sxs-lookup"><span data-stu-id="16ed7-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="16ed7-123">Ottiene le dimensioni compresse dei dati utente nell'albero dei valori Long.</span><span class="sxs-lookup"><span data-stu-id="16ed7-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="16ed7-124">Si tratta dello stesso valore di <a href="hh557913(v=exchg.10).md">cbLongValueData</a> se nessun valore Long separato viene compresso.</span><span class="sxs-lookup"><span data-stu-id="16ed7-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="16ed7-127">Ottiene l'overhead dei dati con valori Long.</span><span class="sxs-lookup"><span data-stu-id="16ed7-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="16ed7-130">Ottiene l'overhead della struttura di record ESENT per questo record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="16ed7-131">Sono incluse le dimensioni della chiave del record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="16ed7-134">Ottiene il numero totale di colonne nel record compresse.</span><span class="sxs-lookup"><span data-stu-id="16ed7-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="16ed7-137">Ottiene il numero totale di valori Long archiviati nell'albero dei valori Long per questo record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="16ed7-138">Non sono inclusi i valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="16ed7-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="16ed7-141">Ottiene l'accumulo del numero totale di valori oltre il primo per tutte le colonne del record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="16ed7-144">Ottiene il numero totale di colonne fisse e variabili impostate in questo record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="16ed7-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="16ed7-147">Ottiene il numero totale di colonne con tag impostati in questo record.</span><span class="sxs-lookup"><span data-stu-id="16ed7-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16ed7-148">Inizio</span><span class="sxs-lookup"><span data-stu-id="16ed7-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="16ed7-149">Metodi</span><span class="sxs-lookup"><span data-stu-id="16ed7-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="16ed7-150">Nome</span><span class="sxs-lookup"><span data-stu-id="16ed7-150">Name</span></span></th>
<th><span data-ttu-id="16ed7-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ed7-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="16ed7-154"><a href="hh538879(v=exchg.10).md">Aggiungere</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="16ed7-155">Aggiungere le dimensioni in due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="16ed7-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="16ed7-157"><a href="hh558506(v=exchg.10).md">Equals (oggetto)</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="16ed7-158">Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="16ed7-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="16ed7-159">Esegue l'override di <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.</span><span class="sxs-lookup"><span data-stu-id="16ed7-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="16ed7-161"><a href="hh577992(v=exchg.10).md">Uguale a (JET_RECSIZE)</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="16ed7-162">Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="16ed7-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="16ed7-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="16ed7-165">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="16ed7-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="16ed7-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="16ed7-168">Restituisce il codice hash per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="16ed7-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="16ed7-169">Esegue l'override di <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.</span><span class="sxs-lookup"><span data-stu-id="16ed7-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="16ed7-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="16ed7-172">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="16ed7-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="16ed7-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="16ed7-175">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="16ed7-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="16ed7-178"><a href="hh579561(v=exchg.10).md">Sottrarre</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="16ed7-179">Calcolare la differenza di dimensioni tra due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="16ed7-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="16ed7-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="16ed7-182">Ereditato da <a href="/dotnet/api/system.valuetype">ValueType</a>.</span><span class="sxs-lookup"><span data-stu-id="16ed7-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16ed7-183">Inizio</span><span class="sxs-lookup"><span data-stu-id="16ed7-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="16ed7-184">Operatori</span><span class="sxs-lookup"><span data-stu-id="16ed7-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="16ed7-185">Nome</span><span class="sxs-lookup"><span data-stu-id="16ed7-185">Name</span></span></th>
<th><span data-ttu-id="16ed7-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ed7-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="16ed7-189"><a href="hh578675(v=exchg.10).md">Oltre</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="16ed7-190">Aggiungere le dimensioni in due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="16ed7-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="16ed7-193"><a href="hh596362(v=exchg.10).md">Uguaglianza</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="16ed7-194">Determina se due istanze specificate di JET_RECSIZE sono uguali.</span><span class="sxs-lookup"><span data-stu-id="16ed7-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="16ed7-197"><a href="hh578809(v=exchg.10).md">Disuguaglianza</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="16ed7-198">Determina se due istanze specificate di JET_RECSIZE non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="16ed7-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="16ed7-201"><a href="hh596696(v=exchg.10).md">Sottrazione</a></span><span class="sxs-lookup"><span data-stu-id="16ed7-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="16ed7-202">Calcolare la differenza di dimensioni tra due strutture di JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="16ed7-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16ed7-203">Inizio</span><span class="sxs-lookup"><span data-stu-id="16ed7-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="16ed7-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16ed7-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16ed7-205">Riferimento</span><span class="sxs-lookup"><span data-stu-id="16ed7-205">Reference</span></span>

[<span data-ttu-id="16ed7-206">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="16ed7-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="16ed7-207">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="16ed7-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
