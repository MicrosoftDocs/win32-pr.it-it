---
description: 'Altre informazioni su: metodi di transazione'
title: 'Metodi di Transaction '
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562396"
---
# <a name="transaction-methods"></a><span data-ttu-id="31bdb-103">Metodi di Transaction </span><span class="sxs-lookup"><span data-stu-id="31bdb-103">Transaction methods</span></span>

<span data-ttu-id="31bdb-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="31bdb-104">Include protected members</span></span>  
<span data-ttu-id="31bdb-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="31bdb-105">Include inherited members</span></span>  

<span data-ttu-id="31bdb-106">Il tipo di [transazione](./transaction-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="31bdb-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="31bdb-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="31bdb-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="31bdb-108">Nome</span><span class="sxs-lookup"><span data-stu-id="31bdb-108">Name</span></span></th>
<th><span data-ttu-id="31bdb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31bdb-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-111"><a href="dn351172(v=exchg.10).md">Inizia</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="31bdb-112">Inizia una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-112">Begin a transaction.</span></span> <span data-ttu-id="31bdb-113">Questo oggetto non deve essere attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="31bdb-116">Genera un'eccezione se l'oggetto è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="31bdb-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="31bdb-117">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-119"><a href="dn351179(v=exchg.10).md">Commit (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="31bdb-120">Eseguire il commit di una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-120">Commit a transaction.</span></span> <span data-ttu-id="31bdb-121">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-123"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="31bdb-124">Eseguire il commit di una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-124">Commit a transaction.</span></span> <span data-ttu-id="31bdb-125">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-127"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="31bdb-128">Eliminare questo oggetto, rilasciando la risorsa ESENT sottostante.</span><span class="sxs-lookup"><span data-stu-id="31bdb-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="31bdb-129">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-131"><a href="dn350543(v=exchg.10).md">Dispose (valore booleano)</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="31bdb-132">Chiamato da Dispose e dal finalizzatore.</span><span class="sxs-lookup"><span data-stu-id="31bdb-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="31bdb-133">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="31bdb-136">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="31bdb-139">Finalizza un'istanza della classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="31bdb-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="31bdb-140">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="31bdb-143">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="31bdb-146">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="31bdb-149">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="31bdb-152">Chiamato quando la transazione viene eliminata quando è attiva.</span><span class="sxs-lookup"><span data-stu-id="31bdb-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="31bdb-153">Questa operazione deve eseguire il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-153">This should rollback the transaction.</span></span> <span data-ttu-id="31bdb-154">Esegue l'override di <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="31bdb-157">Chiamato da una sottoclasse quando viene allocata una risorsa.</span><span class="sxs-lookup"><span data-stu-id="31bdb-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="31bdb-158">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="31bdb-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="31bdb-161">Chiamato da una sottoclasse quando una risorsa viene liberata.</span><span class="sxs-lookup"><span data-stu-id="31bdb-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="31bdb-162">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="31bdb-165">Eseguire il rollback di una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-165">Rollback a transaction.</span></span> <span data-ttu-id="31bdb-166">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="31bdb-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="31bdb-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="31bdb-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="31bdb-169">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn351174(v=exchg.10).md">transazione</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="31bdb-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="31bdb-170">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="31bdb-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31bdb-171">Inizio</span><span class="sxs-lookup"><span data-stu-id="31bdb-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="31bdb-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31bdb-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31bdb-173">Riferimento</span><span class="sxs-lookup"><span data-stu-id="31bdb-173">Reference</span></span>

[<span data-ttu-id="31bdb-174">Transaction (classe)</span><span class="sxs-lookup"><span data-stu-id="31bdb-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="31bdb-175">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="31bdb-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
