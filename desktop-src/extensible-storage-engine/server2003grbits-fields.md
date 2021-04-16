---
description: 'Altre informazioni su: campi Server2003Grbits'
title: Campi Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556303"
---
# <a name="server2003grbits-fields"></a><span data-ttu-id="a40f7-103">Campi Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="a40f7-103">Server2003Grbits fields</span></span>

<span data-ttu-id="a40f7-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="a40f7-104">Include protected members</span></span>  
<span data-ttu-id="a40f7-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="a40f7-105">Include inherited members</span></span>  

<span data-ttu-id="a40f7-106">Il tipo [Server2003Grbits](./server2003grbits-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a40f7-106">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="a40f7-107">Campi</span><span class="sxs-lookup"><span data-stu-id="a40f7-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a40f7-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a40f7-108">Name</span></span></th>
<th><span data-ttu-id="a40f7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40f7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="a40f7-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="a40f7-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="a40f7-113">Se una colonna specificata non è presente nel record e presenta un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="a40f7-113">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="a40f7-114">Questa opzione impedisce al callback che calcola il valore predefinito definito dall'utente per la colonna di essere chiamato durante l'enumerazione dei valori per la colonna.</span><span class="sxs-lookup"><span data-stu-id="a40f7-114">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="a40f7-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="a40f7-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="a40f7-118">Questa opzione richiede che la tabella temporanea venga creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query.</span><span class="sxs-lookup"><span data-stu-id="a40f7-118">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="a40f7-119">Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="a40f7-119">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="a40f7-120">Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate.</span><span class="sxs-lookup"><span data-stu-id="a40f7-120">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="a40f7-121">Per ulteriori informazioni, vedere <a href="hh558517(v=exchg.10).md">Unique</a> .</span><span class="sxs-lookup"><span data-stu-id="a40f7-121">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="a40f7-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="a40f7-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="a40f7-125">Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="a40f7-125">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="a40f7-126">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="a40f7-126">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="a40f7-127">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="a40f7-127">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="a40f7-128">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="a40f7-128">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a40f7-129">Inizio</span><span class="sxs-lookup"><span data-stu-id="a40f7-129">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a40f7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a40f7-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a40f7-131">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a40f7-131">Reference</span></span>

[<span data-ttu-id="a40f7-132">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="a40f7-132">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="a40f7-133">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="a40f7-133">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
