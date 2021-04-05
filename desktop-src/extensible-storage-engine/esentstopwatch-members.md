---
description: 'Altre informazioni su: membri di EsentStopwatch'
title: Membri di EsentStopwatch
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757988"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="3a712-103">Membri di EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="3a712-103">EsentStopwatch members</span></span>

<span data-ttu-id="3a712-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="3a712-104">Include protected members</span></span>  
<span data-ttu-id="3a712-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="3a712-105">Include inherited members</span></span>  

<span data-ttu-id="3a712-106">Fornisce un set di metodi e proprietà che è possibile usare per misurare le statistiche di lavoro di ESENT per un thread.</span><span class="sxs-lookup"><span data-stu-id="3a712-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="3a712-107">Se la versione corrente di ESENT non supporta [JetGetThreadStats (JET_THREADSTATS),](./vistaapi.jetgetthreadstats-method.md) tutte le statistiche ESENT saranno pari a 0.</span><span class="sxs-lookup"><span data-stu-id="3a712-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="3a712-108">Il tipo [EsentStopwatch](./esentstopwatch-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a712-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="3a712-109">Costruttori</span><span class="sxs-lookup"><span data-stu-id="3a712-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3a712-110">Nome</span><span class="sxs-lookup"><span data-stu-id="3a712-110">Name</span></span></th>
<th><span data-ttu-id="3a712-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a712-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span><span class="sxs-lookup"><span data-stu-id="3a712-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a712-114">Inizio</span><span class="sxs-lookup"><span data-stu-id="3a712-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="3a712-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a712-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3a712-116">Nome</span><span class="sxs-lookup"><span data-stu-id="3a712-116">Name</span></span></th>
<th><span data-ttu-id="3a712-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a712-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="3a712-119"><a href="dn334934(v=exchg.10).md">Trascorso</a></span><span class="sxs-lookup"><span data-stu-id="3a712-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="3a712-120">Ottiene il tempo totale trascorso misurato dall'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="3a712-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="3a712-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span><span class="sxs-lookup"><span data-stu-id="3a712-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="3a712-123">Ottiene un valore che indica se il timer EsentStopwatch è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3a712-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="3a712-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span><span class="sxs-lookup"><span data-stu-id="3a712-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="3a712-126">Ottiene le statistiche di lavoro ESENT totali misurate dall'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="3a712-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a712-127">Inizio</span><span class="sxs-lookup"><span data-stu-id="3a712-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="3a712-128">Metodi</span><span class="sxs-lookup"><span data-stu-id="3a712-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3a712-129">Nome</span><span class="sxs-lookup"><span data-stu-id="3a712-129">Name</span></span></th>
<th><span data-ttu-id="3a712-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a712-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="3a712-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3a712-133">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3a712-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3a712-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="3a712-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="3a712-136">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3a712-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3a712-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3a712-139">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3a712-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3a712-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3a712-142">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3a712-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3a712-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="3a712-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3a712-145">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3a712-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-147"><a href="dn334869(v=exchg.10).md">Reimpostazione</a></span><span class="sxs-lookup"><span data-stu-id="3a712-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="3a712-148">Interrompe la misurazione dell'intervallo di tempo e reimposta le statistiche del thread.</span><span class="sxs-lookup"><span data-stu-id="3a712-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-150"><a href="dn334931(v=exchg.10).md">Inizia</a></span><span class="sxs-lookup"><span data-stu-id="3a712-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="3a712-151">Inizia a misurare il lavoro di ESENT.</span><span class="sxs-lookup"><span data-stu-id="3a712-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="3a712-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span><span class="sxs-lookup"><span data-stu-id="3a712-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="3a712-155">Inizializza una nuova istanza di EsentStopwatch e avvia la misurazione del tempo trascorso.</span><span class="sxs-lookup"><span data-stu-id="3a712-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-157"><a href="dn334932(v=exchg.10).md">Stop</a></span><span class="sxs-lookup"><span data-stu-id="3a712-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="3a712-158">Interrompe la misurazione del lavoro ESENT.</span><span class="sxs-lookup"><span data-stu-id="3a712-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3a712-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3a712-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3a712-161">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta il <a href="/dotnet/api/system.diagnostics.stopwatch">cronometro</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="3a712-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="3a712-162">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="3a712-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a712-163">Inizio</span><span class="sxs-lookup"><span data-stu-id="3a712-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3a712-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a712-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a712-165">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3a712-165">Reference</span></span>

[<span data-ttu-id="3a712-166">Classe EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="3a712-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="3a712-167">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3a712-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
