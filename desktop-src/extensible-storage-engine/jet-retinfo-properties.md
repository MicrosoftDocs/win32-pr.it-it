---
description: 'Altre informazioni su: Proprietà JET_RETINFO'
title: Proprietà JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566792"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="ad01e-103">Proprietà JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="ad01e-103">JET_RETINFO properties</span></span>

<span data-ttu-id="ad01e-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="ad01e-104">Include protected members</span></span>  
<span data-ttu-id="ad01e-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="ad01e-105">Include inherited members</span></span>  

<span data-ttu-id="ad01e-106">Il tipo di [JET_RETINFO](./jet-retinfo-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad01e-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="ad01e-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad01e-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ad01e-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ad01e-108">Name</span></span></th>
<th><span data-ttu-id="ad01e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad01e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ad01e-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="ad01e-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="ad01e-112">Ottiene l'ColumnID della colonna con tag, multivalore o di tipo sparse recuperata quando tutte le colonne con tag vengono recuperate passando 0 come ColumnID a JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="ad01e-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ad01e-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="ad01e-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="ad01e-115">Ottiene o imposta l'offset al primo byte da recuperare da una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a>o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="ad01e-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ad01e-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="ad01e-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="ad01e-118">Ottiene o imposta il numero di sequenza del valore in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="ad01e-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="ad01e-119">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="ad01e-119">The array of values is one-based.</span></span> <span data-ttu-id="ad01e-120">Il primo valore è Sequence 1, not 0.</span><span class="sxs-lookup"><span data-stu-id="ad01e-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="ad01e-121">Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence.</span><span class="sxs-lookup"><span data-stu-id="ad01e-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad01e-122">Inizio</span><span class="sxs-lookup"><span data-stu-id="ad01e-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ad01e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad01e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad01e-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ad01e-124">Reference</span></span>

[<span data-ttu-id="ad01e-125">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="ad01e-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="ad01e-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ad01e-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
