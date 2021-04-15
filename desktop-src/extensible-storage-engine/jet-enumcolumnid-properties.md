---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMNID'
title: Proprietà JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525027"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="9f03e-103">Proprietà JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="9f03e-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="9f03e-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="9f03e-104">Include protected members</span></span>  
<span data-ttu-id="9f03e-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="9f03e-105">Include inherited members</span></span>  

<span data-ttu-id="9f03e-106">Il tipo di [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f03e-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="9f03e-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f03e-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9f03e-108">Nome</span><span class="sxs-lookup"><span data-stu-id="9f03e-108">Name</span></span></th>
<th><span data-ttu-id="9f03e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f03e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9f03e-111"><a href="dn335141(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="9f03e-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="9f03e-112">Ottiene o imposta l'ID ColumnID da enumerare.</span><span class="sxs-lookup"><span data-stu-id="9f03e-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9f03e-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="9f03e-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="9f03e-115">Ottiene o imposta il conteggio dei valori di colonna (in base a un indice in base 1) da enumerare per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="9f03e-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="9f03e-116">Se ctagSequence è 0 (zero), rgtagSequence viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.</span><span class="sxs-lookup"><span data-stu-id="9f03e-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9f03e-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="9f03e-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="9f03e-119">Ottiene o imposta la matrice di indici in base uno in una matrice di valori di colonna per una colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="9f03e-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="9f03e-120">Un singolo elemento è un itagSequence definito in JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="9f03e-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="9f03e-121">Un itagSequence pari a 0 (zero) indica &quot; Skip &quot; .</span><span class="sxs-lookup"><span data-stu-id="9f03e-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="9f03e-122">Un itagSequence di 1 indica che restituisce il primo valore della colonna, 2 indica il secondo e così via.</span><span class="sxs-lookup"><span data-stu-id="9f03e-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f03e-123">Inizio</span><span class="sxs-lookup"><span data-stu-id="9f03e-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9f03e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f03e-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f03e-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9f03e-125">Reference</span></span>

[<span data-ttu-id="9f03e-126">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="9f03e-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="9f03e-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9f03e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
