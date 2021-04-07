---
description: 'Altre informazioni su: Proprietà JET_RECSIZE'
title: Proprietà JET_RECSIZE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885589"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="83cf8-103">Proprietà JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="83cf8-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="83cf8-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="83cf8-104">Include protected members</span></span>  
<span data-ttu-id="83cf8-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="83cf8-105">Include inherited members</span></span>  

<span data-ttu-id="83cf8-106">Il tipo di [JET_RECSIZE](./jet-recsize-structure2.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="83cf8-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="83cf8-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83cf8-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="83cf8-108">Nome</span><span class="sxs-lookup"><span data-stu-id="83cf8-108">Name</span></span></th>
<th><span data-ttu-id="83cf8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83cf8-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="83cf8-112">Ottiene il set di dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="83cf8-115">Ottiene la dimensione compressa dei dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="83cf8-116">Si tratta dello stesso valore di <a href="hh557581(v=exchg.10).md">cbData</a> se non vengono compressi valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="83cf8-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="83cf8-119">Ottiene il set di dati utente nel record, ma archiviato nell'albero dei valori Long.</span><span class="sxs-lookup"><span data-stu-id="83cf8-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="83cf8-122">Ottiene le dimensioni compresse dei dati utente nell'albero dei valori Long.</span><span class="sxs-lookup"><span data-stu-id="83cf8-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="83cf8-123">Si tratta dello stesso valore di <a href="hh557913(v=exchg.10).md">cbLongValueData</a> se nessun valore Long separato viene compresso.</span><span class="sxs-lookup"><span data-stu-id="83cf8-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="83cf8-126">Ottiene l'overhead dei dati con valori Long.</span><span class="sxs-lookup"><span data-stu-id="83cf8-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="83cf8-129">Ottiene l'overhead della struttura di record ESENT per questo record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="83cf8-130">Sono incluse le dimensioni della chiave del record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="83cf8-133">Ottiene il numero totale di colonne nel record compresse.</span><span class="sxs-lookup"><span data-stu-id="83cf8-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="83cf8-136">Ottiene il numero totale di valori Long archiviati nell'albero dei valori Long per questo record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="83cf8-137">Non sono inclusi i valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="83cf8-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="83cf8-140">Ottiene l'accumulo del numero totale di valori oltre il primo per tutte le colonne del record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="83cf8-143">Ottiene il numero totale di colonne fisse e variabili impostate in questo record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="83cf8-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="83cf8-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="83cf8-146">Ottiene il numero totale di colonne con tag impostati in questo record.</span><span class="sxs-lookup"><span data-stu-id="83cf8-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="83cf8-147">Inizio</span><span class="sxs-lookup"><span data-stu-id="83cf8-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="83cf8-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83cf8-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83cf8-149">Riferimento</span><span class="sxs-lookup"><span data-stu-id="83cf8-149">Reference</span></span>

[<span data-ttu-id="83cf8-150">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="83cf8-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="83cf8-151">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="83cf8-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
