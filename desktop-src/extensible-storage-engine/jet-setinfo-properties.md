---
description: 'Altre informazioni su: Proprietà JET_SETINFO'
title: Proprietà JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128647"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="93c42-103">Proprietà JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="93c42-103">JET_SETINFO properties</span></span>

<span data-ttu-id="93c42-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="93c42-104">Include protected members</span></span>  
<span data-ttu-id="93c42-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="93c42-105">Include inherited members</span></span>  

<span data-ttu-id="93c42-106">Il tipo di [JET_SETINFO](./jet-setinfo-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="93c42-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="93c42-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93c42-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="93c42-108">Nome</span><span class="sxs-lookup"><span data-stu-id="93c42-108">Name</span></span></th>
<th><span data-ttu-id="93c42-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c42-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="93c42-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="93c42-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="93c42-112">Ottiene o imposta l'offset al primo byte da impostare in una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="93c42-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="93c42-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="93c42-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="93c42-115">Ottiene o imposta il numero di sequenza del valore in una colonna multivalore da impostare.</span><span class="sxs-lookup"><span data-stu-id="93c42-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="93c42-116">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="93c42-116">The array of values is one-based.</span></span> <span data-ttu-id="93c42-117">Il primo valore è Sequence 1, non 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="93c42-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="93c42-118">Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence se tale valore viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="93c42-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="93c42-119">Il valore 0 (zero) indica di aggiungere una nuova istanza di valore di colonna alla fine della sequenza dei valori di colonna.</span><span class="sxs-lookup"><span data-stu-id="93c42-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93c42-120">Inizio</span><span class="sxs-lookup"><span data-stu-id="93c42-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="93c42-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93c42-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="93c42-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="93c42-122">Reference</span></span>

[<span data-ttu-id="93c42-123">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="93c42-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="93c42-124">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="93c42-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
