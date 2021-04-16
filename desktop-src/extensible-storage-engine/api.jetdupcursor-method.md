---
description: 'Altre informazioni su: metodo API. JetDupCursor'
title: API. JetDupCursor, metodo
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525632"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="5a6d8-103">API. JetDupCursor, metodo</span><span class="sxs-lookup"><span data-stu-id="5a6d8-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="5a6d8-104">Duplica un cursore aperto e restituisce un handle per il cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="5a6d8-105">Se il cursore duplicato era un cursore di sola lettura, il cursore duplicato è anche un cursore di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="5a6d8-106">Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="5a6d8-107">Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="5a6d8-108">Il cursore duplicato viene sempre aperto nell'indice cluster e il relativo percorso è sempre nella prima riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="5a6d8-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a6d8-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a6d8-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a6d8-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6d8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a6d8-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5a6d8-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a6d8-112">Parameters</span></span>

  - <span data-ttu-id="5a6d8-113">sesid</span><span class="sxs-lookup"><span data-stu-id="5a6d8-113">sesid</span></span>  
    <span data-ttu-id="5a6d8-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a6d8-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5a6d8-115">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a6d8-116">TableID</span><span class="sxs-lookup"><span data-stu-id="5a6d8-116">tableid</span></span>  
    <span data-ttu-id="5a6d8-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a6d8-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5a6d8-118">Cursore da duplicare.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a6d8-119">newTableid</span><span class="sxs-lookup"><span data-stu-id="5a6d8-119">newTableid</span></span>  
    <span data-ttu-id="5a6d8-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a6d8-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5a6d8-121">Cursore duplicato.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a6d8-122">grbit</span><span class="sxs-lookup"><span data-stu-id="5a6d8-122">grbit</span></span>  
    <span data-ttu-id="5a6d8-123">Tipo: [Microsoft. ISAM. esent. Interop. DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5a6d8-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5a6d8-124">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="5a6d8-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a6d8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a6d8-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a6d8-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5a6d8-126">Reference</span></span>

[<span data-ttu-id="5a6d8-127">Classe API</span><span class="sxs-lookup"><span data-stu-id="5a6d8-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5a6d8-128">Membri API</span><span class="sxs-lookup"><span data-stu-id="5a6d8-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5a6d8-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5a6d8-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
