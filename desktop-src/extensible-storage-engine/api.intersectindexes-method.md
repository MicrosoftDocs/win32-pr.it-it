---
description: 'Altre informazioni su: metodo API. IntersectIndexes'
title: API. IntersectIndexes, metodo
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524777"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="53123-103">API. IntersectIndexes, metodo</span><span class="sxs-lookup"><span data-stu-id="53123-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="53123-104">Intersecare un gruppo di intervalli di indice e restituire i segnalibri dei record presenti in tutti gli intervalli di indice.</span><span class="sxs-lookup"><span data-stu-id="53123-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="53123-105">Vedere anche [JetIntersectIndexes (JET_SESID, \[ \] , Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="53123-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="53123-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53123-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53123-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53123-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53123-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53123-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="53123-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="53123-109">Parameters</span></span>

  - <span data-ttu-id="53123-110">sesid</span><span class="sxs-lookup"><span data-stu-id="53123-110">sesid</span></span>  
    <span data-ttu-id="53123-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53123-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="53123-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="53123-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="53123-113">tableids</span><span class="sxs-lookup"><span data-stu-id="53123-113">tableids</span></span>  
    <span data-ttu-id="53123-114">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="53123-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="53123-115">TableIDs da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="53123-115">The tableids to use.</span></span> <span data-ttu-id="53123-116">Ogni TableID deve provenire da un indice diverso nella stessa tabella e avere un intervallo di indice attivo.</span><span class="sxs-lookup"><span data-stu-id="53123-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="53123-117">Per creare un intervallo di indici, usare [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) .</span><span class="sxs-lookup"><span data-stu-id="53123-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="53123-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53123-118">Return value</span></span>

<span data-ttu-id="53123-119">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="53123-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="53123-120">Segnalibri dei record trovati in tutti gli intervalli di indice.</span><span class="sxs-lookup"><span data-stu-id="53123-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="53123-121">I segnalibri vengono restituiti nell'ordine delle chiavi primarie.</span><span class="sxs-lookup"><span data-stu-id="53123-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="53123-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53123-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53123-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="53123-123">Reference</span></span>

[<span data-ttu-id="53123-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="53123-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="53123-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="53123-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="53123-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53123-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
