---
description: 'Altre informazioni su: membri transazione'
title: 'Membri di Transaction '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555596"
---
# <a name="transaction-members"></a><span data-ttu-id="3cfb9-103">Membri di Transaction </span><span class="sxs-lookup"><span data-stu-id="3cfb9-103">Transaction members</span></span>

<span data-ttu-id="3cfb9-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="3cfb9-104">Include protected members</span></span>  
<span data-ttu-id="3cfb9-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="3cfb9-105">Include inherited members</span></span>  

<span data-ttu-id="3cfb9-106">Classe che incapsula una transazione in un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="3cfb9-107">Il tipo di [transazione](./transaction-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="3cfb9-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="3cfb9-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3cfb9-109">Nome</span><span class="sxs-lookup"><span data-stu-id="3cfb9-109">Name</span></span></th>
<th><span data-ttu-id="3cfb9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cfb9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-112"><a href="dn351177(v=exchg.10).md">Transazione</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="3cfb9-113">Inizializza una nuova istanza della classe Transaction.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="3cfb9-114">Viene avviata automaticamente una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-114">This automatically begins a transaction.</span></span> <span data-ttu-id="3cfb9-115">Se non viene eseguito il commit esplicito, verrà eseguito il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3cfb9-116">Inizio</span><span class="sxs-lookup"><span data-stu-id="3cfb9-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="3cfb9-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3cfb9-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3cfb9-118">Nome</span><span class="sxs-lookup"><span data-stu-id="3cfb9-118">Name</span></span></th>
<th><span data-ttu-id="3cfb9-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cfb9-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Proprietà protetta." alt="Protected property" /></td>
<td><span data-ttu-id="3cfb9-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="3cfb9-122">Ottiene un valore che indica se la risorsa sottostante è attualmente allocata.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="3cfb9-123">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="3cfb9-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="3cfb9-126">Ottiene un valore che indica se l'oggetto è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3cfb9-127">Inizio</span><span class="sxs-lookup"><span data-stu-id="3cfb9-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="3cfb9-128">Metodi</span><span class="sxs-lookup"><span data-stu-id="3cfb9-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3cfb9-129">Nome</span><span class="sxs-lookup"><span data-stu-id="3cfb9-129">Name</span></span></th>
<th><span data-ttu-id="3cfb9-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cfb9-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-132"><a href="dn351172(v=exchg.10).md">Inizia</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="3cfb9-133">Inizia una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-133">Begin a transaction.</span></span> <span data-ttu-id="3cfb9-134">Questo oggetto non deve essere attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="3cfb9-137">Genera un'eccezione se l'oggetto è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="3cfb9-138">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-140"><a href="dn351179(v=exchg.10).md">Commit (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="3cfb9-141">Eseguire il commit di una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-141">Commit a transaction.</span></span> <span data-ttu-id="3cfb9-142">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-144"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="3cfb9-145">Eseguire il commit di una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-145">Commit a transaction.</span></span> <span data-ttu-id="3cfb9-146">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-148"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="3cfb9-149">Eliminare questo oggetto, rilasciando la risorsa ESENT sottostante.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="3cfb9-150">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-152"><a href="dn350543(v=exchg.10).md">Dispose (valore booleano)</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="3cfb9-153">Chiamato da Dispose e dal finalizzatore.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="3cfb9-154">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3cfb9-157">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="3cfb9-160">Finalizza un'istanza della classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="3cfb9-161">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3cfb9-164">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3cfb9-167">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3cfb9-170">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="3cfb9-173">Chiamato quando la transazione viene eliminata quando è attiva.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="3cfb9-174">Questa operazione deve eseguire il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-174">This should rollback the transaction.</span></span> <span data-ttu-id="3cfb9-175">Esegue l'override di <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="3cfb9-178">Chiamato da una sottoclasse quando viene allocata una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="3cfb9-179">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="3cfb9-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="3cfb9-182">Chiamato da una sottoclasse quando una risorsa viene liberata.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="3cfb9-183">Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="3cfb9-186">Eseguire il rollback di una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-186">Rollback a transaction.</span></span> <span data-ttu-id="3cfb9-187">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="3cfb9-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3cfb9-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3cfb9-190">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn351174(v=exchg.10).md">transazione</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="3cfb9-191">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="3cfb9-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3cfb9-192">Inizio</span><span class="sxs-lookup"><span data-stu-id="3cfb9-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3cfb9-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cfb9-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3cfb9-194">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3cfb9-194">Reference</span></span>

[<span data-ttu-id="3cfb9-195">Transaction (classe)</span><span class="sxs-lookup"><span data-stu-id="3cfb9-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="3cfb9-196">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3cfb9-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
