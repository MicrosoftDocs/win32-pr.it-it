---
description: 'Altre informazioni su: membri di Server2003Grbits'
title: Membri di Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882257"
---
# <a name="server2003grbits-members"></a><span data-ttu-id="a602c-103">Membri di Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="a602c-103">Server2003Grbits members</span></span>

<span data-ttu-id="a602c-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="a602c-104">Include protected members</span></span>  
<span data-ttu-id="a602c-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="a602c-105">Include inherited members</span></span>  

<span data-ttu-id="a602c-106">Grbits che sono stati aggiunti alla versione Windows Server 2003 di ESENT.</span><span class="sxs-lookup"><span data-stu-id="a602c-106">Grbits that have been added to the Windows Server 2003 version of ESENT.</span></span>

<span data-ttu-id="a602c-107">Il tipo [Server2003Grbits](./server2003grbits-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a602c-107">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="a602c-108">Campi</span><span class="sxs-lookup"><span data-stu-id="a602c-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a602c-109">Nome</span><span class="sxs-lookup"><span data-stu-id="a602c-109">Name</span></span></th>
<th><span data-ttu-id="a602c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a602c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="a602c-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="a602c-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="a602c-114">Se una colonna specificata non è presente nel record e presenta un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="a602c-114">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="a602c-115">Questa opzione impedisce al callback che calcola il valore predefinito definito dall'utente per la colonna di essere chiamato durante l'enumerazione dei valori per la colonna.</span><span class="sxs-lookup"><span data-stu-id="a602c-115">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="a602c-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="a602c-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="a602c-119">Questa opzione richiede che la tabella temporanea venga creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query.</span><span class="sxs-lookup"><span data-stu-id="a602c-119">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="a602c-120">Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="a602c-120">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="a602c-121">Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate.</span><span class="sxs-lookup"><span data-stu-id="a602c-121">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="a602c-122">Per ulteriori informazioni, vedere <a href="hh558517(v=exchg.10).md">Unique</a> .</span><span class="sxs-lookup"><span data-stu-id="a602c-122">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="a602c-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="a602c-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="a602c-126">Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="a602c-126">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="a602c-127">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="a602c-127">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="a602c-128">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="a602c-128">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="a602c-129">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="a602c-129">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a602c-130">Inizio</span><span class="sxs-lookup"><span data-stu-id="a602c-130">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a602c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a602c-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a602c-132">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a602c-132">Reference</span></span>

[<span data-ttu-id="a602c-133">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="a602c-133">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="a602c-134">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="a602c-134">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
