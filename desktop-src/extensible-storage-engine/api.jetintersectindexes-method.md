---
description: 'Altre informazioni su: metodo API. JetIntersectIndexes'
title: API. JetIntersectIndexes, metodo
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968644"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="902ec-103">API. JetIntersectIndexes, metodo</span><span class="sxs-lookup"><span data-stu-id="902ec-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="902ec-104">Calcola l'intersezione tra più set di voci di indice da indici secondari diversi nella stessa tabella.</span><span class="sxs-lookup"><span data-stu-id="902ec-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="902ec-105">Questa operazione è utile per trovare il set di record in una tabella che corrisponde a due o più criteri che possono essere espressi utilizzando intervalli di indice.</span><span class="sxs-lookup"><span data-stu-id="902ec-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="902ec-106">Vedere anche [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="902ec-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="902ec-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="902ec-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="902ec-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="902ec-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="902ec-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="902ec-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="902ec-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="902ec-110">Parameters</span></span>

  - <span data-ttu-id="902ec-111">sesid</span><span class="sxs-lookup"><span data-stu-id="902ec-111">sesid</span></span>  
    <span data-ttu-id="902ec-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="902ec-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="902ec-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="902ec-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="902ec-114">ranges</span><span class="sxs-lookup"><span data-stu-id="902ec-114">ranges</span></span>  
    <span data-ttu-id="902ec-115">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="902ec-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="902ec-116">Gli intervalli di indice da intersecare.</span><span class="sxs-lookup"><span data-stu-id="902ec-116">An the index ranges to intersect.</span></span> <span data-ttu-id="902ec-117">Per TableIDs negli intervalli devono essere impostati intervalli di indice.</span><span class="sxs-lookup"><span data-stu-id="902ec-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="902ec-118">Per creare un intervallo di indici, usare [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) .</span><span class="sxs-lookup"><span data-stu-id="902ec-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="902ec-119">numRanges</span><span class="sxs-lookup"><span data-stu-id="902ec-119">numRanges</span></span>  
    <span data-ttu-id="902ec-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="902ec-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="902ec-121">Numero di intervalli di indice.</span><span class="sxs-lookup"><span data-stu-id="902ec-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="902ec-122">Recording</span><span class="sxs-lookup"><span data-stu-id="902ec-122">recordlist</span></span>  
    <span data-ttu-id="902ec-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="902ec-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="902ec-124">Restituisce informazioni sulla tabella temporanea contenente i risultati dell'intersezione.</span><span class="sxs-lookup"><span data-stu-id="902ec-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="902ec-125">grbit</span><span class="sxs-lookup"><span data-stu-id="902ec-125">grbit</span></span>  
    <span data-ttu-id="902ec-126">Tipo: [Microsoft. ISAM. esent. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="902ec-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="902ec-127">Opzioni di intersezione.</span><span class="sxs-lookup"><span data-stu-id="902ec-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="902ec-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="902ec-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="902ec-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="902ec-129">Reference</span></span>

[<span data-ttu-id="902ec-130">Classe API</span><span class="sxs-lookup"><span data-stu-id="902ec-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="902ec-131">Membri API</span><span class="sxs-lookup"><span data-stu-id="902ec-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="902ec-132">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="902ec-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
