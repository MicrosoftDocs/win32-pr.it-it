---
description: 'Altre informazioni su: metodo API. TrySetIndexRange'
title: API. TrySetIndexRange, metodo
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d175fdfc931d24742d61f962a45e690a5c49c2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760070"
---
# <a name="apitrysetindexrange-method"></a><span data-ttu-id="1bcc2-103">API. TrySetIndexRange, metodo</span><span class="sxs-lookup"><span data-stu-id="1bcc2-103">Api.TrySetIndexRange method</span></span>

<span data-ttu-id="1bcc2-104">Limita temporaneamente il set di voci di indice che il cursore può utilizzare JetMove a quelli che iniziano dalla voce di indice corrente fino alla voce di indice corrispondente ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e ai criteri associati specificati.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-104">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="1bcc2-105">È necessario che una chiave di ricerca sia stata costruita in precedenza usando JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-105">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="1bcc2-106">Restituisce true se l'intervallo di indici non è vuoto; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-106">Returns true if the index range is non-empty, false otherwise.</span></span>

<span data-ttu-id="1bcc2-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1bcc2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1bcc2-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1bcc2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1bcc2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bcc2-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1bcc2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bcc2-110">Parameters</span></span>

  - <span data-ttu-id="1bcc2-111">sesid</span><span class="sxs-lookup"><span data-stu-id="1bcc2-111">sesid</span></span>  
    <span data-ttu-id="1bcc2-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1bcc2-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1bcc2-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1bcc2-114">TableID</span><span class="sxs-lookup"><span data-stu-id="1bcc2-114">tableid</span></span>  
    <span data-ttu-id="1bcc2-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1bcc2-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1bcc2-116">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="1bcc2-117">grbit</span><span class="sxs-lookup"><span data-stu-id="1bcc2-117">grbit</span></span>  
    <span data-ttu-id="1bcc2-118">Tipo: [Microsoft. ISAM. esent. Interop. SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1bcc2-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1bcc2-119">Opzione Seek.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-119">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1bcc2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bcc2-120">Return value</span></span>

<span data-ttu-id="1bcc2-121">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1bcc2-121">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1bcc2-122">True se la ricerca ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1bcc2-122">True if the seek was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bcc2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bcc2-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1bcc2-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1bcc2-124">Reference</span></span>

[<span data-ttu-id="1bcc2-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="1bcc2-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1bcc2-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="1bcc2-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1bcc2-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1bcc2-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
