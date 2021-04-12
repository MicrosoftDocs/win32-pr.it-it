---
description: 'Altre informazioni su: metodo API. JetRetrieveColumn'
title: API. JetRetrieveColumn, metodo
TOCTitle: 'JetRetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100791
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: e4e43d57f4393d6b0d4ce2f1cdbe4ecd8338ec54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233973"
---
# <a name="apijetretrievecolumn-method"></a><span data-ttu-id="67f68-103">API. JetRetrieveColumn, metodo</span><span class="sxs-lookup"><span data-stu-id="67f68-103">Api.JetRetrieveColumn method</span></span>

<span data-ttu-id="67f68-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="67f68-104">Include protected members</span></span>  
<span data-ttu-id="67f68-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="67f68-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="67f68-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="67f68-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="67f68-107">Nome</span><span class="sxs-lookup"><span data-stu-id="67f68-107">Name</span></span></th>
<th><span data-ttu-id="67f68-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67f68-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="67f68-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="67f68-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="67f68-112">Recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="67f68-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="67f68-113">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="67f68-113">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="67f68-114">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="67f68-114">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="67f68-115">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="67f68-115">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="67f68-116">Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="67f68-116">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="67f68-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="67f68-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="67f68-120">Recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="67f68-120">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="67f68-121">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="67f68-121">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="67f68-122">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="67f68-122">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="67f68-123">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="67f68-123">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="67f68-124">Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="67f68-124">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67f68-125">Inizio</span><span class="sxs-lookup"><span data-stu-id="67f68-125">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="67f68-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67f68-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67f68-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="67f68-127">Reference</span></span>

[<span data-ttu-id="67f68-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="67f68-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="67f68-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="67f68-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="67f68-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="67f68-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
